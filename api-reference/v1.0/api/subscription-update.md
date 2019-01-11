---
title: Update subscription
description: Renueva una suscripción ampliando su tiempo de expiración.
localization_priority: Normal
ms.openlocfilehash: f0804421c2e178d176975317ba82bb0aac0ae212
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809719"
---
# <a name="update-subscription"></a><span data-ttu-id="c43df-103">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="c43df-103">Update subscription</span></span>

<span data-ttu-id="c43df-104">Renueva una suscripción ampliando su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="c43df-104">Renew a subscription by extending its expiry time.</span></span>

<span data-ttu-id="c43df-105">Las suscripciones caducan después de un período de tiempo que varía en función del tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c43df-105">Subscriptions expire after a length of time that varies by resource type.</span></span> <span data-ttu-id="c43df-106">Con el fin de evitar la pérdida de notificaciones, una aplicación debe renovar sus suscripciones antes de su fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="c43df-106">In order to avoid missing notifications, an app should renew its subscriptions well in advance of their expiry date.</span></span> <span data-ttu-id="c43df-107">Vea la [suscripción](../resources/subscription.md) para la longitud máxima de una suscripción para cada tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c43df-107">See [subscription](../resources/subscription.md) for maximum length of a subscription for each resource type.</span></span>

## <a name="permissions"></a><span data-ttu-id="c43df-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c43df-108">Permissions</span></span>

<span data-ttu-id="c43df-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c43df-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c43df-111">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="c43df-111">Resource type / Item</span></span>        | <span data-ttu-id="c43df-112">Permiso</span><span class="sxs-lookup"><span data-stu-id="c43df-112">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="c43df-113">Contactos</span><span class="sxs-lookup"><span data-stu-id="c43df-113">Contacts</span></span>                    | <span data-ttu-id="c43df-114">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="c43df-114">Contacts.Read</span></span>       |
| <span data-ttu-id="c43df-115">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="c43df-115">Conversations</span></span>               | <span data-ttu-id="c43df-116">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="c43df-116">Group.Read.All</span></span>      |
| <span data-ttu-id="c43df-117">Eventos</span><span class="sxs-lookup"><span data-stu-id="c43df-117">Events</span></span>                      | <span data-ttu-id="c43df-118">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c43df-118">Calendars.Read</span></span>      |
| <span data-ttu-id="c43df-119">Mensajes</span><span class="sxs-lookup"><span data-stu-id="c43df-119">Messages</span></span>                    | <span data-ttu-id="c43df-120">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="c43df-120">Mail.Read</span></span>           |
| <span data-ttu-id="c43df-121">Grupos</span><span class="sxs-lookup"><span data-stu-id="c43df-121">Groups</span></span>                      | <span data-ttu-id="c43df-122">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="c43df-122">Group.Read.All</span></span>      |
| <span data-ttu-id="c43df-123">Usuarios</span><span class="sxs-lookup"><span data-stu-id="c43df-123">Users</span></span>                       | <span data-ttu-id="c43df-124">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="c43df-124">User.Read.All</span></span>       |
| <span data-ttu-id="c43df-125">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="c43df-125">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="c43df-126">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c43df-126">Files.ReadWrite</span></span>     |
| <span data-ttu-id="c43df-127">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="c43df-127">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="c43df-128">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c43df-128">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="c43df-129">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="c43df-129">Security alert</span></span>| <span data-ttu-id="c43df-130">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c43df-130">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c43df-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c43df-131">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="c43df-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c43df-132">Request headers</span></span>

| <span data-ttu-id="c43df-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="c43df-133">Name</span></span>       | <span data-ttu-id="c43df-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="c43df-134">Type</span></span> | <span data-ttu-id="c43df-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="c43df-135">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c43df-136">Autorización</span><span class="sxs-lookup"><span data-stu-id="c43df-136">Authorization</span></span>  | <span data-ttu-id="c43df-137">string</span><span class="sxs-lookup"><span data-stu-id="c43df-137">string</span></span>  | <span data-ttu-id="c43df-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c43df-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="c43df-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c43df-140">Response</span></span>

<span data-ttu-id="c43df-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c43df-141">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c43df-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c43df-142">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c43df-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c43df-143">Request</span></span>

<span data-ttu-id="c43df-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c43df-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_subscription"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id}
Content-type: application/json

{
   "expirationDateTime":"2016-11-22T18:23:45.9356913Z"
}
```

##### <a name="response"></a><span data-ttu-id="c43df-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c43df-145">Response</span></span>

<span data-ttu-id="c43df-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c43df-146">Here is an example of the response.</span></span>
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
  "clientState":"subscription-identifier",
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
