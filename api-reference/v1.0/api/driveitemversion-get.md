---
title: Obtener un recurso DriveItemVersion
description: Recupere los metadatos de una versión específica de un recurso DriveItem.
ms.openlocfilehash: 1b803e92b7a717514e794da5ac8da04c0ef05f6a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032632"
---
# <a name="get-a-driveitemversion-resource"></a><span data-ttu-id="e3a11-103">Obtener un recurso DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="e3a11-103">Get a DriveItemVersion resource</span></span>

<span data-ttu-id="e3a11-104">Recupere los metadatos de una versión específica de un recurso [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="e3a11-104">Retrieve the metadata for a specific version of a [DriveItem](../resources/driveitem.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="e3a11-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e3a11-105">Permissions</span></span>

<span data-ttu-id="e3a11-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3a11-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e3a11-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3a11-108">Permission type</span></span>      | <span data-ttu-id="e3a11-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3a11-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e3a11-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3a11-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e3a11-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3a11-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="e3a11-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3a11-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e3a11-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3a11-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="e3a11-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3a11-114">Application</span></span> | <span data-ttu-id="e3a11-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3a11-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="e3a11-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3a11-116">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions/{version-id}
GET /groups/{group-id}/drive/{item-id}/versions/{version-id}
GET /me/drive/items/{item-id}/versions/{version-id}
GET /sites/{site-id}/drive/items/{item-id}/versions/{version-id}
GET /users/{user-id}/drive/items/{item-id}/versions/{version-id}
```

## <a name="response"></a><span data-ttu-id="e3a11-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3a11-117">Response</span></span>

<span data-ttu-id="e3a11-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [DriveItemVersion](../resources/driveitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3a11-118">If successful, this method returns a `200 OK` response code and a [DriveItemVersion](../resources/driveitemversion.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="e3a11-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3a11-119">Example</span></span>

<span data-ttu-id="e3a11-120">Este ejemplo recupera una versión de un archivo en la unidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e3a11-120">This example retrieves a version of a file in the current user's drive.</span></span>

### <a name="http-request"></a><span data-ttu-id="e3a11-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3a11-121">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-single-version", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/versions/{version-id}
```

### <a name="response"></a><span data-ttu-id="e3a11-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3a11-122">Response</span></span>

<span data-ttu-id="e3a11-123">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="e3a11-123">This returns a collection of versions:</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItemVersion", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": "D4990684-58CE-4FAB-9B87-D6C49E74F298",
    "lastModifiedBy": {
    "user": {
        "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
        "displayName": "Ryan Gregg"
    }
    },
    "lastModifiedDateTime": "2017-09-14T12:34:53.912Z",
    "size": 123
}
```

## <a name="remarks"></a><span data-ttu-id="e3a11-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3a11-124">Remarks</span></span>

<span data-ttu-id="e3a11-125">OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.</span><span class="sxs-lookup"><span data-stu-id="e3a11-125">OneDrive does not preserve the complete metadata for previous versions of a file.</span></span>

<span data-ttu-id="e3a11-126">Cuando la aplicación recupera la lista de versiones disponibles de un archivo, se devuelve un recurso [DriveItemVersion](../resources/driveitemversion.md) que proporciona la información disponible sobre la versión específica.</span><span class="sxs-lookup"><span data-stu-id="e3a11-126">When your app retrieves the list of available versions for a file, a [DriveItemVersion](../resources/driveitemversion.md) resource is returned that provides the available information about the specific version.</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->