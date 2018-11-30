---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener una versión anterior de un registro de lista de SharePoint
ms.openlocfilehash: 12687e679b99e78b046bf54405af6b1a47f67177
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089380"
---
# <a name="listing-versions-of-a-listitem-preview"></a><span data-ttu-id="dfb4c-102">Enumerar versiones de un recurso ListItem (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="dfb4c-102">Listing versions of a ListItem (preview)</span></span>

> <span data-ttu-id="dfb4c-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dfb4c-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dfb4c-105">SharePoint se puede configurar para mantener el historial de elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-105">SharePoint can be configured to retain the history for list items.</span></span>

<span data-ttu-id="dfb4c-106">Las versiones anteriores pueden conservarse durante un período limitado de tiempo, en función de la configuración del administrador que puede ser única para cada usuario o ubicación.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-106">Previous versions may be retained for a finite period of time depending on admin settings which may be unique per user or location.</span></span>

## <a name="permissions"></a><span data-ttu-id="dfb4c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dfb4c-107">Permissions</span></span>

<span data-ttu-id="dfb4c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dfb4c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="dfb4c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dfb4c-110">Permission type</span></span>             | <span data-ttu-id="dfb4c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dfb4c-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="dfb4c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dfb4c-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="dfb4c-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dfb4c-113">Sites.Read.All, Sites.ReadWrite.All</span></span>         |
| <span data-ttu-id="dfb4c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dfb4c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dfb4c-115">N/D</span><span class="sxs-lookup"><span data-stu-id="dfb4c-115">n/a</span></span>                                         |
| <span data-ttu-id="dfb4c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dfb4c-116">Application</span></span>                            | <span data-ttu-id="dfb4c-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dfb4c-117">Sites.Read.All, Sites.ReadWrite.All</span></span>         |


## <a name="http-request"></a><span data-ttu-id="dfb4c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dfb4c-118">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /sites/{site-id}/items/{item-id}/versions
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions
```

## <a name="response"></a><span data-ttu-id="dfb4c-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfb4c-119">Response</span></span>

<span data-ttu-id="dfb4c-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ListItemVersion](../resources/listitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-120">If successful, this method returns a `200 OK` response code and collection of [ListItemVersion](../resources/listitemversion.md) objects in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="dfb4c-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dfb4c-121">Example</span></span>

<span data-ttu-id="dfb4c-122">Este ejemplo recupera las versiones de un recurso listItem en una lista de SharePoint:</span><span class="sxs-lookup"><span data-stu-id="dfb4c-122">This example retrieves the versions of a listItem in a SharePoint list:</span></span>

### <a name="http-request"></a><span data-ttu-id="dfb4c-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dfb4c-123">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-previous-versions-listitem", "scopes": "files.read" } -->

```http
GET /sites/{site-id}/items/{item-id}/versions
```

### <a name="response"></a><span data-ttu-id="dfb4c-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfb4c-124">Response</span></span>

<span data-ttu-id="dfb4c-125">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="dfb4c-125">This returns a collection of versions:</span></span>

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