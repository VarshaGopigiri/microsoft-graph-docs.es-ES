---
title: Lista de versiones de un DriveItem
description: OneDrive y SharePoint se pueden configurar para mantener el historial de archivos.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: fa25734967aca0ad5c7022f147ca243530f1ac3f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932066"
---
# <a name="listing-versions-of-a-driveitem"></a><span data-ttu-id="d20a8-103">Lista de versiones de un DriveItem</span><span class="sxs-lookup"><span data-stu-id="d20a8-103">Listing versions of a DriveItem</span></span>

<span data-ttu-id="d20a8-104">OneDrive y SharePoint se pueden configurar para mantener el historial de archivos.</span><span class="sxs-lookup"><span data-stu-id="d20a8-104">OneDrive and SharePoint can be configured to retain the history for files.</span></span>
<span data-ttu-id="d20a8-105">En función del servicio y la configuración, se puede crear una versión para cada edición, cada vez que se guarda el archivo, manualmente, o nunca.</span><span class="sxs-lookup"><span data-stu-id="d20a8-105">Depending on the service and configuration, a new version can be created for each edit, each time the file is saved, manually, or never.</span></span>

<span data-ttu-id="d20a8-106">Las versiones anteriores de un documento pueden conservarse durante un período limitado de tiempo, en función de la configuración del administrador que puede ser única para cada usuario o ubicación.</span><span class="sxs-lookup"><span data-stu-id="d20a8-106">Previous versions of a document may be retained for a finite period of time depending on admin settings which may be unique per user or location.</span></span>

## <a name="permissions"></a><span data-ttu-id="d20a8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d20a8-107">Permissions</span></span>

<span data-ttu-id="d20a8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d20a8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d20a8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d20a8-110">Permission type</span></span>      | <span data-ttu-id="d20a8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d20a8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d20a8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d20a8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d20a8-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d20a8-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="d20a8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d20a8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d20a8-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d20a8-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="d20a8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d20a8-116">Application</span></span> | <span data-ttu-id="d20a8-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d20a8-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="d20a8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d20a8-118">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions
GET /groups/{group-id}/drive/{item-id}/versions
GET /me/drive/items/{item-id}/versions
GET /sites/{site-id}/drive/items/{item-id}/versions
GET /users/{user-id}/drive/items/{item-id}/versions
```

## <a name="response"></a><span data-ttu-id="d20a8-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d20a8-119">Response</span></span>

<span data-ttu-id="d20a8-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [DriveItemVersion](../resources/driveitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d20a8-120">If successful, this method returns a `200 OK` response code and collection of [DriveItemVersion](../resources/driveitemversion.md) objects in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="d20a8-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d20a8-121">Example</span></span>

<span data-ttu-id="d20a8-122">Este ejemplo recupera las versiones de un archivo en la unidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="d20a8-122">This example retrieves the versions of a file in the current user's drive.</span></span>

### <a name="http-request"></a><span data-ttu-id="d20a8-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d20a8-123">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-previous-versions", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/versions
```

### <a name="response"></a><span data-ttu-id="d20a8-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d20a8-124">Response</span></span>

<span data-ttu-id="d20a8-125">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="d20a8-125">This returns a collection of versions:</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItemVersion)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value":
  [
    {
      "id": "3.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-14T12:34:53.912Z",
      "size": 123
    },
    {
      "id": "2.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-11T10:21:03.000Z",
      "size": 62
    },
    {
      "id": "1.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-10T15:20:01.125Z",
      "size": 16
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="d20a8-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d20a8-126">Remarks</span></span>

<span data-ttu-id="d20a8-127">OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.</span><span class="sxs-lookup"><span data-stu-id="d20a8-127">OneDrive does not preserve the complete metadata for previous versions of a file.</span></span>

<span data-ttu-id="d20a8-128">Cuando la aplicación recupera la lista de versiones disponibles de un archivo, se devuelve un recurso [DriveItemVersion](../resources/driveitemversion.md) que proporciona la información disponible sobre la versión específica.</span><span class="sxs-lookup"><span data-stu-id="d20a8-128">When your app retrieves the list of available versions for a file, a [DriveItemVersion](../resources/driveitemversion.md) resource is returned that provides the available information about the specific version.</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
