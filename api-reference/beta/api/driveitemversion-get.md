---
title: Obtener un recurso DriveItemVersion (versión preliminar)
description: Recupere los metadatos de una versión específica de un recurso DriveItem.
ms.openlocfilehash: c78a81d1a5428bbb969f8761b238655ab7919e5a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084948"
---
# <a name="get-a-driveitemversion-resource-preview"></a><span data-ttu-id="59fbe-103">Obtener un recurso DriveItemVersion (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="59fbe-103">Get a DriveItemVersion resource (preview)</span></span>

> <span data-ttu-id="59fbe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="59fbe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="59fbe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="59fbe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="59fbe-106">Recupere los metadatos de una versión específica de un recurso [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="59fbe-106">Retrieve the metadata for a specific version of a [DriveItem](../resources/driveitem.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="59fbe-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="59fbe-107">Permissions</span></span>

<span data-ttu-id="59fbe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59fbe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="59fbe-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59fbe-110">Permission type</span></span>      | <span data-ttu-id="59fbe-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59fbe-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="59fbe-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59fbe-112">Delegated (work or school account)</span></span> | <span data-ttu-id="59fbe-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59fbe-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="59fbe-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59fbe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="59fbe-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59fbe-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="59fbe-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59fbe-116">Application</span></span> | <span data-ttu-id="59fbe-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59fbe-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="59fbe-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59fbe-118">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions/{version-id}
GET /groups/{group-id}/drive/{item-id}/versions/{version-id}
GET /me/drive/items/{item-id}/versions/{version-id}
GET /sites/{site-id}/drive/items/{item-id}/versions/{version-id}
GET /users/{user-id}/drive/items/{item-id}/versions/{version-id}
```

## <a name="response"></a><span data-ttu-id="59fbe-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59fbe-119">Response</span></span>

<span data-ttu-id="59fbe-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [DriveItemVersion](../resources/driveitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59fbe-120">If successful, this method returns a `200 OK` response code and a [DriveItemVersion](../resources/driveitemversion.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="59fbe-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59fbe-121">Example</span></span>

<span data-ttu-id="59fbe-122">Este ejemplo recupera una versión de un archivo en la unidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="59fbe-122">This example retrieves a version of a file in the current user's drive.</span></span>

### <a name="http-request"></a><span data-ttu-id="59fbe-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59fbe-123">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-single-version", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/versions/{version-id}
```

### <a name="response"></a><span data-ttu-id="59fbe-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59fbe-124">Response</span></span>

<span data-ttu-id="59fbe-125">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="59fbe-125">This returns a collection of versions:</span></span>

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

## <a name="remarks"></a><span data-ttu-id="59fbe-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59fbe-126">Remarks</span></span>

<span data-ttu-id="59fbe-127">OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.</span><span class="sxs-lookup"><span data-stu-id="59fbe-127">OneDrive does not preserve the complete metadata for previous versions of a file.</span></span>

<span data-ttu-id="59fbe-128">Cuando la aplicación recupera la lista de versiones disponibles de un archivo, se devuelve un recurso [DriveItemVersion](../resources/driveitemversion.md) que proporciona la información disponible sobre la versión específica.</span><span class="sxs-lookup"><span data-stu-id="59fbe-128">When your app retrieves the list of available versions for a file, a [DriveItemVersion](../resources/driveitemversion.md) resource is returned that provides the available information about the specific version.</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
