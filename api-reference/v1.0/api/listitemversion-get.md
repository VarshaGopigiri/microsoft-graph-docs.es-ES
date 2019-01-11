---
title: Obtener un recurso ListItemVersion
description: Recupere los metadatos de una versión específica de un recurso ListItem.
localization_priority: Normal
ms.openlocfilehash: 54fb491a13e90e1133127531d32c29e1ec2fa040
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888231"
---
# <a name="get-a-listitemversion-resource"></a><span data-ttu-id="ec740-103">Obtener un recurso ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="ec740-103">Get a ListItemVersion resource</span></span>

<span data-ttu-id="ec740-104">Recupere los metadatos de una versión específica de un recurso [ListItem](../resources/listitem.md).</span><span class="sxs-lookup"><span data-stu-id="ec740-104">Retrieve the metadata for a specific version of a [ListItem](../resources/listitem.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="ec740-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ec740-105">Permissions</span></span>

<span data-ttu-id="ec740-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ec740-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="ec740-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec740-108">Permission type</span></span>             | <span data-ttu-id="ec740-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec740-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="ec740-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec740-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="ec740-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ec740-111">Sites.Read.All, Sites.ReadWrite.All</span></span>         |
| <span data-ttu-id="ec740-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec740-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ec740-113">N/D</span><span class="sxs-lookup"><span data-stu-id="ec740-113">n/a</span></span>                                         |
| <span data-ttu-id="ec740-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec740-114">Application</span></span>                            | <span data-ttu-id="ec740-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ec740-115">Sites.Read.All, Sites.ReadWrite.All</span></span>         |


## <a name="http-request"></a><span data-ttu-id="ec740-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec740-116">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /sites/{site-id}/items/{item-id}/versions/{version-id}
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}
```


## <a name="response"></a><span data-ttu-id="ec740-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec740-117">Response</span></span>

<span data-ttu-id="ec740-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [ListItemVersion](../resources/listitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec740-118">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/listitemversion.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="ec740-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec740-119">Example</span></span>

<span data-ttu-id="ec740-120">Este ejemplo recupera una versión de un recurso listItem y expande la colección fields para solicitar los valores de los campos en el recurso listItem.</span><span class="sxs-lookup"><span data-stu-id="ec740-120">This example retrieves a version of a listItem and expands the fields collection to request the values of fields in the listItem.</span></span>

### <a name="http-request"></a><span data-ttu-id="ec740-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec740-121">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-single-version-listItem", "scopes": "files.read sites.read.all", "tags": "service.graph service.sharepoint" } -->

```http
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}?expand=fields
```

### <a name="response"></a><span data-ttu-id="ec740-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec740-122">Response</span></span>

<span data-ttu-id="ec740-123">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="ec740-123">This returns a collection of versions:</span></span>

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
