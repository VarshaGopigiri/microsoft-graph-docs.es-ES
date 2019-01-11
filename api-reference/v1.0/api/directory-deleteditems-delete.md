---
title: Eliminar elementos permanentemente
description: Elimina permanentemente un elemento de la carpeta Elementos eliminados.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 00f44be1c89b35b81f3665d4bd568939ed309e22
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805190"
---
# <a name="permanently-delete-item"></a><span data-ttu-id="6716a-103">Eliminar elementos permanentemente</span><span class="sxs-lookup"><span data-stu-id="6716a-103">Permanently delete item</span></span>

<span data-ttu-id="6716a-104">Elimina permanentemente un elemento de la carpeta [Elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="6716a-104">Permanently deletes an item from [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="6716a-105">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="6716a-105">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span> <span data-ttu-id="6716a-106">Puede eliminar permanentemente un elemento de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="6716a-106">You can permanently delete an item from deleted items.</span></span> <span data-ttu-id="6716a-107">Pero, cuando un elemento se elimina permanentemente, **no** puede restaurarse.</span><span class="sxs-lookup"><span data-stu-id="6716a-107">But, once an item is permanently deleted, it **cannot** be restored.</span></span>

## <a name="permissions"></a><span data-ttu-id="6716a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6716a-108">Permissions</span></span>
<span data-ttu-id="6716a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6716a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

### <a name="for-users"></a><span data-ttu-id="6716a-111">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="6716a-111">For users:</span></span>

|<span data-ttu-id="6716a-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6716a-112">Permission type</span></span>      | <span data-ttu-id="6716a-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6716a-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6716a-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6716a-114">Delegated (work or school account)</span></span> | <span data-ttu-id="6716a-115">User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6716a-115">User.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="6716a-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6716a-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6716a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6716a-117">Not supported.</span></span> |
|<span data-ttu-id="6716a-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6716a-118">Application</span></span> | <span data-ttu-id="6716a-119">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6716a-119">User.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="6716a-120">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="6716a-120">For groups:</span></span>

|<span data-ttu-id="6716a-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6716a-121">Permission type</span></span>      | <span data-ttu-id="6716a-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6716a-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6716a-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6716a-123">Delegated (work or school account)</span></span> | <span data-ttu-id="6716a-124">Group.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6716a-124">Group.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="6716a-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6716a-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6716a-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6716a-126">Not supported.</span></span>    |
|<span data-ttu-id="6716a-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6716a-127">Application</span></span> | <span data-ttu-id="6716a-128">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6716a-128">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6716a-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6716a-129">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directory/deletedItems/{id}
```
## <a name="request-headers"></a><span data-ttu-id="6716a-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6716a-130">Request headers</span></span>
| <span data-ttu-id="6716a-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="6716a-131">Name</span></span>       | <span data-ttu-id="6716a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6716a-132">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6716a-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="6716a-133">Authorization</span></span>  | <span data-ttu-id="6716a-134">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="6716a-134">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="6716a-135">Accept</span><span class="sxs-lookup"><span data-stu-id="6716a-135">Accept</span></span>  | <span data-ttu-id="6716a-136">application/json</span><span class="sxs-lookup"><span data-stu-id="6716a-136">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="6716a-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6716a-137">Request body</span></span>
<span data-ttu-id="6716a-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6716a-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6716a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6716a-139">Response</span></span>

<span data-ttu-id="6716a-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6716a-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6716a-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6716a-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6716a-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6716a-143">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_directory"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/directory/deletedItems/{object-id}
```
##### <a name="response"></a><span data-ttu-id="6716a-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6716a-144">Response</span></span>
<span data-ttu-id="6716a-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6716a-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete directory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
