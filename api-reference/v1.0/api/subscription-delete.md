---
title: Delete subscription
description: Elimina una suscripción.
ms.openlocfilehash: 249393cef11e2768eec0a6435a8485b51cf6921c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032480"
---
# <a name="delete-subscription"></a><span data-ttu-id="eed4f-103">Delete subscription</span><span class="sxs-lookup"><span data-stu-id="eed4f-103">Delete subscription</span></span>

<span data-ttu-id="eed4f-104">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="eed4f-104">Delete a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="eed4f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="eed4f-105">Permissions</span></span>

<span data-ttu-id="eed4f-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eed4f-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="eed4f-108">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="eed4f-108">Resource type / Item</span></span>        | <span data-ttu-id="eed4f-109">Permiso</span><span class="sxs-lookup"><span data-stu-id="eed4f-109">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="eed4f-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="eed4f-110">Contacts</span></span>                    | <span data-ttu-id="eed4f-111">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="eed4f-111">Contacts.Read</span></span>       |
| <span data-ttu-id="eed4f-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="eed4f-112">Conversations</span></span>               | <span data-ttu-id="eed4f-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="eed4f-113">Group.Read.All</span></span>      |
| <span data-ttu-id="eed4f-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="eed4f-114">Events</span></span>                      | <span data-ttu-id="eed4f-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="eed4f-115">Calendars.Read</span></span>      |
| <span data-ttu-id="eed4f-116">Mensajes</span><span class="sxs-lookup"><span data-stu-id="eed4f-116">Messages</span></span>                    | <span data-ttu-id="eed4f-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="eed4f-117">Mail.Read</span></span>           |
| <span data-ttu-id="eed4f-118">Groups</span><span class="sxs-lookup"><span data-stu-id="eed4f-118">Groups</span></span>                      | <span data-ttu-id="eed4f-119">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="eed4f-119">Group.Read.All</span></span>      |
| <span data-ttu-id="eed4f-120">Users</span><span class="sxs-lookup"><span data-stu-id="eed4f-120">Users</span></span>                       | <span data-ttu-id="eed4f-121">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="eed4f-121">User.Read.All</span></span>       |
| <span data-ttu-id="eed4f-122">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="eed4f-122">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="eed4f-123">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eed4f-123">Files.ReadWrite</span></span>     |
| <span data-ttu-id="eed4f-124">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="eed4f-124">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="eed4f-125">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eed4f-125">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="eed4f-126">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="eed4f-126">Security alert</span></span>| <span data-ttu-id="eed4f-127">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eed4f-127">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eed4f-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eed4f-128">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="eed4f-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eed4f-129">Request headers</span></span>

| <span data-ttu-id="eed4f-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="eed4f-130">Name</span></span>       | <span data-ttu-id="eed4f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="eed4f-131">Type</span></span> | <span data-ttu-id="eed4f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="eed4f-132">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="eed4f-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="eed4f-133">Authorization</span></span>  | <span data-ttu-id="eed4f-134">string</span><span class="sxs-lookup"><span data-stu-id="eed4f-134">string</span></span>  | <span data-ttu-id="eed4f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eed4f-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eed4f-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eed4f-137">Request body</span></span>

<span data-ttu-id="eed4f-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eed4f-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eed4f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eed4f-139">Response</span></span>

<span data-ttu-id="eed4f-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="eed4f-140">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="eed4f-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eed4f-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="eed4f-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eed4f-142">Request</span></span>

<span data-ttu-id="eed4f-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eed4f-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="eed4f-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eed4f-144">Response</span></span>

<span data-ttu-id="eed4f-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eed4f-145">Here is an example of the response.</span></span>
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
