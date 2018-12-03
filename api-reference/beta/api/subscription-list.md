---
title: Suscripciones de lista
description: " Consulte los escenarios a continuación para obtener información detallada."
ms.openlocfilehash: ad5e97a9b721a9e557e01dd4743b53a52c6dc8d7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090077"
---
# <a name="list-subscriptions"></a><span data-ttu-id="98c39-103">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="98c39-103">List subscriptions</span></span>

> <span data-ttu-id="98c39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="98c39-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="98c39-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="98c39-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="98c39-106">Recuperar una lista de las suscripciones de webhook.</span><span class="sxs-lookup"><span data-stu-id="98c39-106">Retrieve a list of webhook subscriptions.</span></span> <span data-ttu-id="98c39-107">El contenido de la respuesta depende del contexto en el que está llamando la aplicación; Consulte los escenarios a continuación para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="98c39-107">The content of the response depends on the context in which the app is calling; see the scenarios below for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="98c39-108">Permissions</span><span class="sxs-lookup"><span data-stu-id="98c39-108">Permissions</span></span>

<span data-ttu-id="98c39-109">Esta API admite los siguientes ámbitos de permisos; Para obtener más información, incluido cómo elegir permisos, vea [permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98c39-109">This API supports the following permission scopes; to learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="98c39-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98c39-110">Permission type</span></span>  | <span data-ttu-id="98c39-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98c39-111">Permissions (from least to most privileged)</span></span>  |
|:---------------- |:-------------------------------------------- |
| <span data-ttu-id="98c39-112">[Delegada](/graph/auth-v2-user) (cuenta de trabajo o escuela)</span><span class="sxs-lookup"><span data-stu-id="98c39-112">[Delegated](/graph/auth-v2-user) (work or school account)</span></span> | <span data-ttu-id="98c39-113">Permisos necesarios para [crear la suscripción](subscription-post-subscriptions.md) o Subscription.Read.All (vea a continuación).</span><span class="sxs-lookup"><span data-stu-id="98c39-113">Permission required to [create subscription](subscription-post-subscriptions.md) or Subscription.Read.All (see below).</span></span> |
| <span data-ttu-id="98c39-114">[Delegada](/graph/auth-v2-user) (cuenta Microsoft personal)</span><span class="sxs-lookup"><span data-stu-id="98c39-114">[Delegated](/graph/auth-v2-user) (personal Microsoft account)</span></span> | <span data-ttu-id="98c39-115">Permisos necesarios para [crear la suscripción](subscription-post-subscriptions.md) o Subscription.Read.All (vea a continuación).</span><span class="sxs-lookup"><span data-stu-id="98c39-115">Permission required to [create subscription](subscription-post-subscriptions.md) or Subscription.Read.All (see below).</span></span> |
| [<span data-ttu-id="98c39-116">Application</span><span class="sxs-lookup"><span data-stu-id="98c39-116">Application</span></span>](/graph/auth-v2-service) | <span data-ttu-id="98c39-117">Permisos necesarios para [crear la suscripción](subscription-post-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="98c39-117">Permission required to [create subscription](subscription-post-subscriptions.md).</span></span> |

<span data-ttu-id="98c39-118">Los resultados de la respuesta se basan en el contexto de la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="98c39-118">Response results are based on the context of the calling app.</span></span> <span data-ttu-id="98c39-119">El siguiente es un resumen de los escenarios comunes:</span><span class="sxs-lookup"><span data-stu-id="98c39-119">The following is a summary of the common scenarios:</span></span>

### <a name="basic-scenarios"></a><span data-ttu-id="98c39-120">Escenarios básicos</span><span class="sxs-lookup"><span data-stu-id="98c39-120">Basic scenarios</span></span>

<span data-ttu-id="98c39-121">Con más frecuencia, una aplicación desea recuperar las suscripciones que creó originalmente para el usuario que ha iniciado la sesión actual, o para todos los usuarios en el directorio (las cuentas de trabajo o escuela).</span><span class="sxs-lookup"><span data-stu-id="98c39-121">Most commonly, an application wants to retrieve subscriptions that it originally created for the currently signed-in user, or for all users in the directory (work/school accounts).</span></span> <span data-ttu-id="98c39-122">Estos escenarios no requieren ningún permiso especial más allá de los que la aplicación que se usó originalmente para crear sus suscripciones.</span><span class="sxs-lookup"><span data-stu-id="98c39-122">These scenarios do not require any special permissions beyond the ones the app used originally to create its subscriptions.</span></span>

| <span data-ttu-id="98c39-123">Contexto de la aplicación que llama</span><span class="sxs-lookup"><span data-stu-id="98c39-123">Context of the calling app</span></span> | <span data-ttu-id="98c39-124">Contiene la respuesta</span><span class="sxs-lookup"><span data-stu-id="98c39-124">Response contains</span></span> |
|:-----|:---------------- |
| <span data-ttu-id="98c39-125">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="98c39-125">App is calling on behalf of the signed-in user (delegated permission).</span></span> <br/><span data-ttu-id="98c39-126">- y -</span><span class="sxs-lookup"><span data-stu-id="98c39-126">-and-</span></span><br/><span data-ttu-id="98c39-127">Aplicación tiene el permiso original necesario para [crear la suscripción](subscription-post-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="98c39-127">App has the original permission required to [create the subscription](subscription-post-subscriptions.md).</span></span><br/><br/><span data-ttu-id="98c39-128">Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="98c39-128">Note: This applies to both personal Microsoft accounts and work/school accounts.</span></span> | <span data-ttu-id="98c39-129">Suscripciones creadas por **esta aplicación** para sólo el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="98c39-129">Subscriptions created by **this app** for the signed-in user only.</span></span> |
| <span data-ttu-id="98c39-130">Aplicación está llamando en nombre propio (permiso a la aplicación).</span><span class="sxs-lookup"><span data-stu-id="98c39-130">App is calling on behalf of itself (application permission).</span></span><br/><span data-ttu-id="98c39-131">- y -</span><span class="sxs-lookup"><span data-stu-id="98c39-131">-and-</span></span><br/><span data-ttu-id="98c39-132">Aplicación tiene el permiso original necesario para [crear la suscripción](subscription-post-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="98c39-132">App has the original permission required to [create the subscription](subscription-post-subscriptions.md).</span></span><br/><br/><span data-ttu-id="98c39-133">Nota: Esto se aplica sólo las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="98c39-133">Note: This applies to work/school accounts only.</span></span>| <span data-ttu-id="98c39-134">Suscripciones creadas por **esta aplicación** para sí o para cualquier usuario en el directorio.</span><span class="sxs-lookup"><span data-stu-id="98c39-134">Subscriptions created by **this app** for itself or for any user in the directory.</span></span>|

### <a name="advanced-scenarios"></a><span data-ttu-id="98c39-135">Escenarios avanzados</span><span class="sxs-lookup"><span data-stu-id="98c39-135">Advanced scenarios</span></span>

<span data-ttu-id="98c39-136">En algunos casos, una aplicación desea recuperar las suscripciones creadas por otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="98c39-136">In some cases, an app wants to retrieve subscriptions created by other apps.</span></span> <span data-ttu-id="98c39-137">Por ejemplo, un usuario desea ver todas las suscripciones creadas por cualquier aplicación en su nombre.</span><span class="sxs-lookup"><span data-stu-id="98c39-137">For example, a user wants to see all subscriptions created by any app on their behalf.</span></span> <span data-ttu-id="98c39-138">O bien, puede que un administrador desee ver todas las suscripciones de todas las aplicaciones en su directorio.</span><span class="sxs-lookup"><span data-stu-id="98c39-138">Or, an administrator may want to see all subscriptions from all apps in their directory.</span></span>
<span data-ttu-id="98c39-139">Para estos escenarios, se requiere un permiso delegado Subscription.Read.All.</span><span class="sxs-lookup"><span data-stu-id="98c39-139">For such scenarios, a delegated permission Subscription.Read.All is required.</span></span>

| <span data-ttu-id="98c39-140">Contexto de la aplicación que llama</span><span class="sxs-lookup"><span data-stu-id="98c39-140">Context of the calling app</span></span> | <span data-ttu-id="98c39-141">Contiene la respuesta</span><span class="sxs-lookup"><span data-stu-id="98c39-141">Response contains</span></span> |
|:-----|:---------------- |
| <span data-ttu-id="98c39-142">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="98c39-142">App is calling on behalf of the signed-in user (delegated permission).</span></span> <span data-ttu-id="98c39-143">*El usuario es un usuario sin permisos de administrador*.</span><span class="sxs-lookup"><span data-stu-id="98c39-143">*The user is a non-admin*.</span></span> <br/><span data-ttu-id="98c39-144">- y -</span><span class="sxs-lookup"><span data-stu-id="98c39-144">-and-</span></span><br/><span data-ttu-id="98c39-145">Aplicación tiene el permiso Subscription.Read.All</span><span class="sxs-lookup"><span data-stu-id="98c39-145">App has the permission Subscription.Read.All</span></span><br/><br/><span data-ttu-id="98c39-146">Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="98c39-146">Note: This applies to both personal Microsoft accounts and work/school accounts.</span></span> | <span data-ttu-id="98c39-147">Suscripciones creadas por **cualquier aplicación** para sólo el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="98c39-147">Subscriptions created by **any app** for the signed-in user only.</span></span> |
| <span data-ttu-id="98c39-148">Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos).</span><span class="sxs-lookup"><span data-stu-id="98c39-148">App is calling on behalf of the signed-in user (delegated permission).</span></span> <span data-ttu-id="98c39-149">*El usuario es un administrador*.</span><span class="sxs-lookup"><span data-stu-id="98c39-149">*The user is an admin*.</span></span><br/><span data-ttu-id="98c39-150">- y -</span><span class="sxs-lookup"><span data-stu-id="98c39-150">-and-</span></span><br/><span data-ttu-id="98c39-151">Aplicación tiene el permiso Subscription.Read.All</span><span class="sxs-lookup"><span data-stu-id="98c39-151">App has the permission Subscription.Read.All</span></span><br/><br/><span data-ttu-id="98c39-152">Nota: Esto se aplica sólo las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="98c39-152">Note: This applies to work/school accounts only.</span></span> | <span data-ttu-id="98c39-153">Suscripciones creadas por **cualquier aplicación** para **cualquier usuario** en el directorio.</span><span class="sxs-lookup"><span data-stu-id="98c39-153">Subscriptions created by **any app** for **any user** in the directory.</span></span>|

## <a name="http-request"></a><span data-ttu-id="98c39-154">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98c39-154">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions
```

## <a name="optional-query-parameters"></a><span data-ttu-id="98c39-155">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="98c39-155">Optional query parameters</span></span>

<span data-ttu-id="98c39-156">Este método no es compatible con los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98c39-156">This method does not support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="98c39-157">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98c39-157">Request headers</span></span>

| <span data-ttu-id="98c39-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="98c39-158">Name</span></span>       | <span data-ttu-id="98c39-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="98c39-159">Type</span></span> | <span data-ttu-id="98c39-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="98c39-160">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="98c39-161">Authorization</span><span class="sxs-lookup"><span data-stu-id="98c39-161">Authorization</span></span>  | <span data-ttu-id="98c39-162">string</span><span class="sxs-lookup"><span data-stu-id="98c39-162">string</span></span>  | <span data-ttu-id="98c39-p108">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98c39-p108">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="98c39-165">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98c39-165">Request body</span></span>

<span data-ttu-id="98c39-166">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="98c39-166">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="98c39-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98c39-167">Response</span></span>

<span data-ttu-id="98c39-168">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98c39-168">If successful, this method returns a `200 OK` response code and a list of [subscription](../resources/subscription.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98c39-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98c39-169">Example</span></span>

##### <a name="request"></a><span data-ttu-id="98c39-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98c39-170">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_subscriptions"
}-->

```http
GET https://graph.microsoft.com/beta/subscriptions
```

##### <a name="response"></a><span data-ttu-id="98c39-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98c39-171">Response</span></span>

<span data-ttu-id="98c39-172">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98c39-172">Here is an example of the response.</span></span> <span data-ttu-id="98c39-173">Nota: Es posible que se trunca la respuesta que se muestra aquí por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="98c39-173">Note: The response shown here may be truncated for brevity.</span></span> <span data-ttu-id="98c39-174">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98c39-174">All of the properties will be returned from an actual call.</span></span>

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
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#subscriptions",
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

<span data-ttu-id="98c39-175">Cuando una solicitud devuelve varias páginas de datos, la respuesta incluye un `@odata.nextLink` (propiedad) que le ayudarán a administrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="98c39-175">When a request returns multiple pages of data, the response includes an `@odata.nextLink` property to help you manage the results.</span></span>  <span data-ttu-id="98c39-176">Para obtener más información, vea [datos de paginación Microsoft Graph en su aplicación](/graph/paging).</span><span class="sxs-lookup"><span data-stu-id="98c39-176">To learn more, see [Paging Microsoft Graph data in your app](/graph/paging).</span></span>