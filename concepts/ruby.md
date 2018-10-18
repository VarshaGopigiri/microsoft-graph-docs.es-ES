# <a name="get-started-with-microsoft-graph-in-a-ruby-on-rails-app"></a><span data-ttu-id="c3759-101">Introducción a Microsoft Graph en una aplicación de Ruby on Rails</span><span class="sxs-lookup"><span data-stu-id="c3759-101">Get started with Microsoft Graph in a Ruby on Rails app</span></span>

<span data-ttu-id="c3759-p101">En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión v2.0 de Azure AD y llamar a Microsoft Graph. Le muestra los pasos para la compilación del [Ejemplo Connect de Microsoft Graph para Ruby on Rails](https://github.com/microsoftgraph/ruby-connect-rest-sample) y explica los conceptos principales que implementará para usar Microsoft Graph. El artículo también describe cómo obtener acceso a Microsoft Graph mediante llamadas de REST directas.</span><span class="sxs-lookup"><span data-stu-id="c3759-p101">This article describes the tasks required to get an access token from the Azure AD v2.0 endpoint and call Microsoft Graph. It walks you through building the [Microsoft Graph Ruby on Rails Connect Sample](https://github.com/microsoftgraph/ruby-connect-rest-sample) and explains the main concepts that you implement to use the Microsoft Graph. The article also describes how to access Microsoft Graph by using direct REST calls.</span></span>

<span data-ttu-id="c3759-105">Para descargar una versión del ejemplo Connect que usa el punto de conexión de Azure AD, consulte el [Ejemplo Connect de Microsoft Graph para Ruby on Rails](https://github.com/microsoftgraph/ruby-connect-rest-sample/tree/last_v1_auth).</span><span class="sxs-lookup"><span data-stu-id="c3759-105">To download a version of the Connect sample that uses the Azure AD endpoint, see [Microsoft Graph Ruby on Rails Connect Sample](https://github.com/microsoftgraph/ruby-connect-rest-sample/tree/last_v1_auth).</span></span>

<span data-ttu-id="c3759-106">En la imagen siguiente, se muestra la aplicación que va a crear.</span><span class="sxs-lookup"><span data-stu-id="c3759-106">The following image shows the app you'll create.</span></span> 

![Captura de pantalla del ejemplo Microsoft Ruby on Rails Connect](./images/Microsoft-Graph-Ruby-Connect-UI.png)

<span data-ttu-id="c3759-p102">**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/en-us/getting-started) para ponerlo todo en funcionamiento de manera rápida o descargue el [Ejemplo Connect de REST de Ruby](https://github.com/microsoftgraph/ruby-connect-rest-sample) en el que se basa este artículo.</span><span class="sxs-lookup"><span data-stu-id="c3759-p102">**Don't feel like building an app?** Use the [Microsoft Graph quick start](https://graph.microsoft.io/en-us/getting-started) to get up and running fast, or download the [Ruby REST Connect sample](https://github.com/microsoftgraph/ruby-connect-rest-sample) that this article is based on.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="c3759-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c3759-110">Prerequisites</span></span>

<span data-ttu-id="c3759-111">Para comenzar, necesitará:</span><span class="sxs-lookup"><span data-stu-id="c3759-111">To get started, you'll need:</span></span> 

- <span data-ttu-id="c3759-112">Ruby 2.1 para ejecutar el ejemplo en un servidor de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c3759-112">Ruby 2.1 to run the sample on a development server.</span></span>
- <span data-ttu-id="c3759-113">Marco Rails (el ejemplo se probó con Rails 4.2).</span><span class="sxs-lookup"><span data-stu-id="c3759-113">Rails framework (the sample has been tested on Rails 4.2).</span></span>
- <span data-ttu-id="c3759-114">Administrador de dependencias Bundler.</span><span class="sxs-lookup"><span data-stu-id="c3759-114">Bundler dependency manager.</span></span>
- <span data-ttu-id="c3759-115">Interfaz de servidor web Rack para Ruby.</span><span class="sxs-lookup"><span data-stu-id="c3759-115">Rack web server interface for Ruby.</span></span>
- <span data-ttu-id="c3759-116">Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program-faq#account-types)</span><span class="sxs-lookup"><span data-stu-id="c3759-116">A [Microsoft account](https://www.outlook.com/) or a [work or school account](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program-faq#account-types)</span></span>
- <span data-ttu-id="c3759-p103">Proyecto inicial de conexión de Microsoft Graph para Ruby on Rails. Descargue el [Ejemplo Connect de Microsoft Graph de Ruby on Rails](https://github.com/microsoftgraph/ruby-connect-rest-sample). El proyecto inicial se encuentra en la carpeta _starter_.</span><span class="sxs-lookup"><span data-stu-id="c3759-p103">The Microsoft Graph Connect Starter Project for Ruby on Rails. Download the [Microsoft Graph Ruby on Rails Connect Sample](https://github.com/microsoftgraph/ruby-connect-rest-sample). The starter project is located in the _starter_ folder.</span></span>


## <a name="register-the-application"></a><span data-ttu-id="c3759-120">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="c3759-120">Register the application</span></span>

<span data-ttu-id="c3759-p104">Registre una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el ID y el secreto de aplicación que usará para configurar la aplicación para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="c3759-p104">Register an app on the Microsoft App Registration Portal. This generates the app ID and secret that you'll use to configure the app for authentication.</span></span>

1. <span data-ttu-id="c3759-123">Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="c3759-123">Sign into the [Microsoft App Registration Portal](https://apps.dev.microsoft.com/) using either your personal or work or school account.</span></span>

2. <span data-ttu-id="c3759-124">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="c3759-124">Choose **Add an app**.</span></span>

3. <span data-ttu-id="c3759-125">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="c3759-125">Enter a name for the app, and choose **Create application**.</span></span>

    <span data-ttu-id="c3759-126">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3759-126">The registration page displays, listing the properties of your app.</span></span>

4. <span data-ttu-id="c3759-p105">Copie el identificador de la aplicación. Se trata del identificador único para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3759-p105">Copy the application ID. This is the unique identifier for your app.</span></span>

5. <span data-ttu-id="c3759-p106">En **Secretos de aplicación**, seleccione **Generar nueva contraseña**. Copie el secreto de aplicación del cuadro de diálogo **Nueva contraseña generada**.</span><span class="sxs-lookup"><span data-stu-id="c3759-p106">Under **Application Secrets**, choose **Generate New Password**. Copy the app secret from the **New password generated** dialog.</span></span>

    <span data-ttu-id="c3759-131">Deberá usar el ID y el secreto de aplicación para configurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3759-131">You'll use the application ID and app secret to configure the app.</span></span>

6. <span data-ttu-id="c3759-132">En **Plataformas**, pulse **Agregar plataforma** > **Web**.</span><span class="sxs-lookup"><span data-stu-id="c3759-132">Under **Platforms**, choose **Add platform** > **Web**.</span></span>

7. <span data-ttu-id="c3759-133">Asegúrese de que la casilla **Permitir flujo implícito** esté activada y escriba *http://localhost:3000/auth/microsoft_v2_auth/callback* como el URI de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="c3759-133">Make sure the **Allow Implicit Flow** check box is selected, and enter *http://localhost:3000/auth/microsoft_v2_auth/callback* as the Redirect URI.</span></span>

    <span data-ttu-id="c3759-p107">La opción Permitir flujo implícito habilita el flujo híbrido de OpenID Connect. Durante la autenticación, esto permite que la aplicación reciba tanto la información de inicio de sesión (id_token) como los artefactos (en este caso, un código de autorización) que la aplicación usa para obtener un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="c3759-p107">The Allow Implicit Flow option enables the OpenID Connect hybrid flow. During authentication, this enables the app to receive both sign-in info (the id_token) and artifacts (in this case, an authorization code) that the app uses to obtain an access token.</span></span>

    <span data-ttu-id="c3759-136">El URI de redireccionamiento *http://localhost:3000/auth/microsoft_v2_auth/callback* es el valor que usará el middleware de OmniAuth después de procesar la solicitud de autenticación.</span><span class="sxs-lookup"><span data-stu-id="c3759-136">The redirect URI *http://localhost:3000/auth/microsoft_v2_auth/callback* is the value that the OmniAuth middleware is configured to use once it has processed the authentication request.</span></span>

8. <span data-ttu-id="c3759-137">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c3759-137">Choose **Save**.</span></span>

## <a name="configure-the-project"></a><span data-ttu-id="c3759-138">Configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="c3759-138">Configure the project</span></span>

1. <span data-ttu-id="c3759-p108">Descargue o clone el [Ejemplo Connect de Microsoft Graph de Ruby on Rails](https://github.com/microsoftgraph/ruby-connect-rest-sample). Abra la carpeta _starter_ en el editor que prefiera.</span><span class="sxs-lookup"><span data-stu-id="c3759-p108">Download or clone the [Microsoft Graph Ruby on Rails Connect Sample](https://github.com/microsoftgraph/ruby-connect-rest-sample). Open the _starter_ folder in the editor of your choice.</span></span>
1. <span data-ttu-id="c3759-141">Si todavía no tiene Bundler ni Rack, puede instalarlos con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="c3759-141">If you don't already have bundler and rack, you can install them with the following command.</span></span>

    ```
    gem install bundler rack
    ```
2. <span data-ttu-id="c3759-142">En el archivo config/environment.rb realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c3759-142">In the config/environment.rb file, do the following:</span></span>
    - <span data-ttu-id="c3759-143">Reemplace *ENTER_YOUR_CLIENT_ID* por el identificador de cliente de su aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="c3759-143">Replace *ENTER_YOUR_CLIENT_ID* with the client ID of your registered  application.</span></span>
    - <span data-ttu-id="c3759-144">Reemplace *ENTER_YOUR_SECRET* por la clave de su aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="c3759-144">Replace *ENTER_YOUR_SECRET* with the key of your registered application.</span></span>

3. <span data-ttu-id="c3759-145">Instale la aplicación Rails y las dependencias con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="c3759-145">Install the Rails application and dependencies with the following command.</span></span>

    ```
    bundle install
    ```

## <a name="authenticate-the-user-and-get-an-access-token"></a><span data-ttu-id="c3759-146">Autenticar al usuario y obtener un token de acceso</span><span class="sxs-lookup"><span data-stu-id="c3759-146">Authenticate the user and get an access token</span></span>

<span data-ttu-id="c3759-p109">Esta aplicación usa el flujo de concesión de códigos de autorización con una identidad de usuario delegado. Para una aplicación web, el flujo requiere el identificador de la aplicación, el secreto y el URI de redireccionamiento de la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="c3759-p109">This app uses the authorization code grant flow with a delegated user identity. For a web application, the flow requires the application ID, secret, and redirect URI from the registered app.</span></span> 

<span data-ttu-id="c3759-149">El flujo de autenticación puede desglosarse en los siguientes pasos básicos:</span><span class="sxs-lookup"><span data-stu-id="c3759-149">The auth flow can be broken down into these basic steps:</span></span>

1. <span data-ttu-id="c3759-150">Redirigir al usuario para la autenticación y el consentimiento</span><span class="sxs-lookup"><span data-stu-id="c3759-150">Redirect the user for authentication and consent</span></span>
2. <span data-ttu-id="c3759-151">Obtener un código de autorización</span><span class="sxs-lookup"><span data-stu-id="c3759-151">Get an authorization code</span></span>
3. <span data-ttu-id="c3759-152">Canjear el código de autorización por un token de acceso</span><span class="sxs-lookup"><span data-stu-id="c3759-152">Redeem the authorization code for an access token</span></span>

><span data-ttu-id="c3759-153">Para obtener más información acerca de este flujo de autenticación, consulte [Aplicación web a API web](https://azure.microsoft.com/en-us/documentation/articles/active-directory-authentication-scenarios/#web-application-to-web-api) e [Integrar la identidad de Microsoft y Microsoft Graph en una aplicación web mediante OpenID Connect](https://azure.microsoft.com/en-us/documentation/samples/active-directory-dotnet-webapp-openidconnect-v2/) en la documentación de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c3759-153">For more information about this auth flow, see [Web application to web API](https://azure.microsoft.com/en-us/documentation/articles/active-directory-authentication-scenarios/#web-application-to-web-api) and  [Integrate Microsoft identity and the Microsoft Graph into a web application using OpenID Connect](https://azure.microsoft.com/en-us/documentation/samples/active-directory-dotnet-webapp-openidconnect-v2/) in the Azure AD documentation.</span></span>

<span data-ttu-id="c3759-154">Usaremos una pila de tres partes del middleware [Rack](http://rack.github.io/) para habilitar la aplicación para que se autentique en Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="c3759-154">We'll be using a stack of three pieces of [Rack](http://rack.github.io/) middleware to enable the app to authenticate against the Microsoft Graph:</span></span>

- <span data-ttu-id="c3759-155">[OmniAuth](https://rubygems.org/gems/omniauth), un marco generalizado de Rack para la autenticación de varios proveedores.</span><span class="sxs-lookup"><span data-stu-id="c3759-155">[OmniAuth](https://rubygems.org/gems/omniauth), a generalized Rack framework for multiple-provider authentication.</span></span>
- <span data-ttu-id="c3759-156">[Omniauth-oauth2](https://rubygems.org/gems/omniauth-oauth2), una estrategia abstracta de OAuth2 para OmniAuth.</span><span class="sxs-lookup"><span data-stu-id="c3759-156">[Omniauth-oauth2](https://rubygems.org/gems/omniauth-oauth2), an abstract OAuth2 strategy for OmniAuth.</span></span> 
- <span data-ttu-id="c3759-p110">omniauth-microsoft_v2_auth, una estrategia de OmniAuth que personaliza Omniauth-oauth2 específicamente para proporcionar autenticación en el punto de conexión v2.0 de Azure AD. Este proyecto se incluye en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="c3759-p110">omniauth-microsoft_v2_auth, an OmniAuth strategy that customizes Omniauth-oauth2 to specifically provide authentication against the Azure AD v2.0 endpoint. This project is included in the code sample.</span></span>

### <a name="specify-gem-dependencies-for-authentication"></a><span data-ttu-id="c3759-159">Especificar dependencias de gemas para la autenticación</span><span class="sxs-lookup"><span data-stu-id="c3759-159">Specify gem dependencies for authentication</span></span>

<span data-ttu-id="c3759-160">En Gemfile, quite el comentario de las siguientes gemas para agregarlas como dependencias.</span><span class="sxs-lookup"><span data-stu-id="c3759-160">In Gemfile, uncomment the following gems to add them as dependencies.</span></span>

    ```
    gem 'omniauth'
    gem 'omniauth-oauth2'
    gem 'omniauth-microsoft_v2_auth', path: './omniauth-microsoft_v2_auth'
    ```

<span data-ttu-id="c3759-161">Tenga en cuenta que `omniauth-microsoft_v2_auth` se incluye en el proyecto de la aplicación y se instalará desde la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="c3759-161">Note that `omniauth-microsoft_v2_auth` is included in the app project, and will be installed from the path specified.</span></span> 

### <a name="configure-the-authentication-middleware"></a><span data-ttu-id="c3759-162">Configurar el middleware de autenticación</span><span class="sxs-lookup"><span data-stu-id="c3759-162">Configure the authentication middleware</span></span>

<span data-ttu-id="c3759-163">En `config/initializers/omniauth-microsoft_v2_auth.rb`, quite la marca de comentario de las siguientes líneas.</span><span class="sxs-lookup"><span data-stu-id="c3759-163">In `config/initializers/omniauth-microsoft_v2_auth.rb`, uncomment the following lines.</span></span>

    ```
    Rails.application.config.middleware.use OmniAuth::Builder do
      provider :microsoft_v2_auth,
      ENV['CLIENT_ID'],
      ENV['CLIENT_SECRET'],
      :scope => ENV['SCOPE']
    end
    ```
<span data-ttu-id="c3759-p111">Esta acción configura el middleware de OmniAuth, incluida la especificación del ID y el secreto de aplicación que se usarán, así como los ámbitos que se solicitarán para el usuario. Estos son los valores que especificó anteriormente en `config/environment.rb`.</span><span class="sxs-lookup"><span data-stu-id="c3759-p111">This configures the OmniAuth middleware, including specifying the app ID and app secret to use, as well as the scopes to request for the user. These are the values you specified earlier in `config/environment.rb`.</span></span>

### <a name="specify-routes-for-authentication"></a><span data-ttu-id="c3759-166">Especificar rutas para la autenticación</span><span class="sxs-lookup"><span data-stu-id="c3759-166">Specify routes for authentication</span></span>

<span data-ttu-id="c3759-p112">Ahora, debemos especificar dos rutas necesarias para el flujo de autenticación. La primera ruta reenvía la solicitud de autenticación al middleware de OmniAuth. La segunda ruta especifica la ubicación de la aplicación a la que OmniAuth deberá redirigir una vez que se haya realizado la autenticación.</span><span class="sxs-lookup"><span data-stu-id="c3759-p112">Now we need to specify two routes necessary for the authentication flow. The first route forwards the authentication request to the OmniAuth middleware, and the second specifies the location in the app to which OmniAuth should redirect once authentication has occurred.</span></span>

<span data-ttu-id="c3759-169">En `config/routes.rb`, quite la marca de comentario de la siguiente directiva de ruta.</span><span class="sxs-lookup"><span data-stu-id="c3759-169">In `config/routes.rb`, uncomment the following route directive.</span></span>

    get '/login', to: 'pages#login'

<span data-ttu-id="c3759-170">Esto dirige las solicitudes de inicio de sesión al método `login` del controlador de páginas, que a su vez redirige la solicitud al middleware omniauth-microsoft_v2_auth.</span><span class="sxs-lookup"><span data-stu-id="c3759-170">This directs login requests to the pages controller's `login` method, which in turn redirects the request to the omniauth-microsoft_v2_auth middleware.</span></span>

    def login
        redirect_to '/auth/microsoft_v2_auth'
    end

<span data-ttu-id="c3759-p113">Después, necesita especificar la ubicación de la aplicación a la que OmniAuth redirigirá cuando se realice la autenticación. Quite la marca de comentario de la ruta siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3759-p113">Next, we need to specify where in the app OmniAuth should redirect once authentication has occurred. Uncomment the following route.</span></span>

    match '/auth/:provider/callback', to: 'pages#callback', via: [:get, :post]

<span data-ttu-id="c3759-173">Cuando OmniAuth termine de autenticar al usuario, llamará a la URL de redireccionamiento especificada en el registro de la aplicación (en este caso, *http://localhost:3000/auth/microsoft_v2_auth/callback*).</span><span class="sxs-lookup"><span data-stu-id="c3759-173">When OmniAuth has finished authenticating the user, it calls the redirect URL specified in the app registration; in this case, *http://localhost:3000/auth/microsoft_v2_auth/callback*.</span></span> <span data-ttu-id="c3759-174">El patrón de ruta anterior coincide con esa URL y, en consecuencia, redirige la solicitud al método `callback` del controlador de páginas.</span><span class="sxs-lookup"><span data-stu-id="c3759-174">The route pattern above matches that URL and so routes the request to the page controller's `callback` method.</span></span>

### <a name="get-an-access-token"></a><span data-ttu-id="c3759-175">Obtener un token de acceso</span><span class="sxs-lookup"><span data-stu-id="c3759-175">Get an access token</span></span>

<span data-ttu-id="c3759-176">A continuación, agregaremos el código que realmente inicia el proceso de autenticación y recupera el token de acceso una vez que el usuario ha iniciado sesión correctamente.</span><span class="sxs-lookup"><span data-stu-id="c3759-176">Next, we'll add the code that actually starts the authentication process, and retrieves the access token once the user has successfully signed in.</span></span>

<span data-ttu-id="c3759-p115">Eche un vistazo a `app/views/pages/index.html.erb`, la vista de la raíz del sitio. La vista incluye un solo botón, que permite a los usuarios iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="c3759-p115">Take a look at `app/views/pages/index.html.erb`, the view for the site root. The view includes a single button, which enables users to sign in.</span></span>

    <button class="ms-Button" onclick="window.location.href = '/login'">
        <span class="ms-Button-label"><%= t('connect_button') %></span>
    </button>

<span data-ttu-id="c3759-p116">Como se muestra anteriormente, el método de inicio de sesión redirige al middleware de OmniAuth, que se ha configurado con el ID y el secreto de aplicación, así como con los ámbitos que se van a solicitar para el usuario. Una vez que el usuario se autentique correctamente, OmniAuth devolverá un hash con el token de acceso y otra información de usuario a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3759-p116">As shown earlier, the login method redirects to the OmniAuth middleware, which has been configured with the app ID and app secret, as well as the scopes to request for the user. Once the user is successfully authenticated, OmniAuth returns a hash with the access token and other user information to the app.</span></span>

<span data-ttu-id="c3759-181">Ahora, agregaremos el código para realizar la devolución de llamada de OmniAuth y recuperar la información de ese hash.</span><span class="sxs-lookup"><span data-stu-id="c3759-181">Now let's add code to handle the OmniAuth callback, and retrieve information from that hash.</span></span> 

<span data-ttu-id="c3759-182">En `app/controllers/pages_controller.rb`, reemplace el método vacío `callback` por el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3759-182">In `app/controllers/pages_controller.rb`, replace the empty `callback` method with the following code.</span></span>

    ```
    def callback
        # Access the authentication hash for omniauth
        # and extract the auth token, user name, and email
        data = request.env['omniauth.auth']
    
        @email = data[:extra][:raw_info][:userPrincipalName]
        @name = data[:extra][:raw_info][:displayName]

        # Associate token/user values to the session
        session[:access_token] = data['credentials']['token']
        session[:name] = @name
        session[:email] = @email
        
        # Debug logging
        logger.info "Name: #{@name}"
        logger.info "Email: #{@email}"
        logger.info "[callback] - Access token: #{session[:access_token]}"
    end

    ```

<span data-ttu-id="c3759-183">Este método recupera el hash de autenticación y, a continuación, almacena el token de acceso, el nombre de usuario y el correo electrónico en la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="c3759-183">This method retrieves the authentication hash, and then stores the access token, user name, and email in the current session.</span></span>

> <span data-ttu-id="c3759-p117">**Nota:** La autenticación simple y el uso de tokens en este proyecto se presentan solo con fines ilustrativos. En una aplicación de producción, deberá crear una forma más segura de usar la autenticación, incluidos el uso seguro de tokens y la actualización de tokens.</span><span class="sxs-lookup"><span data-stu-id="c3759-p117">**Note:** The simple authentication  and token handling in this project is presented for illustrative purposes only. In a production app, you would likely construct a more robust way of handling authentication, including secure token handling and token refresh.</span></span>

## <a name="call-microsoft-graph"></a><span data-ttu-id="c3759-186">Llamar a Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c3759-186">Call Microsoft Graph</span></span>

<span data-ttu-id="c3759-187">Ahora, ya puede agregar el código para llamar a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c3759-187">Now you're ready to add code to call Microsoft Graph.</span></span> 

<span data-ttu-id="c3759-p118">La vista que representa el método `callback` (`app/views/pages/callback.html.erb`) incluye un formulario simple con un solo botón. El formulario se publica en `send_mail` e incluye un solo parámetro: la dirección de correo electrónico del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c3759-p118">The view rendered by the `callback` method (`app/views/pages/callback.html.erb`) includes a simple form with a single button. The form posts to  `send_mail`, and includes a single parameter, the email address of the intended recipient.</span></span>
    
    ``` 
    <form action="../../send_mail" method="post">
      <div class="ms-Grid-col ms-u-mdPush1 ms-u-md9 ms-u-lgPush1 ms-u-lg6">
        ...
            <div class="ms-TextField">
               <input class="ms-TextField-field" name="specified_email" value="<%= @email %>">
            </div>
            <button class="ms-Button">
            <span class="ms-Button-label"><i class="ms-Icon ms-Icon--mail" aria-hidden="true"></i><%= t('send_mail_button') %></span>
            </button> 
        ...
    ```

<span data-ttu-id="c3759-190">En `app/controllers/pages_controller.rb`, reemplace el método vacío `send_mail` por el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3759-190">In `app/controllers/pages_controller.rb`, replace the empty `send_mail` method with the following code.</span></span>

    ```
    def send_mail
        logger.debug "[send_mail] - Access token: #{session[:access_token]}"
        
        # Used in the template
        @name = session[:name]
        @email = params[:specified_email]
        @recipient = params[:specified_email]
        @mail_sent = false
        
        send_mail_endpoint = URI("#{GRAPH_RESOURCE}#{SENDMAIL_ENDPOINT}")
        content_type = CONTENT_TYPE
        http = Net::HTTP.new(send_mail_endpoint.host, send_mail_endpoint.port)
        http.use_ssl = true
        
        # If you want to use a sniffer tool, like Fiddler, to see the request
        # you might need to add this line to tell the engine not to verify the
        # certificate or you might see a "certificate verify failed" error
        # http.verify_mode = OpenSSL::SSL::VERIFY_NONE
        
        email_body = File.read('app/assets/MailTemplate.html')
        email_body.sub! '{given_name}', @name
        email_subject = t('email_subject')
        
        logger.debug email_body
    
        email_message = "{
            Message: {
            Subject: '#{email_subject}',
            Body: {
                ContentType: 'HTML',
                Content: '#{email_body}'
            },
            ToRecipients: [
                {
                    EmailAddress: {
                        Address: '#{@recipient}'
                    }
                }
            ]
            },
            SaveToSentItems: true
            }"
            
        response = http.post(
            SENDMAIL_ENDPOINT,
            email_message,
            'Authorization' => "Bearer #{session[:access_token]}",
            'Content-Type' => content_type
        )
        
        logger.debug "Code: #{response.code}"
        logger.debug "Message: #{response.message}"
        
        # The send mail endpoint returns a 202 - Accepted code on success
        if response.code == '202'
            @mail_sent = true
        else
            @mail_sent = false
            flash[:httpError] = "#{response.code} - #{response.message}"
        end
        
        render 'callback'
    end
    ```

<span data-ttu-id="c3759-191">Este código crea la solicitud HTTP, aplica formato al correo electrónico y, a continuación, llama a Microsoft Graph para enviarlo.</span><span class="sxs-lookup"><span data-stu-id="c3759-191">This code constructs the HTTP request, formats the email, and then calls Microsoft Graph to send the email.</span></span>

<span data-ttu-id="c3759-p119">Para crear el correo electrónico, el código extrae el nombre de usuario del token de sesión y la dirección de correo electrónico del destinatario de los parámetros que se han pasado desde el formulario. A continuación, el código lee el cuerpo del correo electrónico desde una plantilla que se incluye en el proyecto, interpola el nombre de usuario y la dirección de correo electrónico y asocia el texto del correo electrónico como cuerpo de la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="c3759-p119">To create the email, the code pulls the user name from the session token and the recipient email address from the parameters passed from the form. The code then reads the email body from a template included in the project, interpolates the user name and email address, and attaches the email text as the HTTP request body.</span></span>

<span data-ttu-id="c3759-194">Para enviar el correo electrónico, el código crea la solicitud HTTP, adjunta el token de acceso como encabezado de autorización y, a continuación, publica la solicitud en el punto de conexión de envío de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c3759-194">To send the email, the code constructs the HTTP request, attaches the access token as an authorization header, and then posts the request to the send email endpoint.</span></span>

<span data-ttu-id="c3759-195">Por último, el código usa el código de respuesta HTTP que se ha devuelto para notificar al usuario si el correo electrónico se envió o no correctamente.</span><span class="sxs-lookup"><span data-stu-id="c3759-195">Finally, the code uses the HTTP response code returned to notify the user whether or not the email was successful.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="c3759-196">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="c3759-196">Run the app</span></span>

1. <span data-ttu-id="c3759-197">Instale la aplicación Rails y las dependencias con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="c3759-197">Install the Rails application and dependencies with the following command.</span></span>

    ```
    bundle install
    ```
2. <span data-ttu-id="c3759-198">Para iniciar la aplicación Rails, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="c3759-198">To start the Rails application, type the following command.</span></span>

    ```
    rackup -p 3000
    ```
3. <span data-ttu-id="c3759-199">Vaya a `http://localhost:3000` en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="c3759-199">Go to `http://localhost:3000` in your web browser.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3759-200">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c3759-200">See also</span></span>
- <span data-ttu-id="c3759-201">Pruebe la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="c3759-201">Try out the REST API using the [Graph explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>
- <span data-ttu-id="c3759-202">Explore nuestros otros [ejemplos de Microsoft Graph](https://github.com/microsoftgraph) en GitHub.</span><span class="sxs-lookup"><span data-stu-id="c3759-202">Explore our other [Microsoft Graph samples](https://github.com/microsoftgraph) on GitHub.</span></span>


