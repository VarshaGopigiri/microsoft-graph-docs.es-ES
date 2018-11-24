# <a name="list-subscriptions"></a><span data-ttu-id="286b6-101">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="286b6-101">List subscriptions</span></span>

<span data-ttu-id="286b6-102">Recuperar las propiedades y relaciones de suscripciones de webhook, según el identificador de la aplicación, el usuario y el rol del usuario con un inquilino.</span><span class="sxs-lookup"><span data-stu-id="286b6-102">Retrieve the properties and relationships of webhook subscriptions, based on the app ID, the user, and the user's role with a tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="286b6-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="286b6-103">Permissions</span></span>

<span data-ttu-id="286b6-104">Esta API admite los siguientes ámbitos de permisos; Para obtener más información, incluido cómo elegir permisos, vea [permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="286b6-104">This API supports the following permission scopes; to learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="286b6-105">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="286b6-105">Permission type</span></span>  | <span data-ttu-id="286b6-106">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="286b6-106">Permissions (from least to most privileged)</span></span>  |
|:---------------- |:-------------------------------------------- |
| <span data-ttu-id="286b6-107">[Permisos de delegado](../../../concepts/auth_v2_user.md) (cuenta de trabajo o escuela)</span><span class="sxs-lookup"><span data-stu-id="286b6-107">[Delegated permission](../../../concepts/auth_v2_user.md) (work or school account)</span></span> | <span data-ttu-id="286b6-108">Función necesaria para [crear la suscripción](subscription_post_subscriptions.md) o Subscription.Read.All (vea a continuación).</span><span class="sxs-lookup"><span data-stu-id="286b6-108">Role required to [create subscription](subscription_post_subscriptions.md) or Subscription.Read.All (see below).</span></span> |
| <span data-ttu-id="286b6-109">[Permisos de delegado](../../../concepts/auth_v2_user.md) (cuenta Microsoft personal)</span><span class="sxs-lookup"><span data-stu-id="286b6-109">[Delegated permission](../../../concepts/auth_v2_user.md) (personal Microsoft account)</span></span> | <span data-ttu-id="286b6-110">Función necesaria para [crear la suscripción](subscription_post_subscriptions.md) o Subscription.Read.All (vea a continuación).</span><span class="sxs-lookup"><span data-stu-id="286b6-110">Role required to [create subscription](subscription_post_subscriptions.md) or Subscription.Read.All (see below).</span></span> |
| [<span data-ttu-id="286b6-111">Permiso de aplicación</span><span class="sxs-lookup"><span data-stu-id="286b6-111">Application permission</span></span>](../../../concepts/auth_v2_service.md) | <span data-ttu-id="286b6-112">Función necesaria para [crear la suscripción](subscription_post_subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="286b6-112">Role required to [create subscription](subscription_post_subscriptions.md).</span></span> |

<span data-ttu-id="286b6-113">Los resultados de la respuesta se basan en el contexto de la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="286b6-113">Response results are based on the context of the calling app.</span></span> <span data-ttu-id="286b6-114">El siguiente es un resumen de los escenarios comunes:</span><span class="sxs-lookup"><span data-stu-id="286b6-114">The following is a summary of the common scenarios:</span></span>

### <a name="basic-scenarios"></a><span data-ttu-id="286b6-115">Escenarios básicos</span><span class="sxs-lookup"><span data-stu-id="286b6-115">Basic scenarios</span></span>

<span data-ttu-id="286b6-116">Con más frecuencia, una aplicación desea recuperar las suscripciones que creó originalmente para el usuario que ha iniciado la sesión actual, o para todos los usuarios en el directorio (las cuentas de trabajo o escuela).</span><span class="sxs-lookup"><span data-stu-id="286b6-116">Most commonly, an application wants to retrieve subscriptions that it originally created for the currently signed-in user, or for all users in the directory (work/school accounts).</span></span> <span data-ttu-id="286b6-117">Estos escenarios no requieren ningún permiso especial más allá de los que la aplicación que se usó originalmente para crear sus suscripciones.</span><span class="sxs-lookup"><span data-stu-id="286b6-117">These scenarios do not require any special permissions beyond the ones the app used originally to create its subscriptions.</span></span>

| <span data-ttu-id="286b6-118">Contexto de la aplicación que llama</span><span class="sxs-lookup"><span data-stu-id="286b6-118">Context of the calling app</span></span> | <span data-ttu-id="286b6-119">Contiene la respuesta</span><span class="sxs-lookup"><span data-stu-id="286b6-119">Response contains</span></span> |
|:-----|:---------------- |
| <span data-ttu-id="286b6-120">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="286b6-120">App is calling on behalf of the signed-in user (delegated permission).</span></span> <br/><span data-ttu-id="286b6-121">- y -</span><span class="sxs-lookup"><span data-stu-id="286b6-121">-and-</span></span><br/><span data-ttu-id="286b6-122">Aplicación tiene el permiso original necesario para [crear la suscripción](subscription_post_subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="286b6-122">App has the original permission required to [create the subscription](subscription_post_subscriptions.md).</span></span><br/><br/><span data-ttu-id="286b6-123">Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="286b6-123">Note: This applies to both personal Microsoft accounts and work/school accounts.</span></span> | <span data-ttu-id="286b6-124">Suscripciones creadas por **esta aplicación** para sólo el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="286b6-124">Subscriptions created by **this app** for the signed-in user only.</span></span> |
| <span data-ttu-id="286b6-125">Aplicación está llamando en nombre propio (permiso a la aplicación).</span><span class="sxs-lookup"><span data-stu-id="286b6-125">App is calling on behalf of itself (application permission).</span></span><br/><span data-ttu-id="286b6-126">- y -</span><span class="sxs-lookup"><span data-stu-id="286b6-126">-and-</span></span><br/><span data-ttu-id="286b6-127">Aplicación tiene el permiso original necesario para [crear la suscripción](subscription_post_subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="286b6-127">App has the original permission required to [create the subscription](subscription_post_subscriptions.md).</span></span><br/><br/><span data-ttu-id="286b6-128">Nota: Esto se aplica sólo las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="286b6-128">Note: This applies to work/school accounts only.</span></span>| <span data-ttu-id="286b6-129">Suscripciones creadas por **esta aplicación** para sí o para cualquier usuario en el directorio.</span><span class="sxs-lookup"><span data-stu-id="286b6-129">Subscriptions created by **this app** for itself or for any user in the directory.</span></span>|

### <a name="advanced-scenarios"></a><span data-ttu-id="286b6-130">Escenarios avanzados</span><span class="sxs-lookup"><span data-stu-id="286b6-130">Advanced scenarios</span></span>

<span data-ttu-id="286b6-131">En algunos casos, una aplicación desea recuperar las suscripciones creadas por otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="286b6-131">In some cases, an app wants to retrieve subscriptions created by other apps.</span></span> <span data-ttu-id="286b6-132">Por ejemplo, un usuario desea ver todas las suscripciones creadas por cualquier aplicación en su nombre.</span><span class="sxs-lookup"><span data-stu-id="286b6-132">For example, a user wants to see all subscriptions created by any app on their behalf.</span></span> <span data-ttu-id="286b6-133">O bien, puede que un administrador desee ver todas las suscripciones de todas las aplicaciones en su directorio.</span><span class="sxs-lookup"><span data-stu-id="286b6-133">Or, an administrator may want to see all subscriptions from all apps in their directory.</span></span>
<span data-ttu-id="286b6-134">Para estos escenarios, se requiere un permiso delegado Subscription.Read.All.</span><span class="sxs-lookup"><span data-stu-id="286b6-134">For such scenarios, a delegated permission Subscription.Read.All is required.</span></span>

| <span data-ttu-id="286b6-135">Contexto de la aplicación que llama</span><span class="sxs-lookup"><span data-stu-id="286b6-135">Context of the calling app</span></span> | <span data-ttu-id="286b6-136">Contiene la respuesta</span><span class="sxs-lookup"><span data-stu-id="286b6-136">Response contains</span></span> |
|:-----|:---------------- |
| <span data-ttu-id="286b6-137">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="286b6-137">App is calling on behalf of the signed-in user (delegated permission).</span></span> <span data-ttu-id="286b6-138">*El usuario es un usuario sin permisos de administrador*.</span><span class="sxs-lookup"><span data-stu-id="286b6-138">*The user is a non-admin*.</span></span> <br/><span data-ttu-id="286b6-139">- y -</span><span class="sxs-lookup"><span data-stu-id="286b6-139">-and-</span></span><br/><span data-ttu-id="286b6-140">Aplicación tiene el permiso Subscription.Read.All</span><span class="sxs-lookup"><span data-stu-id="286b6-140">App has the permission Subscription.Read.All</span></span><br/><br/><span data-ttu-id="286b6-141">Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="286b6-141">Note: This applies to both personal Microsoft accounts and work/school accounts.</span></span> | <span data-ttu-id="286b6-142">Suscripciones creadas por **cualquier aplicación** para sólo el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="286b6-142">Subscriptions created by **any app** for the signed-in user only.</span></span> |
| <span data-ttu-id="286b6-143">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="286b6-143">App is calling on behalf of the signed-in user (delegated permission).</span></span> <span data-ttu-id="286b6-144">*El usuario es un administrador*.</span><span class="sxs-lookup"><span data-stu-id="286b6-144">*The user is an admin*.</span></span><br/><span data-ttu-id="286b6-145">- y -</span><span class="sxs-lookup"><span data-stu-id="286b6-145">-and-</span></span><br/><span data-ttu-id="286b6-146">Aplicación tiene el permiso Subscription.Read.All</span><span class="sxs-lookup"><span data-stu-id="286b6-146">App has the permission Subscription.Read.All</span></span><br/><br/><span data-ttu-id="286b6-147">Nota: Esto se aplica sólo las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="286b6-147">Note: This applies to work/school accounts only.</span></span> | <span data-ttu-id="286b6-148">Suscripciones creadas por **cualquier aplicación** para **cualquier usuario** en el directorio.</span><span class="sxs-lookup"><span data-stu-id="286b6-148">Subscriptions created by **any app** for **any user** in the directory.</span></span>|

## <a name="http-request"></a><span data-ttu-id="286b6-149">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="286b6-149">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions
```

## <a name="optional-query-parameters"></a><span data-ttu-id="286b6-150">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="286b6-150">Optional query parameters</span></span>

<span data-ttu-id="286b6-151">Este método no es compatible con los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="286b6-151">This method does not support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="286b6-152">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="286b6-152">Request headers</span></span>

| <span data-ttu-id="286b6-153">Nombre</span><span class="sxs-lookup"><span data-stu-id="286b6-153">Name</span></span>       | <span data-ttu-id="286b6-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="286b6-154">Type</span></span> | <span data-ttu-id="286b6-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="286b6-155">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="286b6-156">Authorization</span><span class="sxs-lookup"><span data-stu-id="286b6-156">Authorization</span></span>  | <span data-ttu-id="286b6-157">string</span><span class="sxs-lookup"><span data-stu-id="286b6-157">string</span></span>  | <span data-ttu-id="286b6-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="286b6-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="286b6-160">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="286b6-160">Request body</span></span>

<span data-ttu-id="286b6-161">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="286b6-161">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="286b6-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="286b6-162">Response</span></span>

<span data-ttu-id="286b6-163">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="286b6-163">If successful, this method returns a `200 OK` response code and a list of [subscription](../resources/subscription.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="286b6-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="286b6-164">Example</span></span>

##### <a name="request"></a><span data-ttu-id="286b6-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="286b6-165">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_subscriptions"
}-->

```http
GET https://graph.microsoft.com/v1.0/subscriptions
```

##### <a name="response"></a><span data-ttu-id="286b6-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="286b6-166">Response</span></span>

<span data-ttu-id="286b6-167">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="286b6-167">Here's an an example of the response.</span></span>  <span data-ttu-id="286b6-168">Tenga en cuenta que es posible que esté truncada por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="286b6-168">Note that it may be truncated for brevity.</span></span>  <span data-ttu-id="286b6-169">Todos los admiten propiedades adecuadas para la solicitud y se devolverá el contexto de la llamada de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="286b6-169">All supported properties appropriate for the request and the calling context will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 586

{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#subscriptions",
  "value": [
    {
      "id": "0fc0d6db-0073-42e5-a186-853da75fb308",
      "resource": "Users",
      "applicationId": "24d3b144-21ae-4080-943f-7067b395b913",
      "changeType": "updated,deleted",
      "clientState": null,
      "notificationUrl": "https://webhookappexample.azurewebsites.net/api/notifications",
      "expirationDateTime": "2018-03-12T05:00:00Z",
      "creatorId": "8ee44408-0679-472c-bc2a-692812af3437"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List subscriptions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

<span data-ttu-id="286b6-170">Cuando una solicitud devuelve varias páginas de datos, la respuesta incluye un `@odata.nextLink` (propiedad) que le ayudarán a administrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="286b6-170">When a request returns multiple pages of data, the response includes an `@odata.nextLink` property to help you manage the results.</span></span>  <span data-ttu-id="286b6-171">Para obtener más información, vea [datos de paginación Microsoft Graph en su aplicación](../../../concepts/paging.md).</span><span class="sxs-lookup"><span data-stu-id="286b6-171">To learn more, see [Paging Microsoft Graph data in your app](../../../concepts/paging.md).</span></span>
