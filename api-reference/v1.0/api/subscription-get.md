---
title: Get subscription
description: Recupera las propiedades y relaciones de una suscripción.
ms.openlocfilehash: 62bcb730a5743146113cda30d6dafa022afa4fc1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030051"
---
# <a name="get-subscription"></a><span data-ttu-id="6df93-103">Get subscription</span><span class="sxs-lookup"><span data-stu-id="6df93-103">Get subscription</span></span>

<span data-ttu-id="6df93-104">Recupera las propiedades y relaciones de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="6df93-104">Retrieve the properties and relationships of a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="6df93-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6df93-105">Permissions</span></span>

<span data-ttu-id="6df93-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6df93-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="6df93-108">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="6df93-108">Resource type / Item</span></span>        | <span data-ttu-id="6df93-109">Permiso</span><span class="sxs-lookup"><span data-stu-id="6df93-109">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="6df93-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="6df93-110">Contacts</span></span>                    | <span data-ttu-id="6df93-111">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="6df93-111">Contacts.Read</span></span>       |
| <span data-ttu-id="6df93-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="6df93-112">Conversations</span></span>               | <span data-ttu-id="6df93-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="6df93-113">Group.Read.All</span></span>      |
| <span data-ttu-id="6df93-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="6df93-114">Events</span></span>                      | <span data-ttu-id="6df93-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6df93-115">Calendars.Read</span></span>      |
| <span data-ttu-id="6df93-116">Mensajes</span><span class="sxs-lookup"><span data-stu-id="6df93-116">Messages</span></span>                    | <span data-ttu-id="6df93-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="6df93-117">Mail.Read</span></span>           |
| <span data-ttu-id="6df93-118">Groups</span><span class="sxs-lookup"><span data-stu-id="6df93-118">Groups</span></span>                      | <span data-ttu-id="6df93-119">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="6df93-119">Group.Read.All</span></span>      |
| <span data-ttu-id="6df93-120">Users</span><span class="sxs-lookup"><span data-stu-id="6df93-120">Users</span></span>                       | <span data-ttu-id="6df93-121">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="6df93-121">User.Read.All</span></span>       |
| <span data-ttu-id="6df93-122">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="6df93-122">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="6df93-123">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6df93-123">Files.ReadWrite</span></span>     |
| <span data-ttu-id="6df93-124">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="6df93-124">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="6df93-125">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6df93-125">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="6df93-126">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="6df93-126">Security alert</span></span>| <span data-ttu-id="6df93-127">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6df93-127">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6df93-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6df93-128">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6df93-129">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6df93-129">Optional query parameters</span></span>

<span data-ttu-id="6df93-130">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6df93-130">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6df93-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6df93-131">Request headers</span></span>

| <span data-ttu-id="6df93-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="6df93-132">Name</span></span>       | <span data-ttu-id="6df93-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="6df93-133">Type</span></span> | <span data-ttu-id="6df93-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="6df93-134">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6df93-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="6df93-135">Authorization</span></span>  | <span data-ttu-id="6df93-136">string</span><span class="sxs-lookup"><span data-stu-id="6df93-136">string</span></span>  | <span data-ttu-id="6df93-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6df93-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6df93-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6df93-139">Request body</span></span>

<span data-ttu-id="6df93-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6df93-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6df93-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6df93-141">Response</span></span>

<span data-ttu-id="6df93-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6df93-142">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6df93-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6df93-143">Example</span></span>

##### <a name="request"></a><span data-ttu-id="6df93-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6df93-144">Request</span></span>

<span data-ttu-id="6df93-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6df93-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->

```http
GET https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="6df93-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6df93-146">Response</span></span>

<span data-ttu-id="6df93-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6df93-147">Here is an example of the response.</span></span>
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
