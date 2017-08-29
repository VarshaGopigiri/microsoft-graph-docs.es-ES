# <a name="get-started-with-microsoft-graph-and-rest"></a><span data-ttu-id="0c47e-101">Introducción a Microsoft Graph y REST</span><span class="sxs-lookup"><span data-stu-id="0c47e-101">Get started with Microsoft Graph and REST</span></span>

<span data-ttu-id="0c47e-p101">En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión v2.0 de Azure AD y llamar a Microsoft Graph mediante llamadas de REST. Describe la secuencia de solicitudes y respuestas que una aplicación usa para autenticar y recuperar mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p101">This article describes the tasks required to get an access token from the Azure AD v2.0 endpoint and call Microsoft Graph using REST calls. It describes the sequence of requests and responses that an app uses to authenticate and retrieve email messages.</span></span>

<span data-ttu-id="0c47e-104">En primer lugar, necesitará registrar la aplicación con Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="0c47e-104">First, you need register your app with Azure Active Directory (Azure AD).</span></span> 

## <a name="register-the-application"></a><span data-ttu-id="0c47e-105">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="0c47e-105">Register the application</span></span>

<span data-ttu-id="0c47e-106">Actualmente, hay dos opciones para registrar su aplicación con Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0c47e-106">There are currently two options to register your app with Azure AD.</span></span>

  - <span data-ttu-id="0c47e-107">Registre una aplicación para usar el punto de conexión v2.0 de Azure AD que funcione tanto con identidades personales (Microsoft) como con cuentas profesionales y educativas (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="0c47e-107">Register an app to use the Azure AD v2.0 endpoint that works for both personal (Microsoft) identities and work and school (Azure AD) accounts.</span></span>
  - <span data-ttu-id="0c47e-108">Registre una aplicación para usar el punto de conexión de Azure AD que admita solo cuentas profesionales y educativas.</span><span class="sxs-lookup"><span data-stu-id="0c47e-108">Register an app to use the Azure AD endpoint that supports work and school accounts only.</span></span>

<span data-ttu-id="0c47e-p102">Si está leyendo este artículo, se supone que ya ha realizado el registro de v2.0, así que deberá registrar su aplicación en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com/). Siga las instrucciones de [Registrar su aplicación de Microsoft Graph con el punto de conexión v2.0 de Azure AD](../concepts/auth_register_app_v2.md) para registrar su aplicación. Para obtener información acerca de cómo usar el punto de conexión de Azure AD, consulte [Realizar la autenticación mediante Azure AD](../concepts/auth_v2_user.md).</span><span class="sxs-lookup"><span data-stu-id="0c47e-p102">This article assumes a v2.0 registration, so you'll register your app on the [Application Registration Portal](https://apps.dev.microsoft.com/). Follow the instructions in [Register your Microsoft Graph application with the Azure AD v2.0 endpoint](../concepts/auth_register_app_v2.md) to register your app. For information about using the Azure AD endpoint, see [Authenticate using Azure AD](../concepts/auth_v2_user.md).</span></span>

> <span data-ttu-id="0c47e-p103">Existen algunas limitaciones en el uso del punto de conexión v2.0. Para decidir si es o no la opción que más le conviene, consulte [¿Debería usar el punto de conexión v2.0?](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-limitations/)</span><span class="sxs-lookup"><span data-stu-id="0c47e-p103">Some limitations apply when using the v2.0 endpoint. To decide if it's right for you, see [Should I use the v2.0 endpoint?](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-limitations/)</span></span>

## <a name="authenticate-the-user-and-get-an-access-token"></a><span data-ttu-id="0c47e-114">Autenticar al usuario y obtener un token de acceso</span><span class="sxs-lookup"><span data-stu-id="0c47e-114">Authenticate the user and get an access token</span></span>

