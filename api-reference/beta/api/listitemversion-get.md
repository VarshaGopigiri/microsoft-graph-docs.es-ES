---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener una versión anterior de un elemento de lista - API de SharePoint
localization_priority: Normal
ms.openlocfilehash: 7f009eb006e44dd2f8e25052b0326ffc92243c7f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881609"
---
# <a name="get-a-listitemversion-resource-preview"></a><span data-ttu-id="3d79b-102">Obtener un recurso ListItemVersion (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="3d79b-102">Get a ListItemVersion resource (preview)</span></span>

> <span data-ttu-id="3d79b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3d79b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3d79b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3d79b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3d79b-105">Recupere los metadatos de una versión específica de un recurso [ListItem](../resources/listitem.md).</span><span class="sxs-lookup"><span data-stu-id="3d79b-105">Retrieve the metadata for a specific version of a [ListItem](../resources/listitem.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="3d79b-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d79b-106">Permissions</span></span>

<span data-ttu-id="3d79b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3d79b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="3d79b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d79b-109">Permission type</span></span>             | <span data-ttu-id="3d79b-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d79b-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="3d79b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d79b-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="3d79b-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3d79b-112">Sites.Read.All, Sites.ReadWrite.All</span></span>         |
| <span data-ttu-id="3d79b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d79b-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3d79b-114">N/D</span><span class="sxs-lookup"><span data-stu-id="3d79b-114">n/a</span></span>                                         |
| <span data-ttu-id="3d79b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d79b-115">Application</span></span>                            | <span data-ttu-id="3d79b-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3d79b-116">Sites.Read.All, Sites.ReadWrite.All</span></span>         |


## <a name="http-request"></a><span data-ttu-id="3d79b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d79b-117">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /sites/{site-id}/items/{item-id}/versions/{version-id}
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}
```


## <a name="response"></a><span data-ttu-id="3d79b-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d79b-118">Response</span></span>

<span data-ttu-id="3d79b-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [ListItemVersion](../resources/listitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d79b-119">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/listitemversion.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="3d79b-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d79b-120">Example</span></span>

<span data-ttu-id="3d79b-121">Este ejemplo recupera una versión de un recurso listItem y expande la colección fields para solicitar los valores de los campos en el recurso listItem.</span><span class="sxs-lookup"><span data-stu-id="3d79b-121">This example retrieves a version of a listItem and expands the fields collection to request the values of fields in the listItem.</span></span>

### <a name="http-request"></a><span data-ttu-id="3d79b-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d79b-122">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-single-version-listItem", "scopes": "files.read" } -->

```http
GET /sites/{site-id}/items/{item-id}/versions/{version-id}?expand=fields
```

### <a name="response"></a><span data-ttu-id="3d79b-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d79b-123">Response</span></span>

<span data-ttu-id="3d79b-124">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="3d79b-124">This returns a collection of versions:</span></span>

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
