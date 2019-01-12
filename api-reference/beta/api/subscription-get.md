---
title: Get subscription
description: Recupera las propiedades y relaciones de una suscripción.
localization_priority: Normal
author: piotrci
ms.openlocfilehash: 165fd990d7dbec64eb61b9e06d05b51b40bf1212
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934887"
---
# <a name="get-subscription"></a><span data-ttu-id="3b721-103">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="3b721-103">Get subscription</span></span>

> <span data-ttu-id="3b721-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b721-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b721-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b721-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b721-106">Recupera las propiedades y relaciones de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="3b721-106">Retrieve the properties and relationships of a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="3b721-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3b721-107">Permissions</span></span>

<span data-ttu-id="3b721-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b721-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3b721-110">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="3b721-110">Resource type / Item</span></span>        | <span data-ttu-id="3b721-111">Permiso</span><span class="sxs-lookup"><span data-stu-id="3b721-111">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="3b721-112">Contactos</span><span class="sxs-lookup"><span data-stu-id="3b721-112">Contacts</span></span>                    | <span data-ttu-id="3b721-113">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="3b721-113">Contacts.Read</span></span>       |
| <span data-ttu-id="3b721-114">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="3b721-114">Conversations</span></span>               | <span data-ttu-id="3b721-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="3b721-115">Group.Read.All</span></span>      |
| <span data-ttu-id="3b721-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="3b721-116">Events</span></span>                      | <span data-ttu-id="3b721-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="3b721-117">Calendars.Read</span></span>      |
| <span data-ttu-id="3b721-118">Mensajes</span><span class="sxs-lookup"><span data-stu-id="3b721-118">Messages</span></span>                    | <span data-ttu-id="3b721-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="3b721-119">Mail.Read</span></span>           |
| <span data-ttu-id="3b721-120">Grupos</span><span class="sxs-lookup"><span data-stu-id="3b721-120">Groups</span></span>                      | <span data-ttu-id="3b721-121">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="3b721-121">Group.Read.All</span></span>      |
| <span data-ttu-id="3b721-122">Usuarios</span><span class="sxs-lookup"><span data-stu-id="3b721-122">Users</span></span>                       | <span data-ttu-id="3b721-123">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="3b721-123">User.Read.All</span></span>       |
| <span data-ttu-id="3b721-124">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="3b721-124">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="3b721-125">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3b721-125">Files.ReadWrite</span></span>     |
| <span data-ttu-id="3b721-126">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="3b721-126">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="3b721-127">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b721-127">Files.ReadWrite.All</span></span> |
| <span data-ttu-id="3b721-128">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="3b721-128">Security alert</span></span>              | <span data-ttu-id="3b721-129">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b721-129">SecurityEvents.ReadWrite.All</span></span> |

<span data-ttu-id="3b721-130">***Nota:*** El extremo de /beta permite que los permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="3b721-130">***Note:*** The /beta endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="3b721-131">Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b721-131">Conversations in a Group and OneDrive drive root items are not supported with application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="3b721-132">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b721-132">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3b721-133">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3b721-133">Optional query parameters</span></span>

<span data-ttu-id="3b721-134">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b721-134">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3b721-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b721-135">Request headers</span></span>

| <span data-ttu-id="3b721-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="3b721-136">Name</span></span>       | <span data-ttu-id="3b721-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b721-137">Type</span></span> | <span data-ttu-id="3b721-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b721-138">Description</span></span>|
|:-----------|:-----|:-----------|
| <span data-ttu-id="3b721-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="3b721-139">Authorization</span></span>  | <span data-ttu-id="3b721-140">string</span><span class="sxs-lookup"><span data-stu-id="3b721-140">string</span></span>  | <span data-ttu-id="3b721-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b721-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3b721-143">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b721-143">Request body</span></span>

<span data-ttu-id="3b721-144">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3b721-144">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3b721-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b721-145">Response</span></span>

<span data-ttu-id="3b721-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b721-146">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3b721-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b721-147">Example</span></span>

##### <a name="request"></a><span data-ttu-id="3b721-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b721-148">Request</span></span>

<span data-ttu-id="3b721-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b721-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->

```http
GET https://graph.microsoft.com/beta/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="3b721-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b721-150">Response</span></span>

<span data-ttu-id="3b721-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b721-151">Here is an example of the response.</span></span>
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
