---
title: Eliminar elementos permanentemente
description: Elimina permanentemente un elemento de la carpeta Elementos eliminados.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: a5f9bfb7a235386abb6f0e885aa9ada5f1e32517
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853980"
---
# <a name="permanently-delete-item"></a><span data-ttu-id="3b4d3-103">Eliminar elementos permanentemente</span><span class="sxs-lookup"><span data-stu-id="3b4d3-103">Permanently delete item</span></span>

> <span data-ttu-id="3b4d3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b4d3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b4d3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b4d3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b4d3-106">Elimina permanentemente un elemento de la carpeta [Elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="3b4d3-106">Permanently deletes an item from [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="3b4d3-107">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="3b4d3-107">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span> <span data-ttu-id="3b4d3-108">Puede eliminar permanentemente un elemento de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="3b4d3-108">You can permanently delete an item from deleted items.</span></span> <span data-ttu-id="3b4d3-109">Pero, cuando un elemento se elimina permanentemente, **no** puede restaurarse.</span><span class="sxs-lookup"><span data-stu-id="3b4d3-109">But, once an item is permanently deleted, it **cannot** be restored.</span></span>

## <a name="permissions"></a><span data-ttu-id="3b4d3-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="3b4d3-110">Permissions</span></span>
<span data-ttu-id="3b4d3-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b4d3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="3b4d3-113">Para los usuarios: User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3b4d3-113">For users: User.ReadWrite.All, Directory.AccessAsUser.All</span></span>
* <span data-ttu-id="3b4d3-114">Para los grupos: Group.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3b4d3-114">For groups: Group.ReadWrite.All, Directory.AccessAsUser.All</span></span>

## <a name="http-request"></a><span data-ttu-id="3b4d3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b4d3-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directory/deleteditems/{id}
```
## <a name="request-headers"></a><span data-ttu-id="3b4d3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b4d3-116">Request headers</span></span>
| <span data-ttu-id="3b4d3-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="3b4d3-117">Name</span></span>       | <span data-ttu-id="3b4d3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b4d3-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3b4d3-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="3b4d3-119">Authorization</span></span>  | <span data-ttu-id="3b4d3-120">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="3b4d3-120">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="3b4d3-121">Accept</span><span class="sxs-lookup"><span data-stu-id="3b4d3-121">Accept</span></span>  | <span data-ttu-id="3b4d3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3b4d3-122">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="3b4d3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b4d3-123">Request body</span></span>
<span data-ttu-id="3b4d3-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3b4d3-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3b4d3-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b4d3-125">Response</span></span>

<span data-ttu-id="3b4d3-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b4d3-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3b4d3-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b4d3-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3b4d3-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b4d3-129">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_directory"
}-->
```http
DELETE https://graph.microsoft.com/beta/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb
```
##### <a name="response"></a><span data-ttu-id="3b4d3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b4d3-130">Response</span></span>
<span data-ttu-id="3b4d3-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3b4d3-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
