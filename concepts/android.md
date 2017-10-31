# <a name="get-started-with-microsoft-graph-in-an-android-app"></a>Introducción a Microsoft Graph en una aplicación de Android

> **¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores. 

> Para admitir **todos los clientes empresariales** en **todos los escenarios de empresa**, deberá usar el punto de conexión de Azure AD y administrar las aplicaciones mediante el [Portal de administración de Azure](https://aka.ms/aadapplist). Para obtener más información, consulte [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0 ](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión v2.0 de Azure AD y llamar a Microsoft Graph. Le muestra los pasos para la creación del [Ejemplo Connect de Android](https://github.com/microsoftgraph/android-java-connect-sample) y explica los conceptos principales que implementará para usar Microsoft Graph en la aplicación de Android. En el artículo, también se describe cómo obtener acceso a Microsoft Graph usando el [SDK de Microsoft Graph para Android](https://github.com/microsoftgraph/msgraph-sdk-android) o llamadas de REST sin procesar.

Para usar Microsoft Graph en su aplicación para Android, debe mostrar la página de inicio de sesión de Microsoft a los usuarios, como se muestra en la siguiente captura de pantalla.

![Página de inicio de sesión para cuentas Microsoft en Android](images/AndroidConnect.png)

<br/>

**¿No desea compilar una aplicación?** Puede ponerse a trabajar rápidamente si descarga el [Ejemplo Connect de Android](https://github.com/microsoftgraph/android-java-connect-sample) en el que se basa este artículo.


## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

- Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](http://dev.office.com/devprogram)
- Android Studio 2.0 o una versión más reciente


## <a name="configure-a-new-project"></a>Configurar un proyecto nuevo

Si ha descargado el [Ejemplo de conexión para Android](https://github.com/microsoftgraph/android-java-connect-sample), omita este paso. 

Inicie un nuevo proyecto en Android Studio. Puede dejar los valores predeterminados para la mayoría del proceso del asistente, pero asegúrese de elegir las siguientes opciones:

- Dispositivos Android objetivo: **Teléfono y tableta**
- SDK mínimo: **API 16: Android 4.1 (Jelly Bean)**
- Agregar una actividad a Mobile: **Actividad básica**
 
Esto le proporciona un proyecto de Android con una actividad y un botón que puede usar para autenticar al usuario.


## <a name="register-the-application"></a>Registrar la aplicación

Necesita registrar la aplicación en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/), independientemente de si descargó el ejemplo de conexión o si creó un proyecto nuevo.

Registre una aplicación en el portal de registro de aplicaciones de Microsoft. Este proceso generará el id. de aplicación y la contraseña que usará para configurar la aplicación.

1. Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.

2. Seleccione **Agregar una aplicación**.

    > **Sugerencia:** Si descargó el [Ejemplo de conexión para Android](https://github.com/microsoftgraph/android-java-connect-sample) y simplemente está creando un registro para este, desactive la casilla **Configuración guiada** antes de hacer clic en el botón **Crear**.

3. Escriba un nombre para la aplicación y seleccione **Crear**. 
    
    Para el flujo de **Configuración guiada**:
 
    a. Seleccione la opción **Aplicación de escritorio y móvil** para definir el tipo de aplicación que quiera crear.

    b. Seleccione **Android** para definir la tecnología móvil que usa.

    c. Revise el tema de introducción y, cuando termine, haga clic en el botón **Configuración** al final de la página.

    d. Siga las instrucciones en el paso **Configuración** para agregar la biblioteca de MSAL al build.gradle de la aplicación.

    e. Siga las indicaciones en el paso **Uso** para agregar la lógica de MSAL al nuevo proyecto.

    f. En la página **Configurar**, el portal creó automáticamente un id. de aplicación único. Úselo para configurar la aplicación.

    <br/>
    
    Para el flujo no guiado:

    Se muestra la página de registro con una lista de las propiedades de la aplicación.

    a. Copie el id. de aplicación. Es el identificador único de la aplicación. 

    b. Seleccione **Agregar plataforma** y **Aplicación nativa**.

      > **Nota**: El Portal de registro de aplicaciones proporciona un URI de redireccionamiento con un valor de `msalENTER_YOUR_CLIENT_ID://auth`. No use los URI de redireccionamiento integrados. El [Ejemplo de conexión para Android](https://github.com/microsoftgraph/android-java-connect-sample) implementa la biblioteca de autenticación de MSAL, que necesita el URI de redireccionamiento. Si usa una [biblioteca de terceros compatible](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-v2-libraries#compatible-client-libraries) o la biblioteca de **ADAL**, necesita usar los URI de redireccionamiento integrados.
      
      c. Agregue los permisos delegados. Necesitará **profile**, **Mail.ReadWrite**, **Mail.Send**, **Files.ReadWrite** y **User.ReadBasic.All**. 

      d. Haga clic en **Guardar**.


## <a name="authenticate-the-user-and-get-an-access-token"></a>Autenticar al usuario y obtener un token de acceso

> **Nota**: Si siguió las instrucciones en el flujo de **Configuración guiada** desde el portal de registro de aplicaciones para crear una aplicación, puede omitir estos pasos. Para obtener más información sobre la API de Graph, vea [Llamar a Microsoft Graph con el SDK de Microsoft Graph](#call-microsoft-graph-using-the-microsoft-graph-sdk).

Veamos los pasos del [Ejemplo de conexión para Android](https://github.com/microsoftgraph/android-java-connect-sample) para obtener más información sobre MSAL y el código de Microsoft Graph que agregamos.

### <a name="add-the-dependency-to-appbuildgradle"></a>Agregar la dependencia a app/build.gradle

Abra el archivo `build.gradle` en el módulo de la aplicación e incluya la dependencia siguiente:

```gradle
    compile ('com.microsoft.identity.client:msal:0.1.+') {
        exclude group: 'com.android.support', module: 'appcompat-v7'
    }
    compile 'com.android.volley:volley:1.0.0'
```

<br/>

### <a name="start-the-authentication-flow"></a>Iniciar el flujo de autenticación

1. Abra el archivo **AuthenticationManager**, busque la declaración de objeto **PublicClientApplication** y, después, agregue la instancia del método **getInstance**.

   ```java
    private static PublicClientApplication mPublicClientApplication;
    ....

    public static synchronized AuthenticationManager getInstance() {
        if (INSTANCE == null) {
            INSTANCE = new AuthenticationManager();
            if (mPublicClientApplication == null) {
                mPublicClientApplication = new PublicClientApplication(Connect.getInstance());
            }
        }
        return INSTANCE;
    }

   ```

<br/>

2. En la clase**ConnectActivity**, busque el controlador de eventos del evento de clic de **mConnectButton**. Busque el método **onClick** y revise el código relevante.
  
    El método **connect** permite registrar información de identificación personal (DCP), obtiene una instancia de la clase auxiliar de ejemplo **AuthenticationManager** y obtiene la colección de usuarios de objeto de la plataforma de MSAL. Si no hay usuarios, el nuevo usuario será dirigido al flujo de autenticación y autorización de Azure AD. De lo contrario, se obtendrá un token de autenticación en modo silencioso.

   ```java
    @Override
    public void onClick(View view) {
        ....
        connect();
    }

        private void connect() {

        if (mEnablePiiLogging) {
            Logger.getInstance().setEnablePII(true);
        } else {
            Logger.getInstance().setEnablePII(false);
        }

        AuthenticationManager mgr = AuthenticationManager.getInstance();

        List<User> users = null;

        try {
            users = mgr.getPublicClient().getUsers();

            if (users != null && users.size() == 1) {
                mUser = users.get(0);
                mgr.callAcquireTokenSilent(mUser, true, this);
            } else {
                mgr.callAcquireToken(
                        this,
                        this);
            }
        } catch (MsalClientException e) {
            Log.d(TAG, "MSAL Exception Generated while getting users: " + e.toString());

        } catch (IndexOutOfBoundsException e) {
            Log.d(TAG, "User at this position does not exist: " + e.toString());
        }
    }

   ```
   
<br/>

3. Busque el controlador de eventos que procesa la respuesta de redireccionamiento generada por Azure AD cuando el usuario cierra el cuadro de diálogo de autenticación. Este controlador está en la clase **ConnectActivity**.

   ```java
       /**
     * Handles redirect response from https://login.microsoftonline.com/common and
     * notifies the MSAL library that the user has completed the authentication
     * dialog
     * @param requestCode
     * @param resultCode
     * @param data
     */
    @Override
    protected void onActivityResult(int requestCode, int resultCode, Intent data) {
        super.onActivityResult(requestCode, resultCode, data);
        if (AuthenticationManager
                .getInstance()
                .getPublicClient() != null) {
            AuthenticationManager
                    .getInstance()
                    .getPublicClient()
                    .handleInteractiveRequestRedirect(requestCode, resultCode, data);
        }
    }

   ```  
   
   <br/>

4. Busque el método de devolución de llamada de autenticación que almacena en la memoria caché el token de autenticación usado en las llamadas API de Graph.


```java
    /* Callback used for interactive request.  If succeeds we use the access
         * token to call the Microsoft Graph. Does not check cache
         */
    private AuthenticationCallback getAuthInteractiveCallback() {
        return new AuthenticationCallback() {
            @Override
            public void onSuccess(AuthenticationResult authenticationResult) {
            /* Successfully got a token, call graph now */
                Log.d(TAG, "Successfully authenticated");
                Log.d(TAG, "ID Token: " + authenticationResult.getIdToken());

            /* Store the auth result */
                mAuthResult = authenticationResult;
                if (mActivityCallback != null)
                    mActivityCallback.onSuccess(mAuthResult);
            }

            @Override
            public void onError(MsalException exception) {
            /* Failed to acquireToken */
                Log.d(TAG, "Authentication failed: " + exception.toString());
                if (mActivityCallback != null)
                    mActivityCallback.onError(exception);
            }

            @Override
            public void onCancel() {
            /* User canceled the authentication */
                Log.d(TAG, "User cancelled login.");
            }
        };
    }

```

<br/>
   
La aplicación de ejemplo de conexión tiene el botón **Conectar** en la actividad principal. Si selecciona el botón en el primer uso, la aplicación mostrará una página de autenticación en el explorador del dispositivo. El paso siguiente es controlar el código que envía el servidor de autorización al URI de redireccionamiento y cambiarlo por un token de acceso.

### <a name="exchange-the-authorization-code-for-an-access-token"></a>Cambiar el código de autorización por un token de acceso

Es necesario que prepare la aplicación para controlar la respuesta del servidor de autorización, que contiene un código que se puede intercambiar por un token de acceso.

1. Necesita indicarle al sistema Android que la aplicación de conexión admite solicitudes a la URL de redireccionamiento configurada en el registro de la aplicación. Para hacerlo, abra el archivo de recursos de cadenas **strings.xml** y agregue los siguientes elementos secundarios al elemento **\<application/\>**de proyectos.

   ```xml
   <!DOCTYPE resources [
       <!ENTITY clientId "ENTER_YOUR_CLIENT_ID">
       ]>

    ...
    <string name="client_Id">&clientId;</string>
    <string name="msalPrefix">msal&clientId;</string>
   ```

   <br/>

   Los recursos de cadena se utilizan en el archivo **AndroidManifest.xml**. La biblioteca **MSAL** lee el id. de cliente en tiempo de ejecución y devuelve las respuestas REST a la redirección de la dirección URL definida para la **BrowserTabActivity**.

    ```xml
        <uses-sdk tools:overrideLibrary="com.microsoft.identity.msal" />
        <application ...>
            ...
           <activity
               android:name="com.microsoft.identity.client.BrowserTabActivity">
               <intent-filter>
                   <action android:name="android.intent.action.VIEW" />
                   <category android:name="android.intent.category.DEFAULT" />
                   <category android:name="android.intent.category.BROWSABLE" />
                   <data android:scheme="@string/msalPrefix"
                       android:host="auth" />
               </intent-filter>
           </activity>
           <meta-data
               android:name="https://login.microsoftonline.com/common"
               android:value="authority string"/>
           <meta-data
               android:name="com.microsoft.identity.client.ClientId"
               android:value="@string/client_Id"/>
        </application>
    ```


2. La biblioteca de **MSAL** necesita obtener acceso al id. de aplicación asignado por el portal de registro. **La biblioteca de MSAL hace referencia al id. de aplicación como “id. de cliente”**. Obtiene el id. de aplicación (id. de cliente) del contexto de la aplicación que pase en el constructor de la biblioteca. 

   > **Nota**: También puede proporcionar el id. de cliente en el tiempo de ejecución si pasa un parámetro de cadena al constructor. 

3. La actividad se invoca cuando el servidor de autorización envía una respuesta. Puede solicitar un token de acceso con la respuesta del servidor de autorización. Vaya al **AuthenticationManager** y busque el código siguiente en la clase.

   ```java
    /**
     * Authenticates the user and lets the user authorize the app for the requested permissions.
     * An authentication token is returned via the getAuthInteractiveCalback method
     * @param activity
     * @param authenticationCallback
     */
    public void connect(Activity activity, final MSALAuthenticationCallback authenticationCallback){
        mActivityCallback = authenticationCallback;
        mPublicClientApplication.acquireToken(
                activity, Constants.SCOPES, getAuthInteractiveCallback());
    }


     /* Callback used for interactive request.  If succeeds we use the access
         * token to call the Microsoft Graph. Does not check cache
         */
    private AuthenticationCallback getAuthInteractiveCallback() {
        return new AuthenticationCallback() {
            @Override
            public void onSuccess(AuthenticationResult authenticationResult) {
            /* Successfully got a token, call graph now */
                Log.d(TAG, "Successfully authenticated");
                Log.d(TAG, "ID Token: " + authenticationResult.getIdToken());

            /* Store the auth result */
                mAuthResult = authenticationResult;
                if (mActivityCallback != null)
                    mActivityCallback.onSuccess(mAuthResult);
            }

            @Override
            public void onError(MsalException exception) {
            /* Failed to acquireToken */
                Log.d(TAG, "Authentication failed: " + exception.toString());
                if (mActivityCallback != null)
                    mActivityCallback.onError(exception);
            }

            @Override
            public void onCancel() {
            /* User canceled the authentication */
                Log.d(TAG, "User cancelled login.");
            }
        };
    }

     /**
     * Returns the access token obtained in authentication
     *
     * @return mAccessToken
     */
    public String getAccessToken() throws AuthenticatorException, IOException, OperationCanceledException {
        return  mAuthResult.getAccessToken();
    }

   ```

<br/>

## <a name="call-microsoft-graph"></a>Llamar a Microsoft Graph

Puede [utilizar el SDK de Microsoft Graph](#call-microsoft-graph-using-the-microsoft-graph-sdk) o la [API de REST de Microsoft Graph](#call-microsoft-graph-using-the-microsoft-graph-rest-api) para llamar a Microsoft Graph.

### <a name="call-microsoft-graph-using-the-microsoft-graph-sdk"></a>Llame a Microsoft Graph mediante el SDK de Microsoft Graph

El [SDK de Microsoft Graph para Android](https://github.com/microsoftgraph/msgraph-sdk-android) proporciona clases que generan solicitudes y procesan los resultados de Microsoft Graph. Siga estos pasos para utilizar el SDK de Microsoft Graph.

1. Conceda permisos de Internet a la aplicación. Abra el archivo **AndroidManifest** y agregue el siguiente elemento secundario al elemento de manifiesto.
    
    ```xml
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
    ```


2. Agregue dependencias al SDK de Microsoft Graph y GSON.
   
   ```gradle
    compile 'com.microsoft.graph:msgraph-sdk-android:1.3.2'
    compile 'com.google.code.gson:gson:2.7'
   ```


3. Agregue un token de autenticación a las nuevas solicitudes con el método auxiliar **AuthenticateRequest**. Este método implementa el mismo método de la interfaz **IAuthenticationProvider** de Microsoft Graph Authentication.
    
   ```java
    /**
     * Appends an access token obtained from the {@link AuthenticationManager} class to the
     * Authorization header of the request.
     * @param request
     */
    @Override
    public void authenticateRequest(IHttpRequest request)  {
        try {
            request.addHeader("Authorization", "Bearer "
                    + AuthenticationManager.getInstance()
                    .getAccessToken());
            // This header has been added to identify this sample in the Microsoft Graph service.
            // If you're using this code for your project please remove the following line.
            request.addHeader("SampleID", "android-java-connect-sample");
        } catch (AuthenticatorException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
        }  catch (OperationCanceledException e) {
            e.printStackTrace();
        } catch (NullPointerException e) {
            e.printStackTrace();
        }
    }
   ```


4. Cree un borrador de correo electrónico y envíelo con los siguientes métodos auxiliares desde la clase auxiliar **GraphServiceController**.

   ```java
    /**
     * Creates a draft email message using the Microsoft Graph API on Office 365. The mail is sent
     * from the address of the signed in user.
     *
     * @param senderPreferredName The mail senders principal user name (email addr)
     * @param emailAddress        The recipient email address.
     * @param subject             The subject to use in the mail message.
     * @param body                The body of the message.
     * @param callback            The callback method to invoke on completion of the POST request
     */
    public void createDraftMail(
            final String senderPreferredName,
            final String emailAddress,
            final String subject,
            final String body,
            ICallback<Message> callback
    ) {
        try {
            // create the email message
            Message message = createMessage(subject, body, emailAddress);
            mGraphServiceClient
                    .getMe()
                    .getMessages()
                    .buildRequest()
                    .post(message, callback);

        } catch (Exception ex) {
            showException(ex, "exception on send mail","Send mail failed", "The send mail method failed");
        }
    }

        /**
     * Creates a new Message object 
     */
    Message createMessage(
            String subject,
            String body,
            String address) {

        if (address == null || address.isEmpty()) {
            throw new IllegalArgumentException("The address parameter can't be null or empty.");
        } else {
            // perform a simple validation of the email address
            String addressParts[] = address.split("@");
            if (addressParts.length != 2 || addressParts[0].length() == 0 || addressParts[1].indexOf('.') == -1) {
                throw new IllegalArgumentException(
                        String.format("The address parameter must be a valid email address {0}", address)
                );
            }
        }
        Message message = new Message();
        EmailAddress emailAddress = new EmailAddress();
        emailAddress.address = address;
        Recipient recipient = new Recipient();
        recipient.emailAddress = emailAddress;
        message.toRecipients = Collections.singletonList(recipient);
        ItemBody itemBody = new ItemBody();
        itemBody.content = body;
        itemBody.contentType = BodyType.html;
        message.body = itemBody;
        message.subject = subject;
        return message;
    }
    /**
     * Sends a draft message to the specified recipients
     *
     * @param messageId String. The id of the message to send
     * @param callback
     */
    public void sendDraftMessage(String messageId,
                                 ICallback<Void> callback) {
        try {

            mGraphServiceClient
                    .getMe()
                    .getMessages(messageId)
                    .getSend()
                    .buildRequest()
                    .post(callback);

        } catch (Exception ex) {
            showException(ex, "exception on send draft message ","Send draft mail failed", "The send draft mail method failed");
        }
    }

   ```
  

### <a name="call-microsoft-graph-using-the-microsoft-graph-rest-api"></a>Llamar a Microsoft Graph con la API de REST de Microsoft Graph

La [API de REST de Microsoft Graph](http://developer.microsoft.com/en-us/graph/docs) expone varias API de servicios de nube de Microsoft a través de un único punto de conexión de la API de REST. Siga estos pasos para utilizar la API de REST.

1. Conceda permisos de Internet a la aplicación. Abra el archivo **AndroidManifest** y agregue el siguiente elemento secundario al elemento de manifiesto.
    
    ```xml
    <uses-permission android:name="android.permission.INTERNET" />
    ```


2. Agregue una dependencia a la biblioteca HTTP Volley.

    ```gradle
    compile 'com.android.volley:volley:1.0.0'
    ```
   

3. Reemplace la línea `String accessToken = tokenResponse.accessToken;` por el siguiente código. Escriba su dirección de correo electrónico en el marcador de posición marcado como **\<YOUR_EMAIL_ADDRESS\>**.
   
   ```java
    final String accessToken = tokenResponse.accessToken;

    final RequestQueue queue = Volley.newRequestQueue(getApplicationContext());
    String url ="https://graph.microsoft.com/v1.0/me/sendMail";
    final String body = "{" +
        "  Message: {" +
        "    subject: 'Sent using the Microsoft Graph REST API'," +
        "    body: {" +
        "      contentType: 'text'," +
        "      content: 'This is the email body'" +
        "    }," +
        "    toRecipients: [" +
        "      {" +
        "        emailAddress: {" +
        "          address: '<YOUR_EMAIL_ADDRESS>'" +
        "        }" +
        "      }" +
        "    ]}" +
        "}";

    final StringRequest stringRequest = new StringRequest(Request.Method.POST, url,
        new Response.Listener<String>() {
            @Override
            public void onResponse(String response) {
                Log.d("Response", response);
            }
        },
        new Response.ErrorListener() {
            @Override
            public void onErrorResponse(VolleyError error) {
                Log.d("ERROR","error => " + error.getMessage());
            }
        }
    ) {
        @Override
        public Map<String, String> getHeaders() throws AuthFailureError {
            Map<String,String> params = new HashMap<>();
            params.put("Authorization", "Bearer " + accessToken);
            params.put("Content-Length", String.valueOf(body.getBytes().length));
            return params;
        }
        @Override
        public String getBodyContentType() {
            return "application/json";
        }
        @Override
        public byte[] getBody() throws AuthFailureError {
            return body.getBytes();
        }
    };

    AsyncTask.execute(new Runnable() {
        @Override
        public void run() {
            queue.add(stringRequest);
        }
    });
   ```


## <a name="run-the-app"></a>Ejecutar la aplicación
Está preparado para probar la aplicación de Android.

1. Inicie el emulador de Android o conecte el dispositivo físico a su equipo.
2. En Android Studio, presione Mayús y F10 para ejecutar la aplicación.
3. Elija el emulador de Android o el dispositivo en el cuadro de diálogo de implementación.
4. Pulse el botón **Acción flotante** en la actividad principal.
5. Inicie sesión con su cuenta personal, profesional o educativa, y conceda los permisos solicitados.
6. En el cuadro de diálogo de selección de la aplicación, pulse en la aplicación para continuar.

Compruebe la Bandeja de entrada de la dirección de correo electrónico que configuró en [Llamar a Microsoft Graph](#call-microsoft-graph). Debe tener un correo electrónico de la cuenta que usó para iniciar sesión en la aplicación.

## <a name="next-steps"></a>Siguientes pasos

- Pruebe el [Probador de Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer).
- Encuentre ejemplos de operaciones comunes en [Fragmentos de código de ejemplo para Android](https://github.com/microsoftgraph/android-java-snippets-sample) o explore nuestros otros [Ejemplos de Android](https://github.com/microsoftgraph?utf8=%E2%9C%93&query=android) en GitHub.


## <a name="see-also"></a>Recursos adicionales

- [SDK de Microsoft Graph para Android](https://github.com/microsoftgraph/msgraph-sdk-android) 
- [Obtener tokens de acceso para llamar a Microsoft Graph](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_overview)
- [Obtener acceso en nombre de un usuario](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_v2_user)
- [Obtener acceso sin un usuario](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_v2_service)
