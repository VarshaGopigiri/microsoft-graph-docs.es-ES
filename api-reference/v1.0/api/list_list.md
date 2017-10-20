---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Enumerar las listas de SharePoint en un sitio
ms.openlocfilehash: 4be4c4aefc29cdcd684bc11ad086b5c0572dbe2b
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="enumerate-lists-in-a-site"></a><span data-ttu-id="3d5f5-102">Enumere listas en un sitio.</span><span class="sxs-lookup"><span data-stu-id="3d5f5-102">Enumerate lists in a site</span></span>

<span data-ttu-id="3d5f5-103">Obtenga la colección de [listas][] de un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="3d5f5-103">Get the collection of [lists][] for a [site][].</span></span>

[lists]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="3d5f5-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d5f5-106">Permissions</span></span>

<span data-ttu-id="3d5f5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3d5f5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3d5f5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d5f5-109">Permission type</span></span>      | <span data-ttu-id="3d5f5-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d5f5-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3d5f5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d5f5-111">Delegated (work or school account)</span></span> | <span data-ttu-id="3d5f5-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3d5f5-112">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="3d5f5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d5f5-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3d5f5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d5f5-114">Not supported.</span></span>    |
|<span data-ttu-id="3d5f5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d5f5-115">Application</span></span> | <span data-ttu-id="3d5f5-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3d5f5-116">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3d5f5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d5f5-117">HTTP request</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists
```

## <a name="example"></a><span data-ttu-id="3d5f5-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d5f5-118">Example</span></span>

#### <a name="request"></a><span data-ttu-id="3d5f5-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d5f5-119">Request</span></span>

<!-- { "blockType": "request", "name": "enum-lists", "scopes": "sites.read.all service.sharepoint" } -->

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists
```

##### <a name="response"></a><span data-ttu-id="3d5f5-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d5f5-120">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.list", "isCollection": true, "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "b57af081-936c-4803-a120-d94887b03864",
      "name": "Documents",
      "createdDateTime": "2016-08-30T08:32:00Z",
      "lastModifiedDateTime": "2016-08-30T08:32:00Z",
      "list": {
        "hidden": false,
        "template": "documentLibrary"
       }
    },
    {
      "id": "1234-112-112-4",
      "name": "MicroFeed",
      "createdDateTime": "2016-08-30T08:32:00Z",
      "lastModifiedDateTime": "2016-08-30T08:32:00Z",
      "list": {
        "hidden": false,
        "template": "genericList"
       }
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Lists/Enumerate"
} -->
