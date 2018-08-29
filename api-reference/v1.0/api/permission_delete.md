---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminar el acceso a un elemento
ms.openlocfilehash: 011345afb9789b0ff2927704a1e678f39656a719
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268623"
---
# <a name="delete-a-sharing-permission-from-a-file-or-folder"></a><span data-ttu-id="d4cb3-102">Eliminar un permiso de uso compartido de un archivo o una carpeta</span><span class="sxs-lookup"><span data-stu-id="d4cb3-102">Delete a sharing permission from a file or folder</span></span>

<span data-ttu-id="d4cb3-103">Quita el acceso a un [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="d4cb3-103">Remove access to a [DriveItem](../resources/driveitem.md).</span></span>

<span data-ttu-id="d4cb3-104">Solo se pueden eliminar los permisos de uso compartido **no** heredados.</span><span class="sxs-lookup"><span data-stu-id="d4cb3-104">Only sharing permissions that are **not** inherited can be deleted.</span></span>
<span data-ttu-id="d4cb3-105">La propiedad **inheritedFrom** debe ser `null`.</span><span class="sxs-lookup"><span data-stu-id="d4cb3-105">The **inheritedFrom** property must be `null`.</span></span>

## <a name="permissions"></a><span data-ttu-id="d4cb3-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="d4cb3-106">Permissions</span></span>

<span data-ttu-id="d4cb3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d4cb3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d4cb3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4cb3-109">Permission type</span></span>      | <span data-ttu-id="d4cb3-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4cb3-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d4cb3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4cb3-111">Delegated (work or school account)</span></span> | <span data-ttu-id="d4cb3-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4cb3-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="d4cb3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4cb3-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d4cb3-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4cb3-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="d4cb3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4cb3-115">Application</span></span> | <span data-ttu-id="d4cb3-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4cb3-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d4cb3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4cb3-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
DELETE /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /me/drive/items/{item-id}/permissions/{perm-id}
DELETE /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="d4cb3-118">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="d4cb3-118">Optional request headers</span></span>

| <span data-ttu-id="d4cb3-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="d4cb3-119">Name</span></span>          | <span data-ttu-id="d4cb3-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4cb3-120">Type</span></span>   | <span data-ttu-id="d4cb3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4cb3-121">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cb3-122">if-match</span><span class="sxs-lookup"><span data-stu-id="d4cb3-122">if-match</span></span>      | <span data-ttu-id="d4cb3-123">cadena</span><span class="sxs-lookup"><span data-stu-id="d4cb3-123">string</span></span> | <span data-ttu-id="d4cb3-124">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="d4cb3-124">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="response"></a><span data-ttu-id="d4cb3-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4cb3-125">Response</span></span>

<span data-ttu-id="d4cb3-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d4cb3-126">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="d4cb3-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4cb3-127">Example</span></span>

<span data-ttu-id="d4cb3-128">En este ejemplo, se quita el permiso identificado como {perm-id} del elemento {item-id} del OneDrive del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="d4cb3-128">This example removes the permission identified as {perm-id} from the item {item-id} in the current user's OneDrive.</span></span>

<!-- { "blockType": "request", "name": "delete-permission", "scopes": "files.readwrite", "tags": "service.graph" }-->

```http
DELETE /me/drive/items/{item-id}/permissions/{perm-id}
```

### <a name="response"></a><span data-ttu-id="d4cb3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4cb3-129">Response</span></span>

<!-- { "blockType": "response", "truncated": false } -->

```http
HTTP/1.1 204 No Content
```

## <a name="remarks"></a><span data-ttu-id="d4cb3-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4cb3-130">Remarks</span></span>

* <span data-ttu-id="d4cb3-131">Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en la DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="d4cb3-131">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span> 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Remove an item's sharing permissions",
  "keywords": "permission, permissions, sharing, remove permissions, delete permissions",
  "section": "documentation",
  "tocPath": "Sharing/Remove permissions"
} -->
