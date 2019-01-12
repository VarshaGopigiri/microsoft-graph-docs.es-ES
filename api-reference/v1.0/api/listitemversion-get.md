---
title: Obtener un recurso ListItemVersion
description: Recupere los metadatos de una versión específica de un recurso ListItem.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 3e45cf260a9f526a7309c63791ed2cb6b8196e45
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972540"
---
# <a name="get-a-listitemversion-resource"></a><span data-ttu-id="93b59-103">Obtener un recurso ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="93b59-103">Get a ListItemVersion resource</span></span>

<span data-ttu-id="93b59-104">Recupere los metadatos de una versión específica de un recurso [ListItem](../resources/listitem.md).</span><span class="sxs-lookup"><span data-stu-id="93b59-104">Retrieve the metadata for a specific version of a [ListItem](../resources/listitem.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="93b59-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="93b59-105">Permissions</span></span>

<span data-ttu-id="93b59-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="93b59-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="93b59-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="93b59-108">Permission type</span></span>             | <span data-ttu-id="93b59-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="93b59-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="93b59-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="93b59-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="93b59-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93b59-111">Sites.Read.All, Sites.ReadWrite.All</span></span>         |
| <span data-ttu-id="93b59-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="93b59-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="93b59-113">N/D</span><span class="sxs-lookup"><span data-stu-id="93b59-113">n/a</span></span>                                         |
| <span data-ttu-id="93b59-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="93b59-114">Application</span></span>                            | <span data-ttu-id="93b59-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93b59-115">Sites.Read.All, Sites.ReadWrite.All</span></span>         |


## <a name="http-request"></a><span data-ttu-id="93b59-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93b59-116">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /sites/{site-id}/items/{item-id}/versions/{version-id}
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}
```


## <a name="response"></a><span data-ttu-id="93b59-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93b59-117">Response</span></span>

<span data-ttu-id="93b59-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [ListItemVersion](../resources/listitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93b59-118">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/listitemversion.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="93b59-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93b59-119">Example</span></span>

<span data-ttu-id="93b59-120">Este ejemplo recupera una versión de un recurso listItem y expande la colección fields para solicitar los valores de los campos en el recurso listItem.</span><span class="sxs-lookup"><span data-stu-id="93b59-120">This example retrieves a version of a listItem and expands the fields collection to request the values of fields in the listItem.</span></span>

### <a name="http-request"></a><span data-ttu-id="93b59-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93b59-121">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-single-version-listItem", "scopes": "files.read sites.read.all", "tags": "service.graph service.sharepoint" } -->

```http
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}?expand=fields
```

### <a name="response"></a><span data-ttu-id="93b59-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93b59-122">Response</span></span>

<span data-ttu-id="93b59-123">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="93b59-123">This returns a collection of versions:</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.listItemVersion", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": "1.0",
    "lastModifiedBy": {
    "user": {
        "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
        "displayName": "Ryan Gregg"
    }
    },
    "lastModifiedDateTime": "2017-09-14T12:34:53.912Z",
    "fields": {  }
}
```

<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
