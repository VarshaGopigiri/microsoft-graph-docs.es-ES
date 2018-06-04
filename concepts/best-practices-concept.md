# <a name="best-practices-for-working-with-microsoft-graph"></a><span data-ttu-id="14a62-101">Procedimientos recomendados para trabajar con Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="14a62-101">Best practices for working with the OneNote API in Microsoft Graph</span></span>

<span data-ttu-id="14a62-102">En este artículo se describen los procedimientos recomendados que puede usar para que sus aplicaciones saquen el máximo provecho de Microsoft Graph, ya sea que se trate de aprender sobre Microsoft Graph, mejorar el rendimiento de las aplicaciones o aumentar la confiabilidad de la aplicación para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="14a62-102">This article describes best practices that you can apply to help your applications get the most out of Microsoft Graph - whether that involves learning about Microsoft Graph, improving app performance, or making your application more reliable for end users.</span></span>

## <a name="use-graph-explorer-to-get-to-know-the-api"></a><span data-ttu-id="14a62-103">Usar la herramienta Probador de Graph para familiarizarse con la API</span><span class="sxs-lookup"><span data-stu-id="14a62-103">Use Graph Explorer to get to know the API</span></span>

<span data-ttu-id="14a62-104">La mejor manera de empezar a explorar los datos disponibles en Microsoft Graph es usar [Probador de Graph](https://aka.ms/ge).</span><span class="sxs-lookup"><span data-stu-id="14a62-104">The easiest way to start exploring the data available through Microsoft Graph is to use [Graph Explorer](https://aka.ms/ge).</span></span> <span data-ttu-id="14a62-105">Probador de Graph le permite crear solicitudes REST (con soporte completo de CRUD), adaptar los encabezados de solicitud HTTP y ver las respuestas de datos.</span><span class="sxs-lookup"><span data-stu-id="14a62-105">Graph Explorer lets you craft REST requests (with full CRUD support), adapt the HTTP request headers, and see the data responses.</span></span> <span data-ttu-id="14a62-106">Para ayudarle a empezar, Probador de Graph ofrece también un conjunto de consultas de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="14a62-106">To help you get started, Graph Explorer also provides a set of sample queries.</span></span>

<span data-ttu-id="14a62-107">Experimente con nuevas API antes de integrarlas en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14a62-107">Experiment with new APIs before you integrate them into your application.</span></span>

## <a name="authentication"></a><span data-ttu-id="14a62-108">Autenticación</span><span class="sxs-lookup"><span data-stu-id="14a62-108">Authentication</span></span>

<span data-ttu-id="14a62-109">Para tener acceso a los datos de Microsoft Graph, la aplicación debe adquirir un token de acceso OAuth 2.0 y presentarlo a Microsoft Graph mediante:</span><span class="sxs-lookup"><span data-stu-id="14a62-109">To access the data in Microsoft Graph, your application will need to acquire an OAuth 2.0 access token, and present it to Microsoft Graph in either of the following:</span></span>

- <span data-ttu-id="14a62-110">El encabezado de solicitud *Authorization* HTTP, como token de *portador*</span><span class="sxs-lookup"><span data-stu-id="14a62-110">The HTTP *Authorization* request header, as a *Bearer* token</span></span>
- <span data-ttu-id="14a62-111">El constructor cliente de Graph, cuando use una biblioteca cliente de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="14a62-111">The graph client constructor, when using a Microsoft Graph client library</span></span>

<span data-ttu-id="14a62-112">Use la API Biblioteca de autenticación de Microsoft ([MSAL](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-libraries)) para adquirir el token de acceso a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="14a62-112">Use the Microsoft Authentication Library API, [MSAL](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-libraries) to acquire the access token to Microsoft Graph.</span></span>

## <a name="consent-and-authorization"></a><span data-ttu-id="14a62-113">Consentimiento y autorización</span><span class="sxs-lookup"><span data-stu-id="14a62-113">Consent and authorization</span></span>

<span data-ttu-id="14a62-114">Siga estos procedimientos recomendados para otorgar consentimiento y autorización en la aplicación:</span><span class="sxs-lookup"><span data-stu-id="14a62-114">Apply the following best practices for consent and authorization in your app:</span></span>

- <span data-ttu-id="14a62-115">**Utilizar privilegios mínimos**.</span><span class="sxs-lookup"><span data-stu-id="14a62-115">**Use least privilege**.</span></span> <span data-ttu-id="14a62-116">Solicite únicamente permisos absolutamente necesarios y solo cuando los necesite.</span><span class="sxs-lookup"><span data-stu-id="14a62-116">Only request permissions that are absolutely necessary, and only when you need them.</span></span> <span data-ttu-id="14a62-117">Para las API a las que llama la aplicación, consulte la sección de permisos en los temas de método (por ejemplo, vea [Crear usuario](../api-reference/v1.0/api/user_post_users.md) y elija los permisos con privilegios mínimos.</span><span class="sxs-lookup"><span data-stu-id="14a62-117">For the APIs your application calls, check the permissions section in the method topics (for example, see [creating a user](../api-reference/v1.0/api/user_post_users.md), and choose the least privileged permissions.</span></span> <span data-ttu-id="14a62-118">Para obtener la lista completa de permisos, vea [Referencia de permisos](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="14a62-118">For a full list of permissions, see [permissions reference](permissions_reference.md).</span></span>

- <span data-ttu-id="14a62-119">**Utilizar el tipo de permiso basado en escenarios adecuado**.</span><span class="sxs-lookup"><span data-stu-id="14a62-119">**Use the correct permission type based on scenarios**.</span></span> <span data-ttu-id="14a62-120">Si crea una aplicación interactiva en la que está presente un usuario que ha iniciado sesión, la aplicación debe utilizar los permisos *delegados*, en donde se delega en la aplicación el permiso para actuar como usuario que ha iniciado sesión al realizar llamadas a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="14a62-120">If you're building an interactive application where a signed in user is present, your application should use *delegated* permissions, where the application is delegated permission to act as the signed-in user when making calls to Microsoft Graph.</span></span> <span data-ttu-id="14a62-121">En cambio, si la aplicación se ejecuta sin que haya un usuario que ha iniciado sesión, como un demonio o servicio en segundo plano, la aplicación debe usar permisos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="14a62-121">If, however, your application runs without a signed-in user, such as a background service or daemon, your application should use application permissions.</span></span>

    ><span data-ttu-id="14a62-122">**Nota:** El uso de permisos de aplicación en escenarios interactivos puede exponer la aplicación a riesgos de seguridad y cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="14a62-122">**Note:** Using application permissions for interactive scenarios can put your application at compliance and security risk.</span></span> <span data-ttu-id="14a62-123">Se pueden elevar involuntariamente los privilegios de acceso a datos de un usuario, lo que elude las directivas configuradas por un administrador.</span><span class="sxs-lookup"><span data-stu-id="14a62-123">It can inadvertantly elevate a user's privileges to access data, circumnavigating policies configured by an administrator.</span></span>
<!-- LG: Use a more clear lead-in here, like "Consider the end user and admin experience"? -->
- <span data-ttu-id="14a62-124">**Tener cuidado al configurar la aplicación**.</span><span class="sxs-lookup"><span data-stu-id="14a62-124">**Be thoughtful when configuring your app**.</span></span> <span data-ttu-id="14a62-125">Esto afectará directamente a las experiencias de usuario final y de administrador, así como a la seguridad y la adopción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14a62-125">This will directly affect end user and admin experiences, along with application adoption and security.</span></span> <span data-ttu-id="14a62-126">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="14a62-126">For example:</span></span>

    - <span data-ttu-id="14a62-127">La declaración de privacidad, los términos de uso, el nombre, el logotipo y el dominio de la aplicación aparecerán en las experiencias de consentimiento y de otro tipo, por lo que debe asegurarse de configurarlos atentamente para que los usuarios finales las entiendan.</span><span class="sxs-lookup"><span data-stu-id="14a62-127">Your application's privacy statement, terms of use, name, logo and domain will show up in consent and other experiences - so make sure to configure these carefully so they are understood by your end-users.</span></span>
    - <span data-ttu-id="14a62-128">Tenga en cuenta quiénes darán consentimiento en la aplicación (administradores o usuarios finales) y configure la aplicación para [solicitar permisos adecuadamente](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-scopes).</span><span class="sxs-lookup"><span data-stu-id="14a62-128">Consider who will be consenting to your application - either end users or administrators - and configure your application to [request permissions appropriately](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-scopes).</span></span>
    - <span data-ttu-id="14a62-129">Asegúrese de que comprende la diferencia entre [consentimiento estático, dinámico e incremental](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-compare#incremental-and-dynamic-consent).</span><span class="sxs-lookup"><span data-stu-id="14a62-129">Ensure that you understand the difference between [static, dynamic and incremental consent](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-compare#incremental-and-dynamic-consent).</span></span>

- <span data-ttu-id="14a62-130">**Considerar el uso de aplicaciones multiempresa**.</span><span class="sxs-lookup"><span data-stu-id="14a62-130">**Consider multi-tenant applications**.</span></span> <span data-ttu-id="14a62-131">Cuente con la posibilidad de que los clientes tengan varios controles de aplicación y consentimiento en diferentes estados.</span><span class="sxs-lookup"><span data-stu-id="14a62-131">Expect customers to have various application and consent controls in different states.</span></span> <span data-ttu-id="14a62-132">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="14a62-132">For example:</span></span>

    - <span data-ttu-id="14a62-133">Los administradores de inquilinos pueden deshabilitar la posibilidad de que los usuarios finales den su consentimiento a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="14a62-133">Tenant administrators can disable the ability for end users to consent to applications.</span></span> <span data-ttu-id="14a62-134">En este caso, un administrador tendrá que dar el consentimiento en nombre de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="14a62-134">In this case, an administrator would need to consent on behalf of their users.</span></span>
    - <span data-ttu-id="14a62-135">Los administradores de inquilinos pueden establecer directivas de autorización personalizadas tales como impedir que los usuarios lean los perfiles de otros usuarios o restringir la creación de grupos de autoservicio a un conjunto limitado de usuarios.</span><span class="sxs-lookup"><span data-stu-id="14a62-135">Tenant administrators can set custom authorization policies such as blocking users from reading other user's profiles, or limiting self-service group creation to a limited set of users.</span></span> <span data-ttu-id="14a62-136">En este caso, es de esperar que la aplicación tenga que controlar la respuesta de error 403 cuando actúe en nombre de un usuario.</span><span class="sxs-lookup"><span data-stu-id="14a62-136">In this case, your application should expect to handle 403 error response when acting on behalf of a user.</span></span>

## <a name="handle-responses-effectively"></a><span data-ttu-id="14a62-137">Controlar las respuestas con eficacia</span><span class="sxs-lookup"><span data-stu-id="14a62-137">Handle responses effectively</span></span>

<span data-ttu-id="14a62-138">Las aplicaciones han de estar preparadas para controlar distintos tipos de respuestas en función de las solicitudes que se realicen en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="14a62-138">Depending on the requests you make to Microsoft Graph, your applications should be prepared to handle different types of responses.</span></span> <span data-ttu-id="14a62-139">Estos son algunos de los procedimientos más importantes que hay que seguir para garantizar que la aplicación tenga un comportamiento confiable y predecible para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="14a62-139">The following are some of the most important practices to follow to ensure that your application behaves reliably and predictably for your end users.</span></span>

### <a name="pagination"></a><span data-ttu-id="14a62-140">Paginación</span><span class="sxs-lookup"><span data-stu-id="14a62-140">Pagination</span></span>

<span data-ttu-id="14a62-141">Al consultar una colección de recursos, es muy probable que Microsoft Graph establezca el conjunto de resultados obtenido en varias páginas, debido a límites de tamaño de página en el servidor.</span><span class="sxs-lookup"><span data-stu-id="14a62-141">When querying a resource collection, you should expect that Microsoft Graph will the return result set in multiple pages, due to server-side page size limits.</span></span> <span data-ttu-id="14a62-142">Cuando un conjunto de resultados abarca varias páginas, Microsoft Graph devuelve una propiedad `@odata.nextLink` en la respuesta que contiene una dirección URL a la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="14a62-142">Some queries against Microsoft Graph return multiple pages of data either due to server-side paging or due to the use of the  query parameter to specifically limit the page size in a request. When a result set spans multiple pages, Microsoft Graph returns an `@odata.nextLink` property in the response that contains a URL to the next page of results.</span></span>

<span data-ttu-id="14a62-143">Por ejemplo, al mostrar los mensajes de usuarios que han iniciado sesión:</span><span class="sxs-lookup"><span data-stu-id="14a62-143">For example, listing the signed-in users messages:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages
```

<span data-ttu-id="14a62-144">Se devolverá una respuesta que contiene una propiedad `@odata.nextLink` si el conjunto de resultados supera el límite de tamaño de página del servidor.</span><span class="sxs-lookup"><span data-stu-id="14a62-144">Would return a response containing an `@odata.nextLink` property, if the result set exceeds the server-side page size limit.</span></span>

```json
"@odata.nextLink": "https://graph.microsoft.com/v1.0/me/messages?$skip=23"
```

><span data-ttu-id="14a62-145">**Nota:** La aplicación **siempre** debe controlar la posibilidad de que las respuestas se paginen por naturaleza y usen la propiedad `@odata.nextLink` para obtener el próximo conjunto de resultados paginado, hasta que se hayan leído todas las páginas del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="14a62-145">**Note:** Your application should **always** handle the possibility that the responses are paged in nature, and use the `@odata.nextLink` property to obtain the next paged set of results, until all pages of the result set have been read.</span></span> <span data-ttu-id="14a62-146">La última página no contendrá ninguna propiedad `@odata.nextLink`.</span><span class="sxs-lookup"><span data-stu-id="14a62-146">The final page will not contain an `@odata.nextLink` property.</span></span> <span data-ttu-id="14a62-147">Debe incluir la dirección URL completa en la propiedad `@odata:nextLink` de la solicitud de la siguiente página de resultados, que trata la URL completa como opaca.</span><span class="sxs-lookup"><span data-stu-id="14a62-147">Important: You should include the entire URL in the `@odata:nextLink` property in your request for the next page of results.</span></span>

<span data-ttu-id="14a62-148">Para más información, vea [paginación](paging.md).</span><span class="sxs-lookup"><span data-stu-id="14a62-148">For more details, see [](paging.md).</span></span>

### <a name="handling-expected-errors"></a><span data-ttu-id="14a62-149">Control de errores esperados</span><span class="sxs-lookup"><span data-stu-id="14a62-149">Handling expected errors</span></span>

<span data-ttu-id="14a62-150">Aunque la aplicación debe controlar todas las respuestas de error (en los rangos de 400 y 500), preste especial atención a determinados errores esperados y respuestas, que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="14a62-150">While your application should handle all error responses (in the 400 and 500 ranges), pay special attention to certain expected errors and responses, listed in the following table.</span></span>

| <span data-ttu-id="14a62-151">Tema</span><span class="sxs-lookup"><span data-stu-id="14a62-151">Topic</span></span>   | <span data-ttu-id="14a62-152">Código de error HTTP</span><span class="sxs-lookup"><span data-stu-id="14a62-152">HTTP Error Code</span></span>    | <span data-ttu-id="14a62-153">Procedimiento recomendado</span><span class="sxs-lookup"><span data-stu-id="14a62-153">Best practice</span></span>|
|:-----------|:--------|:----------|
| <span data-ttu-id="14a62-154">User does not have access (El usuario no tiene acceso)</span><span class="sxs-lookup"><span data-stu-id="14a62-154">User does not have access</span></span> | <span data-ttu-id="14a62-155">403</span><span class="sxs-lookup"><span data-stu-id="14a62-155">403 Forbidden</span></span> | <span data-ttu-id="14a62-156">Si la aplicación está funcionando, podría encontrarse este error aunque se le hayan concedido los permisos necesarios mediante una experiencia de consentimiento.</span><span class="sxs-lookup"><span data-stu-id="14a62-156">If your application is up and running, it could encounter this error even if it has been granted the necessary permissions through a consent experience.</span></span>  <span data-ttu-id="14a62-157">En este caso, es muy probable que el usuario que ha iniciado sesión no tenga privilegios de acceso al recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="14a62-157">In this case, it's most likely that the signed-in user does not have privileges to access the resource requested.</span></span> <span data-ttu-id="14a62-158">La aplicación debe presentar un error genérico "Acceso denegado" al usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="14a62-158">Your application should provide a generic "Access denied" error back to the signed-in user.</span></span> |
|<span data-ttu-id="14a62-159">No encontrado</span><span class="sxs-lookup"><span data-stu-id="14a62-159">Not Found</span></span>| <span data-ttu-id="14a62-160">404</span><span class="sxs-lookup"><span data-stu-id="14a62-160">404</span></span> | <span data-ttu-id="14a62-161">En algunos casos, es posible que no se encuentre el recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="14a62-161">In certain cases, a requested resource might not be found.</span></span> <span data-ttu-id="14a62-162">Por ejemplo, puede que un recurso no exista, porque no se ha aprovisionado todavía (como la foto de un usuario) o se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="14a62-162">For example a resource might not exist, because it has not yet been provisioned (like a user's photo) or because it has been deleted.</span></span> <span data-ttu-id="14a62-163">Algunos recursos eliminados *podrían* restaurarse completamente en los 30 días siguientes a la eliminación, como los recursos de usuario, de grupo y de aplicación, por lo que la aplicación también debe tener esto en cuenta.</span><span class="sxs-lookup"><span data-stu-id="14a62-163">Some deleted resources *might* be fully restored within 30 days of deletion - such as user, group and application resources, so your application should also take this into account.</span></span>|
|<span data-ttu-id="14a62-164">Limitación</span><span class="sxs-lookup"><span data-stu-id="14a62-164">Throttling</span></span>|<span data-ttu-id="14a62-165">429</span><span class="sxs-lookup"><span data-stu-id="14a62-165">429</span></span>|<span data-ttu-id="14a62-166">Puede que las API limiten las solicitudes en cualquier momento por diversos motivos, por lo que la aplicación debe estar **siempre** preparada para controlar respuestas 429.</span><span class="sxs-lookup"><span data-stu-id="14a62-166">APIs might throttle at any time for a variety of reasons, so your application must **always** be prepared to handle 429 responses.</span></span> <span data-ttu-id="14a62-167">Esta respuesta de error incluye el campo *Retry-After* (volver a intentar más adelante) en el encabezado de la respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="14a62-167">The failed response includes the *Retry-After* field in the response header.</span></span> <span data-ttu-id="14a62-168">La interrupción de solicitudes con el retraso *Retry-After* (volver a intentar más adelante) es la mejor forma de recuperarse de la limitación de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="14a62-168">Backing off requests using the *Retry-After* delay is the fastest way to recover from throttling because Microsoft Graph continues to log resource usage while a client is being throttled.</span></span> <span data-ttu-id="14a62-169">Para más información, vea [limitación](throttling.md).</span><span class="sxs-lookup"><span data-stu-id="14a62-169">For more information see   </span></span>|
|<span data-ttu-id="14a62-170">Servicio no disponible</span><span class="sxs-lookup"><span data-stu-id="14a62-170">Service Unavailable</span></span>| <span data-ttu-id="14a62-171">503</span><span class="sxs-lookup"><span data-stu-id="14a62-171">503</span></span> | <span data-ttu-id="14a62-172">Probablemente se deba a que el servicio está ocupado.</span><span class="sxs-lookup"><span data-stu-id="14a62-172">This is likely because the services is busy.</span></span> <span data-ttu-id="14a62-173">Debe emplear una estrategia de interrupción similar a la respuesta 429.</span><span class="sxs-lookup"><span data-stu-id="14a62-173">You should employ a back-off strategy similar to 429.</span></span> <span data-ttu-id="14a62-174">Además, debe realizar **siempre** nuevas solicitudes de reintento a través de una nueva conexión HTTP.</span><span class="sxs-lookup"><span data-stu-id="14a62-174">Additionally, you should **always** make new retry requests over a new HTTP connection.</span></span>|

### <a name="evolvable-enums"></a><span data-ttu-id="14a62-175">Enumeraciones desarrollables</span><span class="sxs-lookup"><span data-stu-id="14a62-175">Evolvable enums</span></span>

<span data-ttu-id="14a62-176">Las aplicaciones cliente pueden dividirse mediante la adición de miembros a una enumeración existente.</span><span class="sxs-lookup"><span data-stu-id="14a62-176">Client applications can be broken by the addition of members to an existing enum.</span></span> <span data-ttu-id="14a62-177">Con algunas de las enumeraciones más recientes de Microsoft Graph, hay un mecanismo disponible que permite agregar nuevos miembros sin provocar un cambio importante.</span><span class="sxs-lookup"><span data-stu-id="14a62-177">For some newer enums in Microsoft Graph, a mechanism is available to allow for adding new members without incurring a breaking change.</span></span> <span data-ttu-id="14a62-178">En estas enumeraciones más recientes, verá un miembro *centinela* común denominado `unknownFutureValue` que delimita los miembros de enumeración conocidos y desconocidos.</span><span class="sxs-lookup"><span data-stu-id="14a62-178">On these newer enums, you'll see a common *sentinel* member called `unknownFutureValue` that demarcates known and unknown enum members.</span></span> <span data-ttu-id="14a62-179">Los miembros conocidos tendrán un número menor que el miembro centinela, mientras que los miembros desconocidos tendrán un valor mayor.</span><span class="sxs-lookup"><span data-stu-id="14a62-179">Known members will have a number less than the sentinel member, while unknown members will be greater in value.</span></span>
<span data-ttu-id="14a62-180">De forma predeterminada, Microsoft Graph no devuelve miembros desconocidos.</span><span class="sxs-lookup"><span data-stu-id="14a62-180">By default, unknown members are not returned by Microsoft Graph.</span></span> <span data-ttu-id="14a62-181">Aunque, si la aplicación está escrita para controlar la aparición de miembros desconocidos, se puede optar por recibir miembros de enumeración desconocidos, mediante un encabezado de solicitud HTTP *Prefer*.</span><span class="sxs-lookup"><span data-stu-id="14a62-181">If, however, your application is written to handle the appearance of unknown members, it can opt-in to receive unknown enum members, using an HTTP *Prefer* request header.</span></span>

><span data-ttu-id="14a62-182">**Nota:** Si la aplicación está preparada para controlar los miembros de enumeración desconocidos, debe optar por recibirlos mediante un encabezado de solicitud HTTP *Prefer*: `Prefer: include-unknown-enum-members`.</span><span class="sxs-lookup"><span data-stu-id="14a62-182">**Note:** If your application is prepared to handle unknown enum members, it should opt-in by using an HTTP *prefer* request header: `Prefer: include-unknown-enum-members`.</span></span>

## <a name="storing-data-locally"></a><span data-ttu-id="14a62-183">Almacenamiento de datos local</span><span class="sxs-lookup"><span data-stu-id="14a62-183">Storing data locally</span></span>

<span data-ttu-id="14a62-184">Lo ideal es que la aplicación realice llamadas a Microsoft Graph para recuperar datos en tiempo real cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="14a62-184">Your application should ideally make calls to Microsoft Graph to retrieve data in real time as necessary.</span></span> <span data-ttu-id="14a62-185">Solo deben almacenarse datos en caché o localmente si es necesario en un escenario específico y si ese caso de uso está cubierto por las condiciones de uso y la directiva de privacidad del usuario y no infringe los [Términos de uso Microsoft Graph](../misc/terms-of-use.md).</span><span class="sxs-lookup"><span data-stu-id="14a62-185">You should only cache or store data locally if required for a specific scenario, and if that use case is covered by your terms of use and privacy policy, and does not violate the [Microsoft Graph terms of use](../misc/terms-of-use.md).</span></span> <span data-ttu-id="14a62-186">La aplicación también debe implementar políticas de retención y eliminación adecuadas.</span><span class="sxs-lookup"><span data-stu-id="14a62-186">Your application should also implement proper retention and deletion policies.</span></span>

## <a name="optimizations"></a><span data-ttu-id="14a62-187">Optimizaciones</span><span class="sxs-lookup"><span data-stu-id="14a62-187">Optimizations</span></span>

<span data-ttu-id="14a62-188">En general, por motivos de rendimiento e incluso de seguridad o privacidad, solo deben obtenerse los datos que la aplicación realmente necesita y nada más.</span><span class="sxs-lookup"><span data-stu-id="14a62-188">In general, for performance and even security or privacy reasons, you should only get the data your application really needs, and nothing more.</span></span>

### <a name="use-projections"></a><span data-ttu-id="14a62-189">Proyecciones de uso</span><span class="sxs-lookup"><span data-stu-id="14a62-189">Use projections</span></span>

<span data-ttu-id="14a62-190">Elija solo las propiedades que la aplicación realmente necesita y nada más, porque así ahorra tráfico de red y procesamiento de datos innecesarios en su aplicación (y en el servicio).</span><span class="sxs-lookup"><span data-stu-id="14a62-190">Choose only the properties your application really needs and no more, because this saves unnecessary network traffic and data processing in your application (and in the service).</span></span>

><span data-ttu-id="14a62-191">**Nota:** Utilice el parámetro de consulta `$select` para limitar las propiedades devueltas por una consulta a las necesarias para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14a62-191">**Note:** Use the `$select` query parameter to limit the properties returned by a query to those needed by your application.</span></span>

<span data-ttu-id="14a62-192">Por ejemplo, al recuperar los mensajes del usuario que ha iniciado sesión, puede especificar que solo se devuelvan las propiedades **from** y **subject**:</span><span class="sxs-lookup"><span data-stu-id="14a62-192">For example, when retrieving the messages of the signed-in user, you can specify that only the **from** and **subject** properties be returned:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

### <a name="getting-minimal-responses"></a><span data-ttu-id="14a62-193">Obtener respuestas mínimas</span><span class="sxs-lookup"><span data-stu-id="14a62-193">Getting minimal responses</span></span>

<span data-ttu-id="14a62-194">Con algunas operaciones, como PUT y PATCH (y, en algunos casos, POST), si la aplicación no tiene que usar una carga útil de respuesta, puede pedir a la API que devuelva datos mínimos.</span><span class="sxs-lookup"><span data-stu-id="14a62-194">For some operations, such as PUT and PATCH (and in some cases POST), if your application doesn't need to make use of a response payload, you can ask the API to return minimal data.</span></span> <span data-ttu-id="14a62-195">Tenga en cuenta que algunos servicios ya devuelven una respuesta 204 No Content (No hay contenido) en operaciones PUT y PATCH.</span><span class="sxs-lookup"><span data-stu-id="14a62-195">Note that some services already return a 204 No Content response for PUT and PATCH operations.</span></span>

><span data-ttu-id="14a62-196">**Nota:** Solicite respuestas de representación mínima mediante un encabezado de solicitud HTTP cuando corresponda: *Prefer: return=minimal*.</span><span class="sxs-lookup"><span data-stu-id="14a62-196">**Note:** Request minimal representation responses using an HTTP request header where appropriate: *Prefer: return=minimal*.</span></span> <span data-ttu-id="14a62-197">Tenga en cuenta que, para las operaciones de creación, esto tal vez no sea adecuado porque puede que la aplicación espere obtener el `id` del servicio generado para el objeto recién creado en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14a62-197">Note that for creation operations, this might not be appropriate because your application may expect to get the service generated `id` for the newly created object in the response.</span></span>

### <a name="track-changes-delta-query-and-webhook-notifications"></a><span data-ttu-id="14a62-198">Control de cambios: consulta delta y notificaciones de webhook</span><span class="sxs-lookup"><span data-stu-id="14a62-198">Track changes: delta query and webhook notifications</span></span>

<span data-ttu-id="14a62-199">Si la aplicación tiene que estar informada de los cambios en los datos, se puede obtener una notificación de webhook siempre que los datos de interés hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="14a62-199">If your application needs to know about changes to data, you can get a webhook notification whenever data of interest has changed.</span></span> <span data-ttu-id="14a62-200">Esto resulta más eficaz que simplemente realizar sondeos periódicamente.</span><span class="sxs-lookup"><span data-stu-id="14a62-200">This is more efficient than simply polling on a regular basis.</span></span>

<span data-ttu-id="14a62-201">Utilice [notificaciones de webhook](../api-reference/v1.0/resources/webhooks.md) para recibir notificaciones push cuando cambien los datos.</span><span class="sxs-lookup"><span data-stu-id="14a62-201">Use [webhook notifications](../api-reference/v1.0/resources/webhooks.md) to get push notifications when data changes.</span></span>

<span data-ttu-id="14a62-202">Si se requiere que la aplicación almacene en caché o localmente los datos de Microsoft Graph y los mantenga actualizados o que, por otros motivos, siga los cambios en los datos, debe utilizarse la consulta delta.</span><span class="sxs-lookup"><span data-stu-id="14a62-202">If your application is required to cache or store Microsoft Graph data locally, and keep that data up to date, or track changes to data for any other reasons, you should use delta query.</span></span> <span data-ttu-id="14a62-203">Esto evita que la aplicación realice cálculos excesivos para recuperar datos que ya tiene, minimiza el tráfico de red y reduce la probabilidad de alcanzar un umbral de limitación.</span><span class="sxs-lookup"><span data-stu-id="14a62-203">This will avoid excessive computation by your application to retrieve data your application already has, minimize network traffic, and reduce the likelihood of reaching a throttling threshold.</span></span>

<span data-ttu-id="14a62-204">Use la [consulta delta](delta_query_overview.md) para mantener los datos actualizados con eficacia.</span><span class="sxs-lookup"><span data-stu-id="14a62-204">Use [delta query](delta_query_overview.md) to efficiently keep data up to date.</span></span>

### <a name="using-webhooks-and-delta-query-together"></a><span data-ttu-id="14a62-205">Uso conjunto de webhooks y consulta delta</span><span class="sxs-lookup"><span data-stu-id="14a62-205">Using webhooks and delta query together</span></span>

<span data-ttu-id="14a62-206">Suele ser preferible utilizar los webhooks y la consulta delta juntos, porque si se utiliza solo la consulta delta, es necesario averiguar el intervalo de sondeo correcto: si es demasiado corto podría traducirse en respuestas vacías que desperdician recursos y, si es demasiado largo, es posible que se acabe con datos obsoletos.</span><span class="sxs-lookup"><span data-stu-id="14a62-206">Webhooks and delta query are often used better together, because if you use delta query alone, you need to figure out the right polling interval - too short and this might lead to empty responses which wastes resources, too long and you might end up with stale data.</span></span> <span data-ttu-id="14a62-207">Si utiliza notificaciones de webhook como desencadenador de llamadas de consulta delta, obtendrá lo mejor de ambos mundos.</span><span class="sxs-lookup"><span data-stu-id="14a62-207">If you use webhook notifications as the trigger to make delta query calls, you get the best of both worlds.</span></span>

<span data-ttu-id="14a62-208">Utilice [notificaciones de webhook](../api-reference/v1.0/resources/webhooks.md) como desencadenador de llamadas de consulta delta.</span><span class="sxs-lookup"><span data-stu-id="14a62-208">Use [webhook notifications](../api-reference/v1.0/resources/webhooks.md) as the trigger to make delta query calls.</span></span> <span data-ttu-id="14a62-209">También debe asegurarse de que la aplicación tenga un umbral de sondeo de seguridad en caso de que no se active ninguna notificación.</span><span class="sxs-lookup"><span data-stu-id="14a62-209">You should also ensure that your application has a backstop polling threshold, in case no notifications are triggered.</span></span>

### <a name="batching"></a><span data-ttu-id="14a62-210">Procesamiento por lotes</span><span class="sxs-lookup"><span data-stu-id="14a62-210">Batching</span></span>

<span data-ttu-id="14a62-211">El procesamiento por lotes de JSON le permite optimizar la aplicación combinando varias solicitudes en un solo objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="14a62-211">JSON batching allows you to optimize your application by combining multiple requests into a single JSON object. For example, a client might want to compose a view of unrelated data such as:</span></span> <span data-ttu-id="14a62-212">La combinación de solicitudes individuales en una sola solicitud por lotes puede ahorrarle a la aplicación una cantidad significativa de latencia de red y conservar los recursos de conexión.</span><span class="sxs-lookup"><span data-stu-id="14a62-212">Combining these three individual requests into a single batch request can save the application significant network latency.</span></span>

<span data-ttu-id="14a62-213">Use [procesamiento por lotes](json_batching.md) cuando una de latencia de red significativa pueda tener un gran impacto en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="14a62-213">Use [batching](json_batching.md) where significant network latency can have a big impact on the performance.</span></span>

## <a name="reliability-and-support"></a><span data-ttu-id="14a62-214">Confiabilidad y compatibilidad</span><span class="sxs-lookup"><span data-stu-id="14a62-214">Reliability and support</span></span>
<span data-ttu-id="14a62-215">Para garantizar la confiabilidad y facilitar la compatibilidad con la aplicación:</span><span class="sxs-lookup"><span data-stu-id="14a62-215">To ensure reliability and facilitate support for your application:</span></span>

- <span data-ttu-id="14a62-216">Respete el TTL de DNS y establezca el TTL de la conexión para que coincidan.</span><span class="sxs-lookup"><span data-stu-id="14a62-216">Honor DNS TTL and set connection TTL to match it.</span></span> <span data-ttu-id="14a62-217">Esto garantiza la disponibilidad en caso de conmutaciones por error.</span><span class="sxs-lookup"><span data-stu-id="14a62-217">This ensures availability in case of failovers.</span></span>
- <span data-ttu-id="14a62-218">Abra las conexiones a todas las respuestas DNS anunciadas.</span><span class="sxs-lookup"><span data-stu-id="14a62-218">Open connections to all advertised DNS answers.</span></span>
- <span data-ttu-id="14a62-219">Registre siempre el valor de *request-id* y *timestamp* del encabezado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="14a62-219">Always log the *request-id* and *timestamp* from the HTTP response header.</span></span> <span data-ttu-id="14a62-220">Esto es necesario cuando se escalan problemas o se informa de problemas de Stack Overflow o al servicio de soporte al cliente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="14a62-220">This is required when escalating issues or reporting issues in Stack Overflow or to Microsoft Customer Support.</span></span>