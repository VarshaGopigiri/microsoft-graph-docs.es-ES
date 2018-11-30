---
title: Delete subscription
description: Elimina una suscripción.
ms.openlocfilehash: be2c32f0915e8718203e46489be9861bf0f05451
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084734"
---
# <a name="delete-subscription"></a><span data-ttu-id="e0d6c-103">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="e0d6c-103">Delete subscription</span></span>

> <span data-ttu-id="e0d6c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e0d6c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e0d6c-106">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-106">Delete a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="e0d6c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e0d6c-107">Permissions</span></span>

<span data-ttu-id="e0d6c-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e0d6c-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e0d6c-110">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="e0d6c-110">Resource type / Item</span></span>        | <span data-ttu-id="e0d6c-111">Permiso</span><span class="sxs-lookup"><span data-stu-id="e0d6c-111">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="e0d6c-112">Contactos</span><span class="sxs-lookup"><span data-stu-id="e0d6c-112">Contacts</span></span>                    | <span data-ttu-id="e0d6c-113">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="e0d6c-113">Contacts.Read</span></span>       |
| <span data-ttu-id="e0d6c-114">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="e0d6c-114">Conversations</span></span>               | <span data-ttu-id="e0d6c-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="e0d6c-115">Group.Read.All</span></span>      |
| <span data-ttu-id="e0d6c-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="e0d6c-116">Events</span></span>                      | <span data-ttu-id="e0d6c-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e0d6c-117">Calendars.Read</span></span>      |
| <span data-ttu-id="e0d6c-118">Mensajes</span><span class="sxs-lookup"><span data-stu-id="e0d6c-118">Messages</span></span>                    | <span data-ttu-id="e0d6c-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e0d6c-119">Mail.Read</span></span>           |
| <span data-ttu-id="e0d6c-120">Groups</span><span class="sxs-lookup"><span data-stu-id="e0d6c-120">Groups</span></span>                      | <span data-ttu-id="e0d6c-121">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="e0d6c-121">Group.Read.All</span></span>      |
| <span data-ttu-id="e0d6c-122">Users</span><span class="sxs-lookup"><span data-stu-id="e0d6c-122">Users</span></span>                       | <span data-ttu-id="e0d6c-123">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="e0d6c-123">User.Read.All</span></span>       |
| <span data-ttu-id="e0d6c-124">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="e0d6c-124">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="e0d6c-125">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e0d6c-125">Files.ReadWrite</span></span>     |
| <span data-ttu-id="e0d6c-126">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="e0d6c-126">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="e0d6c-127">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0d6c-127">Files.ReadWrite.All</span></span> |
| <span data-ttu-id="e0d6c-128">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="e0d6c-128">Security alert</span></span>              | <span data-ttu-id="e0d6c-129">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0d6c-129">SecurityEvents.ReadWrite.All</span></span> |

<span data-ttu-id="e0d6c-130">***Nota:*** El extremo de /beta permite que los permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-130">***Note:*** The /beta endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="e0d6c-131">Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-131">Conversations in a Group and OneDrive drive root items are not supported with application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="e0d6c-132">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e0d6c-132">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="e0d6c-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d6c-133">Request headers</span></span>

| <span data-ttu-id="e0d6c-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0d6c-134">Name</span></span>       | <span data-ttu-id="e0d6c-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0d6c-135">Type</span></span> | <span data-ttu-id="e0d6c-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0d6c-136">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e0d6c-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="e0d6c-137">Authorization</span></span>  | <span data-ttu-id="e0d6c-138">string</span><span class="sxs-lookup"><span data-stu-id="e0d6c-138">string</span></span>  | <span data-ttu-id="e0d6c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e0d6c-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d6c-141">Request body</span></span>

<span data-ttu-id="e0d6c-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e0d6c-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0d6c-143">Response</span></span>

<span data-ttu-id="e0d6c-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-144">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="e0d6c-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0d6c-145">Example</span></span>

##### <a name="request"></a><span data-ttu-id="e0d6c-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d6c-146">Request</span></span>

<span data-ttu-id="e0d6c-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/beta/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="e0d6c-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0d6c-148">Response</span></span>

<span data-ttu-id="e0d6c-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0d6c-149">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Delete subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
