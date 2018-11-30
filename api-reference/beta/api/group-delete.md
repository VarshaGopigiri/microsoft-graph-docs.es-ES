---
title: Delete group
description: Elimina un grupo.
ms.openlocfilehash: 92a15366fefb6ab70c45f664daa28b75bcea5891
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086180"
---
# <a name="delete-group"></a><span data-ttu-id="dec14-103">Delete group</span><span class="sxs-lookup"><span data-stu-id="dec14-103">Delete group</span></span>

> <span data-ttu-id="dec14-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dec14-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dec14-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dec14-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dec14-106">Elimina un grupo.</span><span class="sxs-lookup"><span data-stu-id="dec14-106">Deletes a group.</span></span>

<span data-ttu-id="dec14-107">Cuando se elimina un grupo, el elemento se agrega a [los elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="dec14-107">When a group is deleted, the item is added to [deleted items](../resources/directory.md).</span></span> <span data-ttu-id="dec14-108">El grupo permanecerá en los elementos eliminados de hasta 30 días.</span><span class="sxs-lookup"><span data-stu-id="dec14-108">The group will remain in deleted items for up to 30 days.</span></span> <span data-ttu-id="dec14-109">Un grupo se puede restaurar totalmente de los elementos eliminados durante los 30 días.</span><span class="sxs-lookup"><span data-stu-id="dec14-109">A group can be fully restored from deleted items during the 30 days.</span></span> <span data-ttu-id="dec14-110">Después de 30 días, se eliminan permanentemente los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="dec14-110">After 30 days, deleted items are permanently deleted.</span></span>

## <a name="permissions"></a><span data-ttu-id="dec14-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="dec14-111">Permissions</span></span>
<span data-ttu-id="dec14-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dec14-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dec14-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dec14-114">Permission type</span></span>      | <span data-ttu-id="dec14-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dec14-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dec14-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dec14-116">Delegated (work or school account)</span></span> | <span data-ttu-id="dec14-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dec14-117">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="dec14-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dec14-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dec14-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dec14-119">Not supported.</span></span>    |
|<span data-ttu-id="dec14-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dec14-120">Application</span></span> | <span data-ttu-id="dec14-121">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dec14-121">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dec14-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dec14-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="dec14-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dec14-123">Request headers</span></span>
| <span data-ttu-id="dec14-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="dec14-124">Name</span></span>       | <span data-ttu-id="dec14-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="dec14-125">Type</span></span> | <span data-ttu-id="dec14-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="dec14-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="dec14-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="dec14-127">Authorization</span></span>  | <span data-ttu-id="dec14-128">string</span><span class="sxs-lookup"><span data-stu-id="dec14-128">string</span></span>  | <span data-ttu-id="dec14-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dec14-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dec14-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dec14-131">Request body</span></span>
<span data-ttu-id="dec14-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dec14-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dec14-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dec14-133">Response</span></span>
<span data-ttu-id="dec14-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dec14-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dec14-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dec14-136">Example</span></span>
#### <a name="request"></a><span data-ttu-id="dec14-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dec14-137">Request</span></span>
<span data-ttu-id="dec14-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dec14-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/{id}
```

#### <a name="response"></a><span data-ttu-id="dec14-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dec14-139">Response</span></span>
<span data-ttu-id="dec14-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dec14-140">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->