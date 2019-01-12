---
title: Delete subscription
description: Elimina una suscripción.
localization_priority: Normal
author: piotrci
ms.openlocfilehash: eeed4a7f6981a89a1869257bed339eb6895f25b9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932584"
---
# <a name="delete-subscription"></a><span data-ttu-id="f5f81-103">Delete subscription</span><span class="sxs-lookup"><span data-stu-id="f5f81-103">Delete subscription</span></span>

<span data-ttu-id="f5f81-104">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="f5f81-104">Delete a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="f5f81-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f5f81-105">Permissions</span></span>

<span data-ttu-id="f5f81-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5f81-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f5f81-108">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="f5f81-108">Resource type / Item</span></span>        | <span data-ttu-id="f5f81-109">Permiso</span><span class="sxs-lookup"><span data-stu-id="f5f81-109">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="f5f81-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="f5f81-110">Contacts</span></span>                    | <span data-ttu-id="f5f81-111">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="f5f81-111">Contacts.Read</span></span>       |
| <span data-ttu-id="f5f81-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="f5f81-112">Conversations</span></span>               | <span data-ttu-id="f5f81-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5f81-113">Group.Read.All</span></span>      |
| <span data-ttu-id="f5f81-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="f5f81-114">Events</span></span>                      | <span data-ttu-id="f5f81-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="f5f81-115">Calendars.Read</span></span>      |
| <span data-ttu-id="f5f81-116">Mensajes</span><span class="sxs-lookup"><span data-stu-id="f5f81-116">Messages</span></span>                    | <span data-ttu-id="f5f81-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="f5f81-117">Mail.Read</span></span>           |
| <span data-ttu-id="f5f81-118">Grupos</span><span class="sxs-lookup"><span data-stu-id="f5f81-118">Groups</span></span>                      | <span data-ttu-id="f5f81-119">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5f81-119">Group.Read.All</span></span>      |
| <span data-ttu-id="f5f81-120">Usuarios</span><span class="sxs-lookup"><span data-stu-id="f5f81-120">Users</span></span>                       | <span data-ttu-id="f5f81-121">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5f81-121">User.Read.All</span></span>       |
| <span data-ttu-id="f5f81-122">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="f5f81-122">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="f5f81-123">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5f81-123">Files.ReadWrite</span></span>     |
| <span data-ttu-id="f5f81-124">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="f5f81-124">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="f5f81-125">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f5f81-125">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="f5f81-126">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="f5f81-126">Security alert</span></span>| <span data-ttu-id="f5f81-127">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f5f81-127">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f5f81-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5f81-128">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="f5f81-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5f81-129">Request headers</span></span>

| <span data-ttu-id="f5f81-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="f5f81-130">Name</span></span>       | <span data-ttu-id="f5f81-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5f81-131">Type</span></span> | <span data-ttu-id="f5f81-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5f81-132">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="f5f81-133">Autorización</span><span class="sxs-lookup"><span data-stu-id="f5f81-133">Authorization</span></span>  | <span data-ttu-id="f5f81-134">string</span><span class="sxs-lookup"><span data-stu-id="f5f81-134">string</span></span>  | <span data-ttu-id="f5f81-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5f81-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f5f81-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5f81-137">Request body</span></span>

<span data-ttu-id="f5f81-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5f81-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5f81-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5f81-139">Response</span></span>

<span data-ttu-id="f5f81-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f5f81-140">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f5f81-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5f81-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="f5f81-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5f81-142">Request</span></span>

<span data-ttu-id="f5f81-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5f81-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="f5f81-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5f81-144">Response</span></span>

<span data-ttu-id="f5f81-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5f81-145">Here is an example of the response.</span></span>
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
