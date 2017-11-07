# <a name="use-microsoft-graph-to-access-excel-in-a-python-app"></a><span data-ttu-id="03947-101">Usar Microsoft Graph para tener acceso a Excel en una aplicación de Python</span><span class="sxs-lookup"><span data-stu-id="03947-101">Use Microsoft Graph to access Excel in a Python app</span></span>

<span data-ttu-id="03947-102">Puede usar la API de Microsoft Graph para leer y actualizar libros almacenados en plataformas de almacenamiento en línea compatibles, incluidas OneDrive y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="03947-102">You can use the Microsoft Graph API to read and update workbooks stored in supported online storage platforms including, OneDrive and SharePoint. The  (or Excel file) resource contains all the other Excel resources and your app can access them via simple navigations.</span></span> <span data-ttu-id="03947-103">El recurso `Workbook` (o archivo de Excel) contiene todos los demás recursos de Excel y su aplicación puede acceder a ellos mediante navegaciones simples.</span><span class="sxs-lookup"><span data-stu-id="03947-103">You can use the Microsoft Graph API to read and update workbooks stored in supported online storage platforms including, OneDrive and SharePoint. The `Workbook` (or Excel file) resource contains all the other Excel resources and your app can access them via simple navigations.</span></span> 

<span data-ttu-id="03947-104">Puede obtener acceso a un conjunto de objetos de Excel (como una tabla, intervalo o gráfico) mediante las API de REST estándares para realizar operaciones de creación, lectura, actualización y eliminación (CRUD) en el libro.</span><span class="sxs-lookup"><span data-stu-id="03947-104">You can access a set of Excel objects (such as Table, Range, or Chart) by using standard REST APIs to perform  create, read, update, and delete (CRUD) operations on the workbook. For example, </span></span> <span data-ttu-id="03947-105">Por ejemplo: `https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/`</span><span class="sxs-lookup"><span data-stu-id="03947-105">For example:`https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/`</span></span>  
<span data-ttu-id="03947-106">devuelve una colección de objetos de hoja de cálculo que forman parte del libro.</span><span class="sxs-lookup"><span data-stu-id="03947-106">returns a collection of worksheet objects that are part of the workbook.</span></span>    

<span data-ttu-id="03947-107">En este tutorial, se describe cómo realizar solicitudes a la API de REST de Excel desde una aplicación web de Python.</span><span class="sxs-lookup"><span data-stu-id="03947-107">This walkthrough describes how to make requests to the Excel REST API from a Python web app.</span></span> 

##  <a name="prerequisites"></a><span data-ttu-id="03947-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03947-108">Prerequisites</span></span>

