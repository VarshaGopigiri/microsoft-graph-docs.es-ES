---
title: Delete subscription
description: Elimina una suscripción.
localization_priority: Normal
ms.openlocfilehash: 1e2efb9835e5e625bdac0385b5011cfe5c8c64b5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842052"
---
# <a name="delete-subscription"></a><span data-ttu-id="ef099-103">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="ef099-103">Delete subscription</span></span>

> <span data-ttu-id="ef099-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ef099-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ef099-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ef099-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ef099-106">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="ef099-106">Delete a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="ef099-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ef099-107">Permissions</span></span>

<span data-ttu-id="ef099-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef099-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ef099-110">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="ef099-110">Resource type / Item</span></span>        | <span data-ttu-id="ef099-111">Permiso</span><span class="sxs-lookup"><span data-stu-id="ef099-111">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="ef099-112">Contactos</span><span class="sxs-lookup"><span data-stu-id="ef099-112">Contacts</span></span>                    | <span data-ttu-id="ef099-113">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="ef099-113">Contacts.Read</span></span>       |
| <span data-ttu-id="ef099-114">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="ef099-114">Conversations</span></span>               | <span data-ttu-id="ef099-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="ef099-115">Group.Read.All</span></span>      |
| <span data-ttu-id="ef099-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="ef099-116">Events</span></span>                      | <span data-ttu-id="ef099-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="ef099-117">Calendars.Read</span></span>      |
| <span data-ttu-id="ef099-118">Mensajes</span><span class="sxs-lookup"><span data-stu-id="ef099-118">Messages</span></span>                    | <span data-ttu-id="ef099-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="ef099-119">Mail.Read</span></span>           |
| <span data-ttu-id="ef099-120">Grupos</span><span class="sxs-lookup"><span data-stu-id="ef099-120">Groups</span></span>                      | <span data-ttu-id="ef099-121">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="ef099-121">Group.Read.All</span></span>      |
| <span data-ttu-id="ef099-122">Usuarios</span><span class="sxs-lookup"><span data-stu-id="ef099-122">Users</span></span>                       | <span data-ttu-id="ef099-123">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="ef099-123">User.Read.All</span></span>       |
| <span data-ttu-id="ef099-124">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="ef099-124">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="ef099-125">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ef099-125">Files.ReadWrite</span></span>     |
| <span data-ttu-id="ef099-126">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="ef099-126">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="ef099-127">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef099-127">Files.ReadWrite.All</span></span> |
| <span data-ttu-id="ef099-128">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="ef099-128">Security alert</span></span>              | <span data-ttu-id="ef099-129">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef099-129">SecurityEvents.ReadWrite.All</span></span> |

<span data-ttu-id="ef099-130">***Nota:*** El extremo de /beta permite que los permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="ef099-130">***Note:*** The /beta endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="ef099-131">Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ef099-131">Conversations in a Group and OneDrive drive root items are not supported with application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="ef099-132">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef099-132">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ef099-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef099-133">Request headers</span></span>

| <span data-ttu-id="ef099-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef099-134">Name</span></span>       | <span data-ttu-id="ef099-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef099-135">Type</span></span> | <span data-ttu-id="ef099-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef099-136">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ef099-137">Autorización</span><span class="sxs-lookup"><span data-stu-id="ef099-137">Authorization</span></span>  | <span data-ttu-id="ef099-138">string</span><span class="sxs-lookup"><span data-stu-id="ef099-138">string</span></span>  | <span data-ttu-id="ef099-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef099-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ef099-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef099-141">Request body</span></span>

<span data-ttu-id="ef099-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ef099-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ef099-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef099-143">Response</span></span>

<span data-ttu-id="ef099-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ef099-144">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ef099-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef099-145">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ef099-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef099-146">Request</span></span>

<span data-ttu-id="ef099-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef099-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/beta/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="ef099-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef099-148">Response</span></span>

<span data-ttu-id="ef099-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef099-149">Here is an example of the response.</span></span>
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
