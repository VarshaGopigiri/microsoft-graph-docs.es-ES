---
title: Get subscription
description: Recupera las propiedades y relaciones de una suscripción.
localization_priority: Priority
ms.openlocfilehash: a9cdc93d958895deaeb8778b69651a898d5a94c2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840302"
---
# <a name="get-subscription"></a><span data-ttu-id="1359d-103">Get subscription</span><span class="sxs-lookup"><span data-stu-id="1359d-103">Get subscription</span></span>

<span data-ttu-id="1359d-104">Recupera las propiedades y relaciones de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="1359d-104">Retrieve the properties and relationships of a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="1359d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1359d-105">Permissions</span></span>

<span data-ttu-id="1359d-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1359d-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1359d-108">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="1359d-108">Resource type / Item</span></span>        | <span data-ttu-id="1359d-109">Permiso</span><span class="sxs-lookup"><span data-stu-id="1359d-109">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="1359d-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="1359d-110">Contacts</span></span>                    | <span data-ttu-id="1359d-111">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="1359d-111">Contacts.Read</span></span>       |
| <span data-ttu-id="1359d-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="1359d-112">Conversations</span></span>               | <span data-ttu-id="1359d-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="1359d-113">Group.Read.All</span></span>      |
| <span data-ttu-id="1359d-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="1359d-114">Events</span></span>                      | <span data-ttu-id="1359d-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="1359d-115">Calendars.Read</span></span>      |
| <span data-ttu-id="1359d-116">Mensajes</span><span class="sxs-lookup"><span data-stu-id="1359d-116">Messages</span></span>                    | <span data-ttu-id="1359d-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="1359d-117">Mail.Read</span></span>           |
| <span data-ttu-id="1359d-118">Grupos</span><span class="sxs-lookup"><span data-stu-id="1359d-118">Groups</span></span>                      | <span data-ttu-id="1359d-119">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="1359d-119">Group.Read.All</span></span>      |
| <span data-ttu-id="1359d-120">Usuarios</span><span class="sxs-lookup"><span data-stu-id="1359d-120">Users</span></span>                       | <span data-ttu-id="1359d-121">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="1359d-121">User.Read.All</span></span>       |
| <span data-ttu-id="1359d-122">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="1359d-122">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="1359d-123">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1359d-123">Files.ReadWrite</span></span>     |
| <span data-ttu-id="1359d-124">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="1359d-124">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="1359d-125">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1359d-125">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="1359d-126">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="1359d-126">Security alert</span></span>| <span data-ttu-id="1359d-127">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1359d-127">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1359d-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1359d-128">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1359d-129">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1359d-129">Optional query parameters</span></span>

<span data-ttu-id="1359d-130">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1359d-130">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1359d-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1359d-131">Request headers</span></span>

| <span data-ttu-id="1359d-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="1359d-132">Name</span></span>       | <span data-ttu-id="1359d-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="1359d-133">Type</span></span> | <span data-ttu-id="1359d-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="1359d-134">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1359d-135">Autorización</span><span class="sxs-lookup"><span data-stu-id="1359d-135">Authorization</span></span>  | <span data-ttu-id="1359d-136">string</span><span class="sxs-lookup"><span data-stu-id="1359d-136">string</span></span>  | <span data-ttu-id="1359d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1359d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1359d-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1359d-139">Request body</span></span>

<span data-ttu-id="1359d-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1359d-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1359d-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1359d-141">Response</span></span>

<span data-ttu-id="1359d-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1359d-142">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1359d-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1359d-143">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1359d-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1359d-144">Request</span></span>

<span data-ttu-id="1359d-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1359d-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->

```http
GET https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="1359d-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1359d-146">Response</span></span>

<span data-ttu-id="1359d-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1359d-147">Here is an example of the response.</span></span>
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
