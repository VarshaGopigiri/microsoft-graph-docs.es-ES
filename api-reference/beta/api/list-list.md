---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Enumerar las listas de SharePoint en un sitio
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: fa13fc93dcfcfc807671082be43a7c4b4eafd63d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957875"
---
# <a name="enumerate-lists-in-a-site"></a><span data-ttu-id="7545a-102">Enumere listas en un sitio.</span><span class="sxs-lookup"><span data-stu-id="7545a-102">Enumerate lists in a site</span></span>

> <span data-ttu-id="7545a-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7545a-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7545a-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7545a-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7545a-105">Obtenga la colección de [listas][] de un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="7545a-105">Get the collection of [lists][] for a [site][].</span></span>

[lists]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="7545a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="7545a-108">Permissions</span></span>

<span data-ttu-id="7545a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7545a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7545a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7545a-111">Permission type</span></span>      | <span data-ttu-id="7545a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7545a-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7545a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7545a-113">Delegated (work or school account)</span></span> | <span data-ttu-id="7545a-114">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7545a-114">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="7545a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7545a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7545a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7545a-116">Not supported.</span></span>    |
|<span data-ttu-id="7545a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7545a-117">Application</span></span> | <span data-ttu-id="7545a-118">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7545a-118">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7545a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7545a-119">HTTP request</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists
```

## <a name="example"></a><span data-ttu-id="7545a-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7545a-120">Example</span></span>

#### <a name="request"></a><span data-ttu-id="7545a-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7545a-121">Request</span></span>

<!-- { "blockType": "request", "name": "enum-lists", "scopes": "sites.read.all service.sharepoint" } -->

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists
```

##### <a name="response"></a><span data-ttu-id="7545a-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7545a-122">Response</span></span>

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

## <a name="remarks"></a><span data-ttu-id="7545a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7545a-123">Remarks</span></span>

<span data-ttu-id="7545a-124">De manera predeterminada, las listas con la faceta [system][] están ocultas.</span><span class="sxs-lookup"><span data-stu-id="7545a-124">Lists with the [system][] facet are hidden by default.</span></span>
<span data-ttu-id="7545a-125">Para obtener una lista de ellas, incluya `system` en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="7545a-125">To list them, include `system` in your `$select` statement.</span></span>

[system]: ../resources/systemfacet.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Lists/Enumerate"
} -->
