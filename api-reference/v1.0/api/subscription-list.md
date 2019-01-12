---
title: Suscripciones de lista
description: Recuperar las propiedades y relaciones de suscripciones de webhook, según el identificador de la aplicación, el usuario y el rol del usuario con un inquilino.
localization_priority: Priority
author: piotrci
ms.openlocfilehash: c2e9446721f4390341c33f8b976893e4b1ab14be
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972939"
---
# <a name="list-subscriptions"></a><span data-ttu-id="65214-103">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="65214-103">List subscriptions</span></span>

<span data-ttu-id="65214-104">Recuperar las propiedades y relaciones de suscripciones de webhook, según el identificador de la aplicación, el usuario y el rol del usuario con un inquilino.</span><span class="sxs-lookup"><span data-stu-id="65214-104">Retrieve the properties and relationships of webhook subscriptions, based on the app ID, the user, and the user's role with a tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="65214-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="65214-105">Permissions</span></span>

<span data-ttu-id="65214-106">Esta API admite los siguientes ámbitos de permisos; Para obtener más información, incluido cómo elegir permisos, vea [permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65214-106">This API supports the following permission scopes; to learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="65214-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65214-107">Permission type</span></span>  | <span data-ttu-id="65214-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65214-108">Permissions (from least to most privileged)</span></span>  |
|:---------------- |:-------------------------------------------- |
| <span data-ttu-id="65214-109">[Permisos de delegado](/graph/auth-v2-user) (cuenta de trabajo o escuela)</span><span class="sxs-lookup"><span data-stu-id="65214-109">[Delegated permission](/graph/auth-v2-user) (work or school account)</span></span> | <span data-ttu-id="65214-110">Función necesaria para [crear la suscripción](subscription-post-subscriptions.md) o Subscription.Read.All (vea a continuación).</span><span class="sxs-lookup"><span data-stu-id="65214-110">Role required to [create subscription](subscription-post-subscriptions.md) or Subscription.Read.All (see below).</span></span> |
| <span data-ttu-id="65214-111">[Permisos de delegado](/graph/auth-v2-user) (cuenta Microsoft personal)</span><span class="sxs-lookup"><span data-stu-id="65214-111">[Delegated permission](/graph/auth-v2-user) (personal Microsoft account)</span></span> | <span data-ttu-id="65214-112">Función necesaria para [crear la suscripción](subscription-post-subscriptions.md) o Subscription.Read.All (vea a continuación).</span><span class="sxs-lookup"><span data-stu-id="65214-112">Role required to [create subscription](subscription-post-subscriptions.md) or Subscription.Read.All (see below).</span></span> |
| [<span data-ttu-id="65214-113">Permiso de aplicación</span><span class="sxs-lookup"><span data-stu-id="65214-113">Application permission</span></span>](/graph/auth-v2-service) | <span data-ttu-id="65214-114">Función necesaria para [crear la suscripción](subscription-post-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="65214-114">Role required to [create subscription](subscription-post-subscriptions.md).</span></span> |

<span data-ttu-id="65214-115">Los resultados de la respuesta se basan en el contexto de la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="65214-115">Response results are based on the context of the calling app.</span></span> <span data-ttu-id="65214-116">El siguiente es un resumen de los escenarios comunes:</span><span class="sxs-lookup"><span data-stu-id="65214-116">The following is a summary of the common scenarios:</span></span>

### <a name="basic-scenarios"></a><span data-ttu-id="65214-117">Escenarios básicos</span><span class="sxs-lookup"><span data-stu-id="65214-117">Basic scenarios</span></span>

<span data-ttu-id="65214-118">Con más frecuencia, una aplicación desea recuperar las suscripciones que creó originalmente para el usuario que ha iniciado la sesión actual, o para todos los usuarios en el directorio (las cuentas de trabajo o escuela).</span><span class="sxs-lookup"><span data-stu-id="65214-118">Most commonly, an application wants to retrieve subscriptions that it originally created for the currently signed-in user, or for all users in the directory (work/school accounts).</span></span> <span data-ttu-id="65214-119">Estos escenarios no requieren ningún permiso especial más allá de los que la aplicación que se usó originalmente para crear sus suscripciones.</span><span class="sxs-lookup"><span data-stu-id="65214-119">These scenarios do not require any special permissions beyond the ones the app used originally to create its subscriptions.</span></span>

| <span data-ttu-id="65214-120">Contexto de la aplicación que llama</span><span class="sxs-lookup"><span data-stu-id="65214-120">Context of the calling app</span></span> | <span data-ttu-id="65214-121">Contiene la respuesta</span><span class="sxs-lookup"><span data-stu-id="65214-121">Response contains</span></span> |
|:-----|:---------------- |
| <span data-ttu-id="65214-122">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="65214-122">App is calling on behalf of the signed-in user (delegated permission).</span></span> <br/><span data-ttu-id="65214-123">- y -</span><span class="sxs-lookup"><span data-stu-id="65214-123">-and-</span></span><br/><span data-ttu-id="65214-124">Aplicación tiene el permiso original necesario para [crear la suscripción](subscription-post-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="65214-124">App has the original permission required to [create the subscription](subscription-post-subscriptions.md).</span></span><br/><br/><span data-ttu-id="65214-125">Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="65214-125">Note: This applies to both personal Microsoft accounts and work/school accounts.</span></span> | <span data-ttu-id="65214-126">Suscripciones creadas por **esta aplicación** para sólo el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="65214-126">Subscriptions created by **this app** for the signed-in user only.</span></span> |
| <span data-ttu-id="65214-127">Aplicación está llamando en nombre propio (permiso a la aplicación).</span><span class="sxs-lookup"><span data-stu-id="65214-127">App is calling on behalf of itself (application permission).</span></span><br/><span data-ttu-id="65214-128">- y -</span><span class="sxs-lookup"><span data-stu-id="65214-128">-and-</span></span><br/><span data-ttu-id="65214-129">Aplicación tiene el permiso original necesario para [crear la suscripción](subscription-post-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="65214-129">App has the original permission required to [create the subscription](subscription-post-subscriptions.md).</span></span><br/><br/><span data-ttu-id="65214-130">Nota: Esto se aplica sólo las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="65214-130">Note: This applies to work/school accounts only.</span></span>| <span data-ttu-id="65214-131">Suscripciones creadas por **esta aplicación** para sí o para cualquier usuario en el directorio.</span><span class="sxs-lookup"><span data-stu-id="65214-131">Subscriptions created by **this app** for itself or for any user in the directory.</span></span>|

### <a name="advanced-scenarios"></a><span data-ttu-id="65214-132">Escenarios avanzados</span><span class="sxs-lookup"><span data-stu-id="65214-132">Advanced scenarios</span></span>

<span data-ttu-id="65214-133">En algunos casos, una aplicación desea recuperar las suscripciones creadas por otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="65214-133">In some cases, an app wants to retrieve subscriptions created by other apps.</span></span> <span data-ttu-id="65214-134">Por ejemplo, un usuario desea ver todas las suscripciones creadas por cualquier aplicación en su nombre.</span><span class="sxs-lookup"><span data-stu-id="65214-134">For example, a user wants to see all subscriptions created by any app on their behalf.</span></span> <span data-ttu-id="65214-135">O bien, puede que un administrador desee ver todas las suscripciones de todas las aplicaciones en su directorio.</span><span class="sxs-lookup"><span data-stu-id="65214-135">Or, an administrator may want to see all subscriptions from all apps in their directory.</span></span>
<span data-ttu-id="65214-136">Para estos escenarios, se requiere un permiso delegado Subscription.Read.All.</span><span class="sxs-lookup"><span data-stu-id="65214-136">For such scenarios, a delegated permission Subscription.Read.All is required.</span></span>

| <span data-ttu-id="65214-137">Contexto de la aplicación que llama</span><span class="sxs-lookup"><span data-stu-id="65214-137">Context of the calling app</span></span> | <span data-ttu-id="65214-138">Contiene la respuesta</span><span class="sxs-lookup"><span data-stu-id="65214-138">Response contains</span></span> |
|:-----|:---------------- |
| <span data-ttu-id="65214-139">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="65214-139">App is calling on behalf of the signed-in user (delegated permission).</span></span> <span data-ttu-id="65214-140">*El usuario es un usuario sin permisos de administrador*.</span><span class="sxs-lookup"><span data-stu-id="65214-140">*The user is a non-admin*.</span></span> <br/><span data-ttu-id="65214-141">- y -</span><span class="sxs-lookup"><span data-stu-id="65214-141">-and-</span></span><br/><span data-ttu-id="65214-142">Aplicación tiene el permiso Subscription.Read.All</span><span class="sxs-lookup"><span data-stu-id="65214-142">App has the permission Subscription.Read.All</span></span><br/><br/><span data-ttu-id="65214-143">Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="65214-143">Note: This applies to both personal Microsoft accounts and work/school accounts.</span></span> | <span data-ttu-id="65214-144">Suscripciones creadas por **cualquier aplicación** para sólo el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="65214-144">Subscriptions created by **any app** for the signed-in user only.</span></span> |
| <span data-ttu-id="65214-145">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="65214-145">App is calling on behalf of the signed-in user (delegated permission).</span></span> <span data-ttu-id="65214-146">*El usuario es un administrador*.</span><span class="sxs-lookup"><span data-stu-id="65214-146">*The user is an admin*.</span></span><br/><span data-ttu-id="65214-147">- y -</span><span class="sxs-lookup"><span data-stu-id="65214-147">-and-</span></span><br/><span data-ttu-id="65214-148">Aplicación tiene el permiso Subscription.Read.All</span><span class="sxs-lookup"><span data-stu-id="65214-148">App has the permission Subscription.Read.All</span></span><br/><br/><span data-ttu-id="65214-149">Nota: Esto se aplica sólo las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="65214-149">Note: This applies to work/school accounts only.</span></span> | <span data-ttu-id="65214-150">Suscripciones creadas por **cualquier aplicación** para **cualquier usuario** en el directorio.</span><span class="sxs-lookup"><span data-stu-id="65214-150">Subscriptions created by **any app** for **any user** in the directory.</span></span>|

## <a name="http-request"></a><span data-ttu-id="65214-151">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65214-151">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions
```

## <a name="optional-query-parameters"></a><span data-ttu-id="65214-152">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="65214-152">Optional query parameters</span></span>

<span data-ttu-id="65214-153">Este método no es compatible con los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65214-153">This method does not support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="65214-154">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65214-154">Request headers</span></span>

| <span data-ttu-id="65214-155">Nombre</span><span class="sxs-lookup"><span data-stu-id="65214-155">Name</span></span>       | <span data-ttu-id="65214-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="65214-156">Type</span></span> | <span data-ttu-id="65214-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="65214-157">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="65214-158">Authorization</span><span class="sxs-lookup"><span data-stu-id="65214-158">Authorization</span></span>  | <span data-ttu-id="65214-159">string</span><span class="sxs-lookup"><span data-stu-id="65214-159">string</span></span>  | <span data-ttu-id="65214-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="65214-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="65214-162">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65214-162">Request body</span></span>

<span data-ttu-id="65214-163">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="65214-163">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="65214-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65214-164">Response</span></span>

<span data-ttu-id="65214-165">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65214-165">If successful, this method returns a `200 OK` response code and a list of [subscription](../resources/subscription.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="65214-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65214-166">Example</span></span>

##### <a name="request"></a><span data-ttu-id="65214-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65214-167">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_subscriptions"
}-->

```http
GET https://graph.microsoft.com/v1.0/subscriptions
```

##### <a name="response"></a><span data-ttu-id="65214-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65214-168">Response</span></span>

<span data-ttu-id="65214-169">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65214-169">Here's an an example of the response.</span></span>  <span data-ttu-id="65214-170">Tenga en cuenta que es posible que esté truncada por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="65214-170">Note that it may be truncated for brevity.</span></span>  <span data-ttu-id="65214-171">Todos los admiten propiedades adecuadas para la solicitud y se devolverá el contexto de la llamada de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65214-171">All supported properties appropriate for the request and the calling context will be returned from an actual call.</span></span>

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

<span data-ttu-id="65214-172">Cuando una solicitud devuelve varias páginas de datos, la respuesta incluye un `@odata.nextLink` (propiedad) que le ayudarán a administrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="65214-172">When a request returns multiple pages of data, the response includes an `@odata.nextLink` property to help you manage the results.</span></span>  <span data-ttu-id="65214-173">Para obtener más información, vea [datos de paginación Microsoft Graph en su aplicación](/graph/paging).</span><span class="sxs-lookup"><span data-stu-id="65214-173">To learn more, see [Paging Microsoft Graph data in your app](/graph/paging).</span></span>
