---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminar el acceso a un elemento
ms.openlocfilehash: 726818b14a694380e46bfd38280e4cba9effb67d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088309"
---
# <a name="delete-a-sharing-permission-from-a-file-or-folder"></a><span data-ttu-id="ed3c0-102">Eliminar un permiso de uso compartido de un archivo o una carpeta</span><span class="sxs-lookup"><span data-stu-id="ed3c0-102">Delete a sharing permission from a file or folder</span></span>

> <span data-ttu-id="ed3c0-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed3c0-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ed3c0-105">Quita el acceso a un [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="ed3c0-105">Remove access to a [DriveItem](../resources/driveitem.md).</span></span>

<span data-ttu-id="ed3c0-106">Solo se pueden eliminar los permisos de uso compartido **no** heredados.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-106">Only sharing permissions that are **not** inherited can be deleted.</span></span>
<span data-ttu-id="ed3c0-107">La propiedad **inheritedFrom** debe ser `null`.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-107">The **inheritedFrom** property must be `null`.</span></span>

## <a name="permissions"></a><span data-ttu-id="ed3c0-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ed3c0-108">Permissions</span></span>
<span data-ttu-id="ed3c0-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed3c0-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed3c0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed3c0-111">Permission type</span></span>      | <span data-ttu-id="ed3c0-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed3c0-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ed3c0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed3c0-113">Delegated (work or school account)</span></span> | <span data-ttu-id="ed3c0-114">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed3c0-114">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="ed3c0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed3c0-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ed3c0-116">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed3c0-116">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="ed3c0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed3c0-117">Application</span></span> | <span data-ttu-id="ed3c0-118">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed3c0-118">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ed3c0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed3c0-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
DELETE /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /me/drive/items/{item-id}/permissions/{perm-id}
DELETE /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="ed3c0-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ed3c0-120">Optional request headers</span></span>

| <span data-ttu-id="ed3c0-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="ed3c0-121">Name</span></span>          | <span data-ttu-id="ed3c0-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed3c0-122">Type</span></span>   | <span data-ttu-id="ed3c0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed3c0-123">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3c0-124">if-match</span><span class="sxs-lookup"><span data-stu-id="ed3c0-124">if-match</span></span>      | <span data-ttu-id="ed3c0-125">string</span><span class="sxs-lookup"><span data-stu-id="ed3c0-125">string</span></span> | <span data-ttu-id="ed3c0-126">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-126">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |


## <a name="response"></a><span data-ttu-id="ed3c0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed3c0-127">Response</span></span>

<span data-ttu-id="ed3c0-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-128">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ed3c0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed3c0-129">Example</span></span>

<span data-ttu-id="ed3c0-130">En este ejemplo, se quita el permiso identificado como {perm-id} del elemento {item-id} del OneDrive del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-130">This example removes the permission identified as {perm-id} from the item {item-id} in the current user's OneDrive.</span></span>

<!-- { "blockType": "request", "name": "delete-permission", "scopes": "files.readwrite" }-->

```http
DELETE https://graph.microsoft.com/beta/me/drive/root/items/{item-id}/permissions/{perm-id}
```

### <a name="response"></a><span data-ttu-id="ed3c0-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed3c0-131">Response</span></span>

<!-- { "blockType": "response", "truncated": false } -->

```http
HTTP/1.1 204 No Content
```

## <a name="remarks"></a><span data-ttu-id="ed3c0-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed3c0-132">Remarks</span></span>

* <span data-ttu-id="ed3c0-133">Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en la DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="ed3c0-133">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span> 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Remove an item's sharing permissions",
  "keywords": "permission, permissions, sharing, remove permissions, delete permissions",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Delete permission"
}-->