* [<span data-ttu-id="03947-109">Python 3.5.2</span><span class="sxs-lookup"><span data-stu-id="03947-109">Python 3.5.2</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="03947-110">Flask-OAuthlib</span><span class="sxs-lookup"><span data-stu-id="03947-110">Flask-OAuthlib</span></span>](https://github.com/lepture/flask-oauthlib)
* <span data-ttu-id="03947-111">Una [cuenta profesional o educativa](https://msdn.microsoft.com/en-us/office/office365/howto/setup-development-environment#bk_Office365Account)<!-- This link target doesn't match the link title. Please verify that this is what you want to link to and update the text, or update the URL as appropriate. --></span><span class="sxs-lookup"><span data-stu-id="03947-111">A [work or school account](https://msdn.microsoft.com/en-us/office/office365/howto/setup-development-environment#bk_Office365Account)<!-- This link target doesn't match the link title. Please verify that this is what you want to link to and update the text, or update the URL as appropriate. --></span></span>


## <a name="authorization-and-scopes"></a><span data-ttu-id="03947-112">Autorización y ámbitos</span><span class="sxs-lookup"><span data-stu-id="03947-112">Authorization and scopes</span></span>
<span data-ttu-id="03947-113">Puede usar el [punto de conexión de Azure AD v2.0](https://graph.microsoft.io/en-us/docs/concepts/converged_auth) para autenticar las llamadas a la API de REST de Excel.</span><span class="sxs-lookup"><span data-stu-id="03947-113">You can use the [Azure AD v2.0 endpoint](https://graph.microsoft.io/en-us/docs/concepts/converged_auth) to authenticate Excel REST API calls. All APIs require the  HTTP header.</span></span> <span data-ttu-id="03947-114">Todas las API requieren el encabezado HTTP `Authorization: Bearer {access-token}`.</span><span class="sxs-lookup"><span data-stu-id="03947-114">All APIs require the `Authorization: Bearer {access-token}` HTTP header.</span></span>   
  
<span data-ttu-id="03947-115">Uno de los siguientes [ámbitos de permiso](https://graph.microsoft.io/en-us/docs/concepts/permissions_reference) es necesario para usar el recurso de Excel:</span><span class="sxs-lookup"><span data-stu-id="03947-115">One of the following [permission scopes](https://graph.microsoft.io/en-us/docs/concepts/permissions_reference) is required to use the Excel resource:</span></span>

* <span data-ttu-id="03947-116">Files.Read</span><span class="sxs-lookup"><span data-stu-id="03947-116">Files.Read</span></span> 
* <span data-ttu-id="03947-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03947-117">Files.ReadWrite</span></span>

## <a name="sessions-and-persistence"></a><span data-ttu-id="03947-118">Sesiones y persistencia</span><span class="sxs-lookup"><span data-stu-id="03947-118">Sessions and persistence</span></span>

<span data-ttu-id="03947-119">Se puede llamar a las API de Excel de dos modos:</span><span class="sxs-lookup"><span data-stu-id="03947-119">Excel APIs can be called in one of two modes:</span></span> 

1. <span data-ttu-id="03947-p104">Sesión persistente - Todos los cambios realizados en el libro son persistentes (se guardan). Este es el modo de operación habitual.</span><span class="sxs-lookup"><span data-stu-id="03947-p104">Persistent session - All changes made to the workbook are persisted (saved). This is the usual mode of operation.</span></span> 
2. <span data-ttu-id="03947-p105">Sesión no persistente - Los cambios realizados por la API no se guardan en la ubicación de origen. En su lugar, el servidor backend de Excel conserva una copia temporal del archivo que refleja los cambios realizados durante esa sesión API en concreto. Cuando expira la sesión de Excel, se pierden los cambios. Este modo es útil para aplicaciones que necesitan realizar análisis u obtener los resultados de un cálculo o una imagen de gráfico, pero no afecta al estado de documento.</span><span class="sxs-lookup"><span data-stu-id="03947-p105">Non-persistent session - Changes made by the API are not saved to the source location. Instead, the Excel backend server keeps a temporary copy of the file that reflects the changes made during that particular API session. When the Excel session expires, the changes are lost. This mode is useful for apps that need to do analysis or obtain the results of a calculation or a chart image, but not affect the document state.</span></span>   

<span data-ttu-id="03947-126">Para representar la sesión en la API, use el encabezado `workbook-session-id: {session-id}`.</span><span class="sxs-lookup"><span data-stu-id="03947-126">To represent the session in the API, use the `workbook-session-id: {session-id}` header.</span></span> 

## <a name="register-the-application-in-azure-active-directory"></a><span data-ttu-id="03947-127">Registrar la aplicación en Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="03947-127">Register the application in Azure Active Directory</span></span>

<span data-ttu-id="03947-p106">En primer lugar, deberá registrar la aplicación y establecer los permisos para usar Microsoft Graph. Esto permite a los usuarios iniciar sesión en la aplicación con cuentas profesionales o educativas.</span><span class="sxs-lookup"><span data-stu-id="03947-p106">First, you need to register your application and set permissions to use Microsoft Graph. This lets users sign in to the application with work or school accounts.</span></span>

### <a name="register-the-application"></a><span data-ttu-id="03947-130">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="03947-130">Register the application</span></span>

<span data-ttu-id="03947-p107">Registre una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el ID y la contraseña de aplicación que usará para configurar la aplicación para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="03947-p107">Register an app on the Microsoft App Registration Portal. This generates the app ID and password that you'll use to configure the app for authentication.</span></span>

1. <span data-ttu-id="03947-133">Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="03947-133">Sign in to the [Microsoft App Registration Portal](https://apps.dev.microsoft.com/) using either your personal or work or school account.</span></span>

2. <span data-ttu-id="03947-134">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="03947-134">Choose **Add an app**.</span></span>

3. <span data-ttu-id="03947-135">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="03947-135">Enter a name for the app, and choose **Create application**.</span></span>

    <span data-ttu-id="03947-136">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="03947-136">The registration page displays, listing the properties of your app.</span></span>

4. <span data-ttu-id="03947-p108">Copie el identificador de la aplicación. Se trata del identificador único para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="03947-p108">Copy the application ID. This is the unique identifier for your app.</span></span>

5. <span data-ttu-id="03947-p109">En **Secretos de aplicación**, elija **Generar nueva contraseña**. Copie el secreto de aplicación del cuadro de diálogo **Nueva contraseña generada**.</span><span class="sxs-lookup"><span data-stu-id="03947-p109">Under **Application Secrets**, choose **Generate New Password**. Copy the app secret from the **New password generated** dialog box.</span></span>

    <span data-ttu-id="03947-141">Deberá usar el ID y el secreto de aplicación para configurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="03947-141">You'll use the application ID and app secret to configure the app.</span></span>

6. <span data-ttu-id="03947-142">En **Plataformas**, elija **Agregar plataforma** > **Web**.</span><span class="sxs-lookup"><span data-stu-id="03947-142">Under **Platforms**, choose **Add platform** > **Web**.</span></span>

7. <span data-ttu-id="03947-143">Asegúrese de que la casilla **Permitir flujo implícito** esté seleccionada y escriba el URI de redireccionamiento de su aplicación.</span><span class="sxs-lookup"><span data-stu-id="03947-143">Make sure the **Allow Implicit Flow** check box is selected, and enter your app's Redirect URI.</span></span>

    <span data-ttu-id="03947-144">La opción **Permitir flujo implícito** habilita el flujo híbrido de OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="03947-144">The **Allow Implicit Flow** option enables the OpenID Connect hybrid flow.</span></span> <span data-ttu-id="03947-145">Durante la autenticación, esto permite que la aplicación reciba tanto la información de inicio de sesión (el **id_token**) como los artefactos (en este caso, un código de autorización) que la aplicación usa para obtener un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="03947-145">During authentication, this enables the app to receive both sign-in info (the id_token) and artifacts (in this case, an authorization code) that the app can use to obtain an access token.</span></span>

8. <span data-ttu-id="03947-146">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="03947-146">Choose **Save**.</span></span>

### <a name="create-oauth-client"></a><span data-ttu-id="03947-147">Crear el cliente de OAuth</span><span class="sxs-lookup"><span data-stu-id="03947-147">Create OAuth client</span></span>

<span data-ttu-id="03947-148">La aplicación debe registrar una instancia del cliente de Flask OAuth que usará para iniciar el flujo de OAuth y obtener un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="03947-148">Your app needs to register an instance of the Flask-OAuth client that you'll use to start the OAuth flow and get an access token.</span></span> <span data-ttu-id="03947-149">Tenga en cuenta que el ámbito *Files.ReadWrite* es necesario para obtener una sesión de Excel que admita cambios persistentes.</span><span class="sxs-lookup"><span data-stu-id="03947-149">Note that the *Files.ReadWrite* scope is required to obtain an Excel session that supports persisted changes.</span></span>

```python
    # Put your consumer key and consumer secret into a config file
    # and don't check it into github!
    microsoft = oauth.remote_app(
        'microsoft',
        consumer_key = client_id,
        consumer_secret = client_secret,
        request_token_params = {'scope': 'User.Read Files.ReadWrite'},
        base_url = 'https://graph.microsoft.com/v1.0/',
        request_token_url = None,
        access_token_method = 'POST',
        access_token_url = 'https://login.microsoftonline.com/common/oauth2/v2.0/token',
        authorize_url = 'https://login.microsoftonline.com/common/oauth2/v2.0/authorize'
    )
```

### <a name="receive-an-authorization-code-in-your-reply-url-page"></a><span data-ttu-id="03947-150">Recibir un código de autorización en la página de la dirección URL de respuesta</span><span class="sxs-lookup"><span data-stu-id="03947-150">Receive an authorization code in your reply URL page</span></span>

<span data-ttu-id="03947-p112">Una vez que el usuario inicia sesión, el explorador se redirige a la dirección URL de respuesta. Tras la autorización correcta, se devolverá el token de acceso (que se usará para autorizar las solicitudes adicionales) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03947-p112">After the user signs in, the browser is redirected to your reply URL. Upon successful authorization, the access token (which will be used to authorize additional requests) will be returned in the response body.</span></span> 

```python
    @app.route('/login/authorized')
    def authorized():
        response = microsoft.authorized_response()
        if response is None:
            return "Access Denied: Reason=%s\nError=%s" % (
                request.args['error'], 
                request.args['error_description']
            )
    
        # Check response for state
        if str(session['state']) != str(request.args['state']):
            raise Exception('State has been messed with, end authentication')
        # Remove state session variable to prevent reuse.
        session['state'] = ""
            
        # Okay to store this in a local variable, encrypt if it's going to client
        # machine or database. Treat as a password. 
        session['microsoft_token'] = (response['access_token'], '')
        # Store the token in another session variable for easy access
        session['access_token'] = response['access_token']
```

## <a name="make-requests-to-the-excel-api"></a><span data-ttu-id="03947-153">Realizar solicitudes a la API de Excel</span><span class="sxs-lookup"><span data-stu-id="03947-153">Make requests to the Excel API</span></span>

### <a name="request-headers"></a><span data-ttu-id="03947-154">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03947-154">Request headers</span></span> 
<span data-ttu-id="03947-p113">El token de acceso permite que su aplicación cree solicitudes autenticadas en la API de Microsoft Graph. Su aplicación debe anexar el token de acceso al encabezado de **autorización** de cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="03947-p113">With an access token, your app can make authenticated requests to the Microsoft Graph API. Your app must append the access token to the **Authorization** header of each request.</span></span>

```python
    # Set request headers.
    headers = { 
        'User-Agent' : 'python_tutorial/1.0',
        'Authorization' : 'Bearer {0}'.format(access_token),
        'Accept' : 'application/json',
        'Content-Type' : 'application/json'
    }
```
> <span data-ttu-id="03947-157">**Nota**: La solicitud también debe enviar un encabezado **Content-Type** con un valor que acepte la API de Graph. Por ejemplo, `application/json`.</span><span class="sxs-lookup"><span data-stu-id="03947-157">**Note** The request must also send a **Content-Type** header with a value accepted by the Graph API, for example, `application/json`.</span></span>

### <a name="getting-an-excel-session"></a><span data-ttu-id="03947-158">Obtención de una sesión de Excel</span><span class="sxs-lookup"><span data-stu-id="03947-158">Getting an Excel Session</span></span>
#### <a name="request"></a><span data-ttu-id="03947-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03947-159">Request</span></span> 

<span data-ttu-id="03947-160">Transmita un objeto JSON al establecer el valor `persistChanges` en `true` o `false`.</span><span class="sxs-lookup"><span data-stu-id="03947-160">Pass a JSON object by setting the `persistChanges` value to `true` or `false`.</span></span> <span data-ttu-id="03947-161">Cuando el valor de `persistChanges` se establece en `false`, se devuelve un identificador de sesión no persistente.</span><span class="sxs-lookup"><span data-stu-id="03947-161">When the value of `persistChanges` is set to `false`, a non-persistent session id is returned.</span></span> <span data-ttu-id="03947-162">En este ejemplo, se usa la biblioteca HTTP [Requests](http://docs.python-requests.org/en/latest/user/quickstart)</span><span class="sxs-lookup"><span data-stu-id="03947-162">This example uses the [Requests](http://docs.python-requests.org/en/latest/user/quickstart) HTTP library</span></span> 

```python
    # Replace the id with your Excel workbook's drive id
    url = 'https://graph.microsoft.com/v1.0/me/drive/items/01TBZDUE23F3CNYSIEGNBZV2LZGWHMC7TE/workbook/createSession'
    # Set request headers
    headers = { 
        'User-Agent' : 'python_tutorial/1.0',
        'Authorization' : 'Bearer {0}'.format(access_token),
        'Accept' : 'application/json',
        'Content-Type' : 'application/json'
    }
    # Specify type of session
    body = {
        'persistChanges': True
    }
    
    response = requests.post(url, headers = headers, json = body)
```

#### <a name="response"></a><span data-ttu-id="03947-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03947-163">Response</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 201 Created
content-type: application/json;odata.metadata 

{
    "@odata.context": "https://graph.microsoft.com/{version}/$metadata#microsoft.graph.sessionInfo",
    "id": "{session-id}",
    "persistChanges": true
}
```

#### <a name="usage"></a><span data-ttu-id="03947-164">Uso</span><span class="sxs-lookup"><span data-stu-id="03947-164">Usage</span></span> 

<span data-ttu-id="03947-165">El identificador de sesión devuelto de la llamada anterior se pasa como un encabezado en las subsiguientes solicitudes API en el encabezado HTTP **Workbook-Session-Id**.</span><span class="sxs-lookup"><span data-stu-id="03947-165">The session ID returned from the previous call is passed as a header on subsequent API requests in the **Workbook-Session-Id** HTTP header. For instance, to list worksheets in that Excel workbook.</span></span> <span data-ttu-id="03947-166">Por ejemplo, para enumerar hojas de cálculo de ese libro de Excel.</span><span class="sxs-lookup"><span data-stu-id="03947-166">For instance, to list worksheets in that Excel workbook.</span></span>

```python
    # Replace the id with your Excel workbook's drive id
    url = 'https://graph.microsoft.com/v1.0/me/drive/items/01TBZDUE23F3CNYSIEGNBZV2LZGWHMC7TE/workbook/worksheets'
    # Set request headers - note the session header 
    headers = { 
        'User-Agent' : 'python_tutorial/1.0',
        'Authorization' : 'Bearer {0}'.format(access_token),
        'Accept' : 'application/json',
        'Workbook-Session-Id': 'cluster=PP1&session=12.a04039942e021.A272...'
    }
    
    response = requests.get(url, headers = headers)
```

#### <a name="response"></a><span data-ttu-id="03947-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03947-167">Response</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('8473b867-3e4e-4e44-8d09-8c6da362080f')/drive/items('01TBZDUE23F3CNYSIEGNBZV2LZGWHMC7TE')/workbook/worksheets",
    "value": [
    {
        "@odata.id": "/users('8473b867-3e4e-4e44-8d09-8c6da362080f')/drive/items('01TBZDUE23F3CNYSIEGNBZV2LZGWHMC7TE')/workbook/worksheets(%27%7B00000000-0001-0000-0000-000000000000%7D%27)",
        "id": "{00000000-0001-0000-0000-000000000000}",
        "name": "Session 1",
        "position": 0,
        "visibility": "Visible"
    },
    {
        "@odata.id": "/users('8473b867-3e4e-4e44-8d09-8c6da362080f')/drive/items('01TBZDUE23F3CNYSIEGNBZV2LZGWHMC7TE')/workbook/worksheets(%27%7B00000000-0001-0000-0100-000000000000%7D%27)",
        "id": "{00000000-0001-0000-0100-000000000000}",
        "name": "Session 2",
        "position": 1,
        "visibility": "Visible"
    }]
}
```

## <a name="next-steps"></a><span data-ttu-id="03947-168">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="03947-168">Next steps</span></span>

<span data-ttu-id="03947-169">Con el encabezado HTTP **Workbook-Session-Id**, puede empezar a emitir solicitudes para capturar datos, crear gráficos, etc.</span><span class="sxs-lookup"><span data-stu-id="03947-169">With the **Workbook-Session-Id** HTTP header, you can begin issuing requests to fetch data, create charts, and much more.</span></span> 

* [<span data-ttu-id="03947-170">Escenarios comunes de la API de Excel</span><span class="sxs-lookup"><span data-stu-id="03947-170">Common Excel API scenarios</span></span>](https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/excel#common-excel-scenarios)
* [<span data-ttu-id="03947-171">Trabajar con Excel en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="03947-171">Working with Excel in Microsoft Graph</span></span>](https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/excel)

<span data-ttu-id="03947-p116">La API de REST de Excel en Microsoft Graph proporciona una forma eficaz de obtener acceso a los datos e interactuar con ellos en libros de Excel. Explore qué más puede hacer con Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="03947-p116">The Excel REST API in Microsoft Graph provides a powerful way to access and interact with data in Excel workbooks. Explore what else is possible with Microsoft Graph.</span></span>

* [<span data-ttu-id="03947-174">Información general de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="03947-174">Overview of Microsoft Graph</span></span>](https://developer.microsoft.com/graph/docs)
* [<span data-ttu-id="03947-175">Introducción a Microsoft Graph en una aplicación de Python</span><span class="sxs-lookup"><span data-stu-id="03947-175">Get started with Microsoft Graph in a Python app</span></span>](https://developer.microsoft.com/graph/docs/get-started/python)
