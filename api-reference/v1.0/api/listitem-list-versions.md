---
title: Lista de versiones de un ListItem
description: SharePoint se puede configurar para mantener el historial de elementos de lista.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 0da37c65c4f7cf737d7e37b0ed50305aa19b3e53
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921377"
---
# <a name="listing-versions-of-a-listitem"></a><span data-ttu-id="d521d-103">Lista de versiones de un ListItem</span><span class="sxs-lookup"><span data-stu-id="d521d-103">Listing versions of a ListItem</span></span>

<span data-ttu-id="d521d-104">SharePoint se puede configurar para mantener el historial de elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="d521d-104">SharePoint can be configured to retain the history for list items.</span></span>

<span data-ttu-id="d521d-105">Las versiones anteriores pueden conservarse durante un período limitado de tiempo, en función de la configuración del administrador que puede ser única para cada usuario o ubicación.</span><span class="sxs-lookup"><span data-stu-id="d521d-105">Previous versions may be retained for a finite period of time depending on admin settings which may be unique per user or location.</span></span>

## <a name="permissions"></a><span data-ttu-id="d521d-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="d521d-106">Permissions</span></span>

<span data-ttu-id="d521d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d521d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="d521d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d521d-109">Permission type</span></span>             | <span data-ttu-id="d521d-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d521d-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="d521d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d521d-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="d521d-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d521d-112">Sites.Read.All, Sites.ReadWrite.All</span></span>         |
| <span data-ttu-id="d521d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d521d-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d521d-114">N/D</span><span class="sxs-lookup"><span data-stu-id="d521d-114">n/a</span></span>                                         |
| <span data-ttu-id="d521d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d521d-115">Application</span></span>                            | <span data-ttu-id="d521d-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d521d-116">Sites.Read.All, Sites.ReadWrite.All</span></span>         |


## <a name="http-request"></a><span data-ttu-id="d521d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d521d-117">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /sites/{site-id}/items/{item-id}/versions
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions
```

## <a name="response"></a><span data-ttu-id="d521d-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d521d-118">Response</span></span>

<span data-ttu-id="d521d-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ListItemVersion](../resources/listitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d521d-119">If successful, this method returns a `200 OK` response code and collection of [ListItemVersion](../resources/listitemversion.md) objects in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="d521d-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d521d-120">Example</span></span>

<span data-ttu-id="d521d-121">Este ejemplo recupera las versiones de un recurso listItem en una lista de SharePoint:</span><span class="sxs-lookup"><span data-stu-id="d521d-121">This example retrieves the versions of a listItem in a SharePoint list:</span></span>

### <a name="http-request"></a><span data-ttu-id="d521d-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d521d-122">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-previous-versions-listitem", "scopes": "files.read sites.read.all" } -->

```http
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions
```

### <a name="response"></a><span data-ttu-id="d521d-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d521d-123">Response</span></span>

<span data-ttu-id="d521d-124">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="d521d-124">This returns a collection of versions:</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.listItemVersion)", "truncated": true } -->

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
      "lastModifiedDateTime": "2017-09-14T12:34:53.912Z"
    },
    {
      "id": "2.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-11T10:21:03.000Z"
    },
    {
      "id": "1.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-10T15:20:01.125Z"
    }
  ]
}
```


<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