<span data-ttu-id="0c47e-p104">La aplicación que se describe en este artículo implementa el [flujo de concesión del código de autorización](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols-oauth-code/) para obtener los tokens de acceso desde el punto de conexión v2.0 de Azure AD, siguiendo los [protocolos de OAuth 2.0 estándares](http://tools.ietf.org/html/rfc6749). Para obtener una guía completa de los flujos que se admiten en el punto de conexión v2.0 de Azure AD, consulte [Tipos de punto de conexión v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-flows/).</span><span class="sxs-lookup"><span data-stu-id="0c47e-p104">The app described in this article implements the [Authorization Code Grant flow](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols-oauth-code/) to get access tokens from the Azure AD v2.0 endpoint, following standard [OAuth 2.0 protocols](http://tools.ietf.org/html/rfc6749). For a complete guide to the flows supported in the Azure AD v2.0 endpoint see [Types of the v2.0 endpoint](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-flows/).</span></span>

<span data-ttu-id="0c47e-117">Con el flujo de concesión del código de autorización, primero obtiene un código de autorización y, a continuación, lo intercambia por un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="0c47e-117">With the Authorization Code Grant flow, first you get an authorization code and then you exchange the code for an access token.</span></span>

### <a name="getting-an-authorization-code"></a><span data-ttu-id="0c47e-118">Obtener un código de autorización</span><span class="sxs-lookup"><span data-stu-id="0c47e-118">Getting an authorization code</span></span>

<span data-ttu-id="0c47e-p105">El primer paso en el flujo de concesión del código de autorización es obtener un código de autorización. El código se devuelve a la aplicación mediante el servidor de autorización cuando el usuario inicia sesión y da su consentimiento a los permisos que solicita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p105">The first step in the Authorization Code Grant flow is to get an authorization code. The code is returned to the app by the authorization server when the user signs in and consents to the permissions requested by the app.</span></span>

<span data-ttu-id="0c47e-p106">Para solicitar un código de autorización, deberá enviar una solicitud GET al punto de conexión v2.0 de Azure AD. Esta URL debe estar abierta en un explorador para que el usuario pueda iniciar sesión y proporcionar su consentimiento.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p106">You request an authorization code by sending a GET request to the Azure AD v2.0 endpoint. This URL must be opened in a browser so that the user can sign in and provide consent.</span></span>

#### <a name="construct-the-request"></a><span data-ttu-id="0c47e-123">Crear la solicitud</span><span class="sxs-lookup"><span data-stu-id="0c47e-123">Construct the request</span></span>

<span data-ttu-id="0c47e-124">1 - Empiece con la URL base:</span><span class="sxs-lookup"><span data-stu-id="0c47e-124">1- Start with the base URL:</span></span>

```
https://login.microsoftonline.com/{tenant}/oauth2/v2.0/authorize
```

<span data-ttu-id="0c47e-p107">El segmento de *inquilino* en la ruta de acceso controla quién puede iniciar sesión en la aplicación. Los valores permitidos son los siguientes: *comunes*, *organizaciones*, *consumidores* e identificadores de inquilino. Para obtener más información, consulte [Puntos de conexión de protocolo](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/#endpoints).</span><span class="sxs-lookup"><span data-stu-id="0c47e-p107">The *tenant* segment in the path controls who can sign into the application. Allowed values are *common*, *organizations*, *consumers*, and tenant identifiers. For more information, see [Protocol endpoints](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/#endpoints).</span></span>

<span data-ttu-id="0c47e-p108">2 - Anexe los parámetros de consulta a la URL base. Estos se usan para identificar la aplicación, los permisos solicitados y el resto de la información de la solicitud de autenticación. En la siguiente tabla, se describen algunos parámetros comunes:</span><span class="sxs-lookup"><span data-stu-id="0c47e-p108">2- Append query parameters to the base URL. These are used to identify the app, the requested permissions, and other auth request information. The following table describes some common parameters.</span></span>

| <span data-ttu-id="0c47e-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0c47e-131">Parameter</span></span> | <span data-ttu-id="0c47e-132">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0c47e-132">Descriptions</span></span> |
|:------|:------|
| <span data-ttu-id="0c47e-133">client_id</span><span class="sxs-lookup"><span data-stu-id="0c47e-133">client_id</span></span> | <span data-ttu-id="0c47e-p109">El identificador de la aplicación que se genera al registrar la aplicación. Esto permite que Azure AD conozca qué aplicación está solicitando el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p109">The app ID generated by registering the app. This lets Azure AD know which app is requesting the logon.</span></span> |
| <span data-ttu-id="0c47e-136">redirect_uri</span><span class="sxs-lookup"><span data-stu-id="0c47e-136">redirect_uri</span></span> | <span data-ttu-id="0c47e-p110">La ubicación a la que Azure redirigirá cuando el usuario haya dado su consentimiento a la aplicación. Este valor debe corresponder al valor del **URI de redireccionamiento** que se usó al registrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p110">The location that Azure will redirect to after the user has granted consent to the app. This value must correspond to the value of **Redirect URI** used when registering the app.</span></span> |
| <span data-ttu-id="0c47e-139">response_type</span><span class="sxs-lookup"><span data-stu-id="0c47e-139">response_type</span></span> | <span data-ttu-id="0c47e-p111">El tipo de respuesta que espera la aplicación. Este valor es `code` para el flujo de concesión del código de autorización.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p111">The type of response the app is expecting. This value is `code` for the Authorization Code Grant flow.</span></span> |
| <span data-ttu-id="0c47e-142">ámbito</span><span class="sxs-lookup"><span data-stu-id="0c47e-142">scope</span></span> | <span data-ttu-id="0c47e-p112">Una lista de los ámbitos de permisos de [Microsoft Graph](./permissions_reference.md) que está solicitando la aplicación separados por espacios. También puede especificar [ámbitos de OpenId Connect](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-scopes/#openid-connect-scopes) para el [inicio de sesión único](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols-oidc/). </span><span class="sxs-lookup"><span data-stu-id="0c47e-p112">A space-separated list of [Microsoft Graph permission scopes](./permissions_reference.md) that the app is requesting. You can also specify [OpenId Connect scopes](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-scopes/#openid-connect-scopes) for [single sign-on](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols-oidc/).</span></span>  |
| <span data-ttu-id="0c47e-145">estado</span><span class="sxs-lookup"><span data-stu-id="0c47e-145">state</span></span> | <span data-ttu-id="0c47e-146">Valor que se incluye en la solicitud, que también se devolverá en la respuesta del token y que se usa para la validación.</span><span class="sxs-lookup"><span data-stu-id="0c47e-146">A value included in the request that will also be returned in the token response, used for validation.</span></span> |

<span data-ttu-id="0c47e-147">Por ejemplo, la URL de solicitud de una aplicación que requiriera acceso de lectura al correo sería similar a la que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="0c47e-147">For example, the request URL for an application that requires read access to mail might look like the following.</span></span>

```
GET https://login.microsoftonline.com/common/oauth2/v2.0/authorize?client_id=<app ID>&redirect_uri=http%3A%2F%2Flocalhost/myapp%2F&response_type=code&state=1234&scope=mail.read
```

<span data-ttu-id="0c47e-p113">3- Redirija al usuario a la URL de inicio de sesión. Se le presentará al usuario una pantalla de inicio de sesión que mostrará el nombre de la aplicación. Después de que inicie sesión, al usuario se le presentará una lista de los permisos que requiere la aplicación y se le solicitará que los permita o que los deniegue. Si el usuario da su consentimiento, el explorador le redirigirá al URI de redireccionamiento con el código de autorización y el estado en la cadena de consulta, tal y como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p113">3- Redirect the user to the logon URL. The user is presented with a sign in screen that displays the name of the app. After signing in, the user is presented with the list of the permissions the app requires and prompted to allow or deny. If the user consents, the browser redirects to the redirect URI with the authorization code and state in the query string, as shown in the following example.</span></span>

```
http://localhost/myapp/?code=AwABAAAA...cZZ6IgAA&state=1234
```

<span data-ttu-id="0c47e-152">El paso siguiente consiste en intercambiar el código de autorización devuelto por un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="0c47e-152">The next step is to exchange the authorization code returned for an access token.</span></span>

### <a name="getting-an-access-token"></a><span data-ttu-id="0c47e-153">Obtener un token de acceso</span><span class="sxs-lookup"><span data-stu-id="0c47e-153">Getting an access token</span></span>

<span data-ttu-id="0c47e-154">Para obtener un token de acceso, la aplicación publica los parámetros del formulario codificado a la URL de solicitud del token (por ejemplo, `https://login.microsoftonline.com/common/oauth2/v2.0/token`) con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0c47e-154">To get an access token, the app posts form-encoded parameters to the token request URL (for example, `https://login.microsoftonline.com/common/oauth2/v2.0/token`) with the following parameters.</span></span>

| <span data-ttu-id="0c47e-155">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0c47e-155">Parameter</span></span> | <span data-ttu-id="0c47e-156">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0c47e-156">Descriptions</span></span> |
|:------|:------|
| <span data-ttu-id="0c47e-157">client_id</span><span class="sxs-lookup"><span data-stu-id="0c47e-157">client_id</span></span> | <span data-ttu-id="0c47e-158">El identificador de la aplicación que se genera al registrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c47e-158">The app ID generated by registering the app.</span></span> |
| <span data-ttu-id="0c47e-159">client_secret</span><span class="sxs-lookup"><span data-stu-id="0c47e-159">client_secret</span></span> | <span data-ttu-id="0c47e-160">El secreto de aplicación que se genera al registrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c47e-160">The app secret generated when registering the app.</span></span> |
| <span data-ttu-id="0c47e-161">código</span><span class="sxs-lookup"><span data-stu-id="0c47e-161">code</span></span> | <span data-ttu-id="0c47e-162">El código de autorización que se obtuvo en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="0c47e-162">The authorization code obtained in the prior step.</span></span> |
| <span data-ttu-id="0c47e-163">redirect_uri</span><span class="sxs-lookup"><span data-stu-id="0c47e-163">redirect_uri</span></span> | <span data-ttu-id="0c47e-164">Este valor debe ser el mismo que el valor usado en la solicitud del código de autorización.</span><span class="sxs-lookup"><span data-stu-id="0c47e-164">This value must be the same as the value used in the authorization code request.</span></span> |
| <span data-ttu-id="0c47e-165">grant_type</span><span class="sxs-lookup"><span data-stu-id="0c47e-165">grant_type</span></span> | <span data-ttu-id="0c47e-p114">El tipo de concesión que está usando la aplicación. Este valor es `code` para el flujo de concesión del código de autorización.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p114">The type of grant the app is using. This value is `code` for the Authorization Code Grant flow.</span></span> |
| <span data-ttu-id="0c47e-168">ámbito</span><span class="sxs-lookup"><span data-stu-id="0c47e-168">scope</span></span> | <span data-ttu-id="0c47e-169">Una lista de los ámbitos de permisos de [Microsoft Graph](./permissions_reference.md) que está solicitando la aplicación separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="0c47e-169">A space-separated list of [Microsoft Graph permission scopes](./permissions_reference.md) that the app is requesting.</span></span> |

<span data-ttu-id="0c47e-170">La URL de solicitud para nuestra aplicación, usando el código del paso anterior, tiene el aspecto que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="0c47e-170">The request URL for our application, using the code from the previous step, looks like the following.</span></span>

```
POST https://login.microsoftonline.com/common/oauth2/v2.0/token
Content-Type: application/x-www-form-urlencoded

{
  grant_type=authorization_code
  &code=AwABAAAA...cZZ6IgAA
  &redirect_uri=http%3A%2F%2Flocalhost%2Fmyapp%2F
  &resource=https%3A%2F%2Fgraph.microsoft.com%2F
  &scope=mail.read
  &client\_id=<app ID>
  &client\_secret=<app SECRET>
}
```

<span data-ttu-id="0c47e-171">El servidor responde con una carga JSON que incluye el token de acceso.</span><span class="sxs-lookup"><span data-stu-id="0c47e-171">The server responds with a JSON payload which includes the access token.</span></span>

```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "token_type":"Bearer",
  "expires_in":"3600",
  "access_token":"eyJ0eXAi...b66LoPVA",
  "scope":"https://graph.microsoft.com/mail.read",
  ...
}
```

<span data-ttu-id="0c47e-p115">El token de acceso se encuentra en el campo `access_token` de la carga JSON. La aplicación usa este valor para establecer el encabezado de autorización al realizar las llamadas REST a la API.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p115">The access token is found in the `access_token` field of the JSON payload. The app uses this value to set the Authorization header when making REST calls to the API.</span></span>

## <a name="call-microsoft-graph"></a><span data-ttu-id="0c47e-174">Llamar a Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="0c47e-174">Call Microsoft Graph</span></span>

<span data-ttu-id="0c47e-p116">Cuando la aplicación tenga un token de acceso, estará lista para llamar a Microsoft Graph. Dado que esta aplicación de ejemplo está recuperando mensajes, usará una solicitud HTTP GET al punto de conexión `https://graph.microsoft.com/v1.0/me/messages`.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p116">After the app has an access token, it's ready to call Microsoft Graph. Because this sample app is retrieving messages, it will use an HTTP GET request to the `https://graph.microsoft.com/v1.0/me/messages` endpoint.</span></span>

### <a name="refine-the-request"></a><span data-ttu-id="0c47e-177">Restringir la solicitud</span><span class="sxs-lookup"><span data-stu-id="0c47e-177">Refine the request</span></span>

<span data-ttu-id="0c47e-p117">Las aplicaciones pueden controlar el comportamiento de las solicitudes GET usando parámetros de consulta OData. Se recomienda que las aplicaciones usen estos parámetros para limitar el número de resultados que se devuelven y los campos que se devuelven para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p117">Apps can control the behavior of GET requests by using OData query parameters. We recommend that apps use these parameters to limit the number of results that are returned and to limit the fields that are returned for each item.</span></span> 

<span data-ttu-id="0c47e-p118">Esta aplicación de ejemplo mostrará los mensajes en una tabla que muestra el asunto, el remitente y la fecha y hora en que se recibió el mensaje. La tabla muestra un máximo de 25 filas y está ordenada de forma que los mensajes recibidos recientemente se encuentren en la parte superior. La aplicación usa los siguientes parámetros de consulta para obtener estos resultados.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p118">This sample app will display messages in a table that shows the subject, sender, and the date and time the message was received. The table displays a maximum of 25 rows and is sorted so that the most recently received message is at the top. The app uses the following query parameters to get these results.</span></span>

- <span data-ttu-id="0c47e-183">`$select` - Especifica solo los campos `subject`, `sender`, y `dateTimeReceived`.</span><span class="sxs-lookup"><span data-stu-id="0c47e-183">`$select` - Specifies only the `subject`, `sender`, and `dateTimeReceived` fields.</span></span>
- <span data-ttu-id="0c47e-184">`$top` - Especifica un máximo de 25 elementos.</span><span class="sxs-lookup"><span data-stu-id="0c47e-184">`$top` - Specifies a maximum of 25 items.</span></span>
- <span data-ttu-id="0c47e-185">`$orderby` - Ordena los resultados por el campo `dateTimeReceived`.</span><span class="sxs-lookup"><span data-stu-id="0c47e-185">`$orderby` - Sorts the results by the `dateTimeReceived` field.</span></span>

<span data-ttu-id="0c47e-186">Esto da como resultado la siguiente solicitud.</span><span class="sxs-lookup"><span data-stu-id="0c47e-186">This results in the following request.</span></span>

```
GET https://graph.microsoft.com/v1.0/me/messages?$select=subject,from,receivedDateTime&$top=25&$orderby=receivedDateTime%20DESC
Accept: application/json
Authorization: Bearer eyJ0eXAi...b66LoPVA
```

<span data-ttu-id="0c47e-p119">Ahora que ha visto cómo realizar llamadas a Microsoft Graph, puede usar la referencia de la API para construir cualquier otro tipo de llamada que su aplicación necesite realizar. Sin embargo, tenga en cuenta que su aplicación debe tener los permisos adecuados configurados en el registro de aplicaciones para las llamadas que realice.</span><span class="sxs-lookup"><span data-stu-id="0c47e-p119">Now that you've seen how to make calls to Microsoft Graph, you can use the API reference to construct any other kinds of calls your app needs to make. However, bear in mind that your app needs to have the appropriate permissions configured on the app registration for the calls it makes.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0c47e-189">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="0c47e-189">Next steps</span></span>
- <span data-ttu-id="0c47e-190">Pruebe más características de la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="0c47e-190">Try out more of the REST API using the [Graph explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>

## <a name="see-also"></a><span data-ttu-id="0c47e-191">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0c47e-191">See also</span></span>
- [<span data-ttu-id="0c47e-192">Protocolos de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="0c47e-192">Azure AD v2.0 protocols</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [<span data-ttu-id="0c47e-193">Tokens de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="0c47e-193">Azure AD v2.0 tokens</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)
