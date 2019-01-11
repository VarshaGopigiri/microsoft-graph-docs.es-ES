---
title: Get subscription
description: Recupera las propiedades y relaciones de una suscripción.
localization_priority: Normal
ms.openlocfilehash: 0feb4ffd49099eabb92e5519b25233100f2acbe5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846840"
---
# <a name="get-subscription"></a><span data-ttu-id="98b03-103">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="98b03-103">Get subscription</span></span>

> <span data-ttu-id="98b03-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="98b03-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="98b03-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="98b03-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="98b03-106">Recupera las propiedades y relaciones de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="98b03-106">Retrieve the properties and relationships of a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="98b03-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="98b03-107">Permissions</span></span>

<span data-ttu-id="98b03-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98b03-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="98b03-110">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="98b03-110">Resource type / Item</span></span>        | <span data-ttu-id="98b03-111">Permiso</span><span class="sxs-lookup"><span data-stu-id="98b03-111">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="98b03-112">Contactos</span><span class="sxs-lookup"><span data-stu-id="98b03-112">Contacts</span></span>                    | <span data-ttu-id="98b03-113">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="98b03-113">Contacts.Read</span></span>       |
| <span data-ttu-id="98b03-114">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="98b03-114">Conversations</span></span>               | <span data-ttu-id="98b03-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="98b03-115">Group.Read.All</span></span>      |
| <span data-ttu-id="98b03-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="98b03-116">Events</span></span>                      | <span data-ttu-id="98b03-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="98b03-117">Calendars.Read</span></span>      |
| <span data-ttu-id="98b03-118">Mensajes</span><span class="sxs-lookup"><span data-stu-id="98b03-118">Messages</span></span>                    | <span data-ttu-id="98b03-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="98b03-119">Mail.Read</span></span>           |
| <span data-ttu-id="98b03-120">Grupos</span><span class="sxs-lookup"><span data-stu-id="98b03-120">Groups</span></span>                      | <span data-ttu-id="98b03-121">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="98b03-121">Group.Read.All</span></span>      |
| <span data-ttu-id="98b03-122">Usuarios</span><span class="sxs-lookup"><span data-stu-id="98b03-122">Users</span></span>                       | <span data-ttu-id="98b03-123">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="98b03-123">User.Read.All</span></span>       |
| <span data-ttu-id="98b03-124">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="98b03-124">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="98b03-125">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="98b03-125">Files.ReadWrite</span></span>     |
| <span data-ttu-id="98b03-126">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="98b03-126">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="98b03-127">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98b03-127">Files.ReadWrite.All</span></span> |
| <span data-ttu-id="98b03-128">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="98b03-128">Security alert</span></span>              | <span data-ttu-id="98b03-129">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98b03-129">SecurityEvents.ReadWrite.All</span></span> |

<span data-ttu-id="98b03-130">***Nota:*** El extremo de /beta permite que los permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="98b03-130">***Note:*** The /beta endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="98b03-131">Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98b03-131">Conversations in a Group and OneDrive drive root items are not supported with application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="98b03-132">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98b03-132">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="98b03-133">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="98b03-133">Optional query parameters</span></span>

<span data-ttu-id="98b03-134">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98b03-134">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="98b03-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98b03-135">Request headers</span></span>

| <span data-ttu-id="98b03-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="98b03-136">Name</span></span>       | <span data-ttu-id="98b03-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="98b03-137">Type</span></span> | <span data-ttu-id="98b03-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="98b03-138">Description</span></span>|
|:-----------|:-----|:-----------|
| <span data-ttu-id="98b03-139">Autorización</span><span class="sxs-lookup"><span data-stu-id="98b03-139">Authorization</span></span>  | <span data-ttu-id="98b03-140">string</span><span class="sxs-lookup"><span data-stu-id="98b03-140">string</span></span>  | <span data-ttu-id="98b03-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98b03-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="98b03-143">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98b03-143">Request body</span></span>

<span data-ttu-id="98b03-144">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="98b03-144">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="98b03-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98b03-145">Response</span></span>

<span data-ttu-id="98b03-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98b03-146">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98b03-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98b03-147">Example</span></span>

##### <a name="request"></a><span data-ttu-id="98b03-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98b03-148">Request</span></span>

<span data-ttu-id="98b03-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98b03-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->

```http
GET https://graph.microsoft.com/beta/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="98b03-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98b03-150">Response</span></span>

<span data-ttu-id="98b03-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98b03-151">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 252

{
  "id":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource":"me/messages",
  "applicationId" : "string",
  "changeType":"created,updated",
  "clientState":"secretClientValue",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-20T18:23:45.9356913Z",
  "creatorId": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
