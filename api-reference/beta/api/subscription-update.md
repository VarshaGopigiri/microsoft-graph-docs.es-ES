---
title: Update subscription
description: Renueva una suscripción ampliando su tiempo de expiración.
ms.openlocfilehash: e2021e22d84ad9e05429db7980d37cbd1574843c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085074"
---
# <a name="update-subscription"></a><span data-ttu-id="1d861-103">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="1d861-103">Update subscription</span></span>

> <span data-ttu-id="1d861-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d861-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d861-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d861-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1d861-106">Renueva una suscripción ampliando su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="1d861-106">Renew a subscription by extending its expiry time.</span></span>

<span data-ttu-id="1d861-107">Las suscripciones caducan después de un período de tiempo que varía en función del tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="1d861-107">Subscriptions expire after a length of time that varies by resource type.</span></span> <span data-ttu-id="1d861-108">Con el fin de evitar la pérdida de notificaciones, una aplicación debe renovar sus suscripciones antes de su fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="1d861-108">In order to avoid missing notifications, an app should renew its subscriptions well in advance of their expiry date.</span></span> <span data-ttu-id="1d861-109">Vea la [suscripción](../resources/subscription.md) para la longitud máxima de una suscripción para cada tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="1d861-109">See [subscription](../resources/subscription.md) for maximum length of a subscription for each resource type.</span></span>

## <a name="permissions"></a><span data-ttu-id="1d861-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d861-110">Permissions</span></span>

<span data-ttu-id="1d861-p103">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d861-p103">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1d861-113">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="1d861-113">Resource type / Item</span></span>        | <span data-ttu-id="1d861-114">Permiso</span><span class="sxs-lookup"><span data-stu-id="1d861-114">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="1d861-115">Contactos</span><span class="sxs-lookup"><span data-stu-id="1d861-115">Contacts</span></span>                    | <span data-ttu-id="1d861-116">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="1d861-116">Contacts.Read</span></span>       |
| <span data-ttu-id="1d861-117">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="1d861-117">Conversations</span></span>               | <span data-ttu-id="1d861-118">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d861-118">Group.Read.All</span></span>      |
| <span data-ttu-id="1d861-119">Eventos</span><span class="sxs-lookup"><span data-stu-id="1d861-119">Events</span></span>                      | <span data-ttu-id="1d861-120">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="1d861-120">Calendars.Read</span></span>      |
| <span data-ttu-id="1d861-121">Mensajes</span><span class="sxs-lookup"><span data-stu-id="1d861-121">Messages</span></span>                    | <span data-ttu-id="1d861-122">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="1d861-122">Mail.Read</span></span>           |
| <span data-ttu-id="1d861-123">Groups</span><span class="sxs-lookup"><span data-stu-id="1d861-123">Groups</span></span>                      | <span data-ttu-id="1d861-124">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d861-124">Group.Read.All</span></span>      |
| <span data-ttu-id="1d861-125">Users</span><span class="sxs-lookup"><span data-stu-id="1d861-125">Users</span></span>                       | <span data-ttu-id="1d861-126">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d861-126">User.Read.All</span></span>       |
| <span data-ttu-id="1d861-127">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="1d861-127">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="1d861-128">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d861-128">Files.ReadWrite</span></span>     |
| <span data-ttu-id="1d861-129">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="1d861-129">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="1d861-130">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d861-130">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="1d861-131">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="1d861-131">Security alert</span></span>               | <span data-ttu-id="1d861-132">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d861-132">SecurityEvents.ReadWrite.All</span></span> |

<span data-ttu-id="1d861-133">***Nota:*** El extremo de /beta permite que los permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="1d861-133">***Note:*** The /beta endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="1d861-134">Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d861-134">Conversations in a Group and OneDrive drive root items are not supported with application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="1d861-135">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d861-135">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="1d861-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d861-136">Request headers</span></span>

| <span data-ttu-id="1d861-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="1d861-137">Name</span></span>       | <span data-ttu-id="1d861-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d861-138">Type</span></span> | <span data-ttu-id="1d861-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d861-139">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1d861-140">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d861-140">Authorization</span></span>  | <span data-ttu-id="1d861-141">string</span><span class="sxs-lookup"><span data-stu-id="1d861-141">string</span></span>  | <span data-ttu-id="1d861-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d861-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="1d861-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d861-144">Response</span></span>

<span data-ttu-id="1d861-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d861-145">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d861-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d861-146">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1d861-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d861-147">Request</span></span>

<span data-ttu-id="1d861-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d861-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_subscription"
}-->

```http
PATCH https://graph.microsoft.com/beta/subscriptions/{id}
Content-type: application/json

{
   "expirationDateTime":"2016-11-22T18:23:45.9356913Z"
}
```

##### <a name="response"></a><span data-ttu-id="1d861-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d861-149">Response</span></span>

<span data-ttu-id="1d861-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d861-150">Here is an example of the response.</span></span>
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
  "applicationId": "24d3b144-21ae-4080-943f-7067b395b913",
  "changeType":"created,updated",
  "clientState":"secretClientValue",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-22T18:23:45.9356913Z",
  "creatorId": "8ee44408-0679-472c-bc2a-692812af3437"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "Update subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
