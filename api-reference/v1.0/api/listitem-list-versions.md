---
title: Lista de versiones de un ListItem
description: SharePoint se puede configurar para mantener el historial de elementos de lista.
ms.openlocfilehash: 43f28b355b733ba9651bba90f81179e59ebd3610
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030050"
---
# <a name="listing-versions-of-a-listitem"></a><span data-ttu-id="65522-103">Lista de versiones de un ListItem</span><span class="sxs-lookup"><span data-stu-id="65522-103">Listing versions of a ListItem</span></span>

<span data-ttu-id="65522-104">SharePoint se puede configurar para mantener el historial de elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="65522-104">SharePoint can be configured to retain the history for list items.</span></span>

<span data-ttu-id="65522-105">Las versiones anteriores pueden conservarse durante un período limitado de tiempo, en función de la configuración del administrador que puede ser única para cada usuario o ubicación.</span><span class="sxs-lookup"><span data-stu-id="65522-105">Previous versions may be retained for a finite period of time depending on admin settings which may be unique per user or location.</span></span>

## <a name="permissions"></a><span data-ttu-id="65522-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="65522-106">Permissions</span></span>

<span data-ttu-id="65522-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65522-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="65522-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65522-109">Permission type</span></span>             | <span data-ttu-id="65522-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65522-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="65522-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65522-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="65522-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="65522-112">Sites.Read.All, Sites.ReadWrite.All</span></span>         |
| <span data-ttu-id="65522-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65522-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="65522-114">N/D</span><span class="sxs-lookup"><span data-stu-id="65522-114">n/a</span></span>                                         |
| <span data-ttu-id="65522-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65522-115">Application</span></span>                            | <span data-ttu-id="65522-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="65522-116">Sites.Read.All, Sites.ReadWrite.All</span></span>         |


## <a name="http-request"></a><span data-ttu-id="65522-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65522-117">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /sites/{site-id}/items/{item-id}/versions
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions
```

## <a name="response"></a><span data-ttu-id="65522-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65522-118">Response</span></span>

<span data-ttu-id="65522-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ListItemVersion](../resources/listitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65522-119">If successful, this method returns a `200 OK` response code and collection of [ListItemVersion](../resources/listitemversion.md) objects in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="65522-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65522-120">Example</span></span>

<span data-ttu-id="65522-121">Este ejemplo recupera las versiones de un recurso listItem en una lista de SharePoint:</span><span class="sxs-lookup"><span data-stu-id="65522-121">This example retrieves the versions of a listItem in a SharePoint list:</span></span>

### <a name="http-request"></a><span data-ttu-id="65522-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65522-122">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-previous-versions-listitem", "scopes": "files.read sites.read.all" } -->

```http
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions
```

### <a name="response"></a><span data-ttu-id="65522-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65522-123">Response</span></span>

<span data-ttu-id="65522-124">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="65522-124">This returns a collection of versions:</span></span>

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
