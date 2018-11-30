---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Enumerar las listas de SharePoint en un sitio
ms.openlocfilehash: 4171947eb2a7ac6be18ba385de39c5befd762f26
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031648"
---
# <a name="enumerate-lists-in-a-site"></a><span data-ttu-id="07599-102">Enumere listas en un sitio.</span><span class="sxs-lookup"><span data-stu-id="07599-102">Enumerate lists in a site</span></span>

<span data-ttu-id="07599-103">Obtenga la colección de [listas][] de un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="07599-103">Get the collection of [lists][] for a [site][].</span></span>

[lists]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="07599-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="07599-106">Permissions</span></span>

<span data-ttu-id="07599-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07599-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="07599-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07599-109">Permission type</span></span>      | <span data-ttu-id="07599-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07599-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="07599-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07599-111">Delegated (work or school account)</span></span> | <span data-ttu-id="07599-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="07599-112">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="07599-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07599-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="07599-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07599-114">Not supported.</span></span>    |
|<span data-ttu-id="07599-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07599-115">Application</span></span> | <span data-ttu-id="07599-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="07599-116">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="07599-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07599-117">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists
```

## <a name="example"></a><span data-ttu-id="07599-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07599-118">Example</span></span>

#### <a name="request"></a><span data-ttu-id="07599-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07599-119">Request</span></span>

<!-- { "blockType": "request", "name": "enum-lists", "scopes": "sites.read.all", "tags": "service.sharepoint" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists
```

##### <a name="response"></a><span data-ttu-id="07599-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07599-120">Response</span></span>

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

## <a name="remarks"></a><span data-ttu-id="07599-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07599-121">Remarks</span></span>

<span data-ttu-id="07599-122">De manera predeterminada, las listas con la faceta [system][] están ocultas.</span><span class="sxs-lookup"><span data-stu-id="07599-122">Lists with the [system][] facet are hidden by default.</span></span>
<span data-ttu-id="07599-123">Para obtener una lista de ellas, incluya `system` en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="07599-123">To list them, include `system` in your `$select` statement.</span></span>

[system]: ../resources/systemfacet.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Lists/Enumerate"
} -->
