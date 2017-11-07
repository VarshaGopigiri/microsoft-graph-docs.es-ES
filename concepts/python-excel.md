# <a name="use-microsoft-graph-to-access-excel-in-a-python-app"></a>Usar Microsoft Graph para tener acceso a Excel en una aplicación de Python

Puede usar la API de Microsoft Graph para leer y actualizar libros almacenados en plataformas de almacenamiento en línea compatibles, incluidas OneDrive y SharePoint. El recurso `Workbook` (o archivo de Excel) contiene todos los demás recursos de Excel y su aplicación puede acceder a ellos mediante navegaciones simples. 

Puede obtener acceso a un conjunto de objetos de Excel (como una tabla, intervalo o gráfico) mediante las API de REST estándares para realizar operaciones de creación, lectura, actualización y eliminación (CRUD) en el libro. Por ejemplo: `https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/`  
devuelve una colección de objetos de hoja de cálculo que forman parte del libro.    

En este tutorial, se describe cómo realizar solicitudes a la API de REST de Excel desde una aplicación web de Python. 

##  <a name="prerequisites"></a>Requisitos previos

* [Python 3.5.2](https://www.python.org/downloads/)
* [Flask-OAuthlib](https://github.com/lepture/flask-oauthlib)
* Una [cuenta profesional o educativa](https://msdn.microsoft.com/en-us/office/office365/howto/setup-development-environment#bk_Office365Account)<!-- This link target doesn't match the link title. Please verify that this is what you want to link to and update the text, or update the URL as appropriate. -->


## <a name="authorization-and-scopes"></a>Autorización y ámbitos
Puede usar el [punto de conexión de Azure AD v2.0](https://graph.microsoft.io/en-us/docs/concepts/converged_auth) para autenticar las llamadas a la API de REST de Excel. Todas las API requieren el encabezado HTTP `Authorization: Bearer {access-token}`.   
  
Uno de los siguientes [ámbitos de permiso](https://graph.microsoft.io/en-us/docs/concepts/permissions_reference) es necesario para usar el recurso de Excel:

* Files.Read 
* Files.ReadWrite

## <a name="sessions-and-persistence"></a>Sesiones y persistencia

Se puede llamar a las API de Excel de dos modos: 

1. Sesión persistente - Todos los cambios realizados en el libro son persistentes (se guardan). Este es el modo de operación habitual. 
2. Sesión no persistente - Los cambios realizados por la API no se guardan en la ubicación de origen. En su lugar, el servidor backend de Excel conserva una copia temporal del archivo que refleja los cambios realizados durante esa sesión API en concreto. Cuando expira la sesión de Excel, se pierden los cambios. Este modo es útil para aplicaciones que necesitan realizar análisis u obtener los resultados de un cálculo o una imagen de gráfico, pero no afecta al estado de documento.   

Para representar la sesión en la API, use el encabezado `workbook-session-id: {session-id}`. 

## <a name="register-the-application-in-azure-active-directory"></a>Registrar la aplicación en Azure Active Directory

En primer lugar, deberá registrar la aplicación y establecer los permisos para usar Microsoft Graph. Esto permite a los usuarios iniciar sesión en la aplicación con cuentas profesionales o educativas.

### <a name="register-the-application"></a>Registrar la aplicación

Registre una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el ID y la contraseña de aplicación que usará para configurar la aplicación para la autenticación.

1. Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.

2. Seleccione **Agregar una aplicación**.

3. Escriba un nombre para la aplicación y seleccione **Crear aplicación**.

    Se muestra la página de registro, indicando las propiedades de la aplicación.

4. Copie el identificador de la aplicación. Se trata del identificador único para su aplicación.

5. En **Secretos de aplicación**, elija **Generar nueva contraseña**. Copie el secreto de aplicación del cuadro de diálogo **Nueva contraseña generada**.

    Deberá usar el ID y el secreto de aplicación para configurar la aplicación.

6. En **Plataformas**, elija **Agregar plataforma** > **Web**.

7. Asegúrese de que la casilla **Permitir flujo implícito** esté seleccionada y escriba el URI de redireccionamiento de su aplicación.

    La opción **Permitir flujo implícito** habilita el flujo híbrido de OpenID Connect. Durante la autenticación, esto permite que la aplicación reciba tanto la información de inicio de sesión (el **id_token**) como los artefactos (en este caso, un código de autorización) que la aplicación usa para obtener un token de acceso.

8. Seleccione **Guardar**.

### <a name="create-oauth-client"></a>Crear el cliente de OAuth

La aplicación debe registrar una instancia del cliente de Flask OAuth que usará para iniciar el flujo de OAuth y obtener un token de acceso. Tenga en cuenta que el ámbito *Files.ReadWrite* es necesario para obtener una sesión de Excel que admita cambios persistentes.

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

### <a name="receive-an-authorization-code-in-your-reply-url-page"></a>Recibir un código de autorización en la página de la dirección URL de respuesta

Una vez que el usuario inicia sesión, el explorador se redirige a la dirección URL de respuesta. Tras la autorización correcta, se devolverá el token de acceso (que se usará para autorizar las solicitudes adicionales) en el cuerpo de la respuesta. 

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

## <a name="make-requests-to-the-excel-api"></a>Realizar solicitudes a la API de Excel

### <a name="request-headers"></a>Encabezados de solicitud 
El token de acceso permite que su aplicación cree solicitudes autenticadas en la API de Microsoft Graph. Su aplicación debe anexar el token de acceso al encabezado de **autorización** de cada solicitud.

```python
    # Set request headers.
    headers = { 
        'User-Agent' : 'python_tutorial/1.0',
        'Authorization' : 'Bearer {0}'.format(access_token),
        'Accept' : 'application/json',
        'Content-Type' : 'application/json'
    }
```
> **Nota**: La solicitud también debe enviar un encabezado **Content-Type** con un valor que acepte la API de Graph. Por ejemplo, `application/json`.

### <a name="getting-an-excel-session"></a>Obtención de una sesión de Excel
#### <a name="request"></a>Solicitud 

Transmita un objeto JSON al establecer el valor `persistChanges` en `true` o `false`. Cuando el valor de `persistChanges` se establece en `false`, se devuelve un identificador de sesión no persistente. En este ejemplo, se usa la biblioteca HTTP [Requests](http://docs.python-requests.org/en/latest/user/quickstart) 

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

#### <a name="response"></a>Respuesta

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

#### <a name="usage"></a>Uso 

El identificador de sesión devuelto de la llamada anterior se pasa como un encabezado en las subsiguientes solicitudes API en el encabezado HTTP **Workbook-Session-Id**. Por ejemplo, para enumerar hojas de cálculo de ese libro de Excel.

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

#### <a name="response"></a>Respuesta

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

## <a name="next-steps"></a>Pasos siguientes

Con el encabezado HTTP **Workbook-Session-Id**, puede empezar a emitir solicitudes para capturar datos, crear gráficos, etc. 

* [Escenarios comunes de la API de Excel](https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/excel#common-excel-scenarios)
* [Trabajar con Excel en Microsoft Graph](https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/excel)

La API de REST de Excel en Microsoft Graph proporciona una forma eficaz de obtener acceso a los datos e interactuar con ellos en libros de Excel. Explore qué más puede hacer con Microsoft Graph.

* [Información general de Microsoft Graph](https://developer.microsoft.com/graph/docs)
* [Introducción a Microsoft Graph en una aplicación de Python](https://developer.microsoft.com/graph/docs/get-started/python)
