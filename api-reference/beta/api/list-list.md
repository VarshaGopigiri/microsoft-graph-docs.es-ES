---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Enumerar las listas de SharePoint en un sitio
ms.openlocfilehash: bae0bc23c6a50200c0c380470bb5c70943c6ab0e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090731"
---
# <a name="enumerate-lists-in-a-site"></a><span data-ttu-id="a2e64-102">Enumere listas en un sitio.</span><span class="sxs-lookup"><span data-stu-id="a2e64-102">Enumerate lists in a site</span></span>

> <span data-ttu-id="a2e64-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2e64-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2e64-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2e64-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a2e64-105">Obtenga la colección de [listas][] de un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="a2e64-105">Get the collection of [lists][] for a [site][].</span></span>

[lists]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="a2e64-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2e64-108">Permissions</span></span>

<span data-ttu-id="a2e64-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2e64-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2e64-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2e64-111">Permission type</span></span>      | <span data-ttu-id="a2e64-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2e64-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a2e64-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2e64-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a2e64-114">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a2e64-114">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="a2e64-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2e64-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2e64-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2e64-116">Not supported.</span></span>    |
|<span data-ttu-id="a2e64-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2e64-117">Application</span></span> | <span data-ttu-id="a2e64-118">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a2e64-118">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a2e64-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2e64-119">HTTP request</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists
```

## <a name="example"></a><span data-ttu-id="a2e64-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2e64-120">Example</span></span>

#### <a name="request"></a><span data-ttu-id="a2e64-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2e64-121">Request</span></span>

<!-- { "blockType": "request", "name": "enum-lists", "scopes": "sites.read.all service.sharepoint" } -->

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists
```

##### <a name="response"></a><span data-ttu-id="a2e64-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2e64-122">Response</span></span>

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

## <a name="remarks"></a><span data-ttu-id="a2e64-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a2e64-123">Remarks</span></span>

<span data-ttu-id="a2e64-124">De manera predeterminada, las listas con la faceta [system][] están ocultas.</span><span class="sxs-lookup"><span data-stu-id="a2e64-124">Lists with the [system][] facet are hidden by default.</span></span>
<span data-ttu-id="a2e64-125">Para obtener una lista de ellas, incluya `system` en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="a2e64-125">To list them, include `system` in your `$select` statement.</span></span>

[system]: ../resources/systemfacet.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Lists/Enumerate"
} -->
