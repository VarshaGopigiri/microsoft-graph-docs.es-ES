---
title: Restaurar una versión anterior de un objeto DriveItem
description: Restaure una versión anterior de un objeto DriveItem para que sea la versión actual. Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del archivo.
localization_priority: Normal
ms.openlocfilehash: 0097d82bb9d317c0bee0392f21040f0963364183
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871613"
---
# <a name="restore-a-previous-version-of-a-driveitem"></a><span data-ttu-id="95638-104">Restaurar una versión anterior de un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="95638-104">Restore a previous version of a DriveItem</span></span>

<span data-ttu-id="95638-105">Restaure una versión anterior de un objeto DriveItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="95638-105">Restore a previous version of a DriveItem to be the current version.</span></span> <span data-ttu-id="95638-106">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del archivo.</span><span class="sxs-lookup"><span data-stu-id="95638-106">This will create a new version with the contents of the previous version, but preserves all existing versions of the file.</span></span>

## <a name="permissions"></a><span data-ttu-id="95638-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="95638-107">Permissions</span></span>

<span data-ttu-id="95638-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="95638-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="95638-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="95638-110">Permission type</span></span>      | <span data-ttu-id="95638-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="95638-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="95638-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="95638-112">Delegated (work or school account)</span></span> | <span data-ttu-id="95638-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="95638-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="95638-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="95638-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="95638-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="95638-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="95638-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="95638-116">Application</span></span> | <span data-ttu-id="95638-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="95638-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="95638-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="95638-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/versions/{version-id}/restoreVersion
POST /groups/{groupId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /me/drive/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{siteId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /users/{userId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="95638-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="95638-119">Request body</span></span>

<span data-ttu-id="95638-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="95638-120">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="95638-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95638-121">Example</span></span>

<span data-ttu-id="95638-122">En este ejemplo, se restaura una versión de un archivo identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="95638-122">This example restores a version of a file identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drives/{drive-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="95638-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95638-123">Response</span></span>

<span data-ttu-id="95638-124">Si se realiza correctamente, la llamada API devuelve `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="95638-124">If successful, the API call returns a `204 No Content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
