---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: FieldValueSet
ms.openlocfilehash: f1cc8d4d61d53b30c1da3e86f614895eb9d10833
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087951"
---
# <a name="fieldvalueset-resource"></a><span data-ttu-id="fd8c4-102">Recurso FieldValueSet</span><span class="sxs-lookup"><span data-stu-id="fd8c4-102">FieldValueSet resource</span></span>

> <span data-ttu-id="fd8c4-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fd8c4-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fd8c4-105">Representa los valores de columna en un recurso [listItem](listitem.md).</span><span class="sxs-lookup"><span data-stu-id="fd8c4-105">Represents the column values in a [listItem](listitem.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fd8c4-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fd8c4-106">JSON representation</span></span>

<span data-ttu-id="fd8c4-107">A continuación se incluye una representación JSON del recurso **fieldValueSet**.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-107">Here is a JSON representation of a **fieldValueSet** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.fieldValueSet",
       "keyProperty": "id", "openType": true } -->

```json
{
    "Author": "Brad Cleaver",
    "AuthorLookupId": "13",
    "Name": "Kangaroos and Wallabies: A Deep Dive",
    "Color": "Red",
    "Quantity": 350,
}
```

## <a name="properties"></a><span data-ttu-id="fd8c4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd8c4-108">Properties</span></span>

<span data-ttu-id="fd8c4-109">Cada campo visible para el usuario en el recurso **listItem** se devuelve como un par nombre-valor en el recurso **fieldValueSet**.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-109">Each user-visible field in the **listItem** is returned as a name-value pair in the **fieldValueSet**.</span></span>
<span data-ttu-id="fd8c4-110">El ejemplo anterior es de una lista que contiene cuatro columnas: **Author** (Autor), **Name** (Nombre), **Color** y **Quantity** (Cantidad).</span><span class="sxs-lookup"><span data-stu-id="fd8c4-110">The example above is for a list that contains four columns, **Author**, **Name**, **Color**, and **Quantity**.</span></span>

<span data-ttu-id="fd8c4-111">Los campos de búsqueda (como `Author`) no se devuelven de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-111">Lookup fields (like `Author` above) are not returned by default.</span></span>
<span data-ttu-id="fd8c4-112">En su lugar, el servidor devuelve un campo "LookupId" (como `AuthorLookupId`) que hace referencia al recurso listItem que se buscaba.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-112">Instead, the server returns a 'LookupId' field (like `AuthorLookupId` above) referencing the listItem targeted in the lookup.</span></span>
<span data-ttu-id="fd8c4-113">El nombre del campo "LookupId" es el nombre de campo original seguido de `LookupId`.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-113">The name of the 'LookupId' field is the original field name followed by `LookupId`.</span></span>

<span data-ttu-id="fd8c4-114">Se pueden solicitar hasta 12 campos de búsqueda en una única consulta.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-114">Up to 12 lookup fields may be requested in a single query.</span></span>
<span data-ttu-id="fd8c4-115">El servidor devolverá valores de búsqueda si la solicitud incluye una instrucción `select` con los campos que necesita.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-115">The server will return lookup values if your request includes a `select` statement with the fields you need.</span></span>
<span data-ttu-id="fd8c4-116">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fd8c4-116">Example:</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Author,BookTitle,PageCount)
```

<span data-ttu-id="fd8c4-117">Puede solicitar hasta 12 campos de búsqueda en una única consulta, además de cualquier número de campos normales.</span><span class="sxs-lookup"><span data-stu-id="fd8c4-117">You may request up to 12 lookup fields in a single query, plus any number of regular fields.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/FieldValueSet"
} -->
