---
title: Lista de versiones de un DriveItem
description: OneDrive y SharePoint se pueden configurar para mantener el historial de archivos.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 52df6b0f7e452d358160de886ed61824fd2d48d0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915728"
---
# <a name="listing-versions-of-a-driveitem"></a><span data-ttu-id="4a3ba-103">Lista de versiones de un DriveItem</span><span class="sxs-lookup"><span data-stu-id="4a3ba-103">Listing versions of a DriveItem</span></span>

> <span data-ttu-id="4a3ba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a3ba-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4a3ba-106">OneDrive y SharePoint se pueden configurar para mantener el historial de archivos.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-106">OneDrive and SharePoint can be configured to retain the history for files.</span></span>
<span data-ttu-id="4a3ba-107">En función del servicio y la configuración, se puede crear una versión para cada edición, cada vez que se guarda el archivo, manualmente, o nunca.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-107">Depending on the service and configuration, a new version can be created for each edit, each time the file is saved, manually, or never.</span></span>

<span data-ttu-id="4a3ba-108">Las versiones anteriores de un documento pueden conservarse durante un período limitado de tiempo, en función de la configuración del administrador que puede ser única para cada usuario o ubicación.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-108">Previous versions of a document may be retained for a finite period of time depending on admin settings which may be unique per user or location.</span></span>

## <a name="permissions"></a><span data-ttu-id="4a3ba-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a3ba-109">Permissions</span></span>

<span data-ttu-id="4a3ba-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4a3ba-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4a3ba-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a3ba-112">Permission type</span></span>      | <span data-ttu-id="4a3ba-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a3ba-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a3ba-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a3ba-114">Delegated (work or school account)</span></span> | <span data-ttu-id="4a3ba-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a3ba-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="4a3ba-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a3ba-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a3ba-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a3ba-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="4a3ba-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a3ba-118">Application</span></span> | <span data-ttu-id="4a3ba-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a3ba-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="4a3ba-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a3ba-120">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions
GET /groups/{group-id}/drive/{item-id}/versions
GET /me/drive/items/{item-id}/versions
GET /sites/{site-id}/drive/items/{item-id}/versions
GET /users/{user-id}/drive/items/{item-id}/versions
```

## <a name="response"></a><span data-ttu-id="4a3ba-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a3ba-121">Response</span></span>

<span data-ttu-id="4a3ba-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [DriveItemVersion](../resources/driveitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-122">If successful, this method returns a `200 OK` response code and collection of [DriveItemVersion](../resources/driveitemversion.md) objects in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="4a3ba-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a3ba-123">Example</span></span>

<span data-ttu-id="4a3ba-124">Este ejemplo recupera las versiones de un archivo en la unidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-124">This example retrieves the versions of a file in the current user's drive.</span></span>

### <a name="http-request"></a><span data-ttu-id="4a3ba-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a3ba-125">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-previous-versions", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/versions
```

### <a name="response"></a><span data-ttu-id="4a3ba-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a3ba-126">Response</span></span>

<span data-ttu-id="4a3ba-127">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="4a3ba-127">This returns a collection of versions:</span></span>

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

## <a name="remarks"></a><span data-ttu-id="4a3ba-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a3ba-128">Remarks</span></span>

<span data-ttu-id="4a3ba-129">OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-129">OneDrive does not preserve the complete metadata for previous versions of a file.</span></span>

<span data-ttu-id="4a3ba-130">Cuando la aplicación recupera la lista de versiones disponibles de un archivo, se devuelve un recurso [DriveItemVersion](../resources/driveitemversion.md) que proporciona la información disponible sobre la versión específica.</span><span class="sxs-lookup"><span data-stu-id="4a3ba-130">When your app retrieves the list of available versions for a file, a [DriveItemVersion](../resources/driveitemversion.md) resource is returned that provides the available information about the specific version.</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
