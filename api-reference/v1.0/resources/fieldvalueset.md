---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: FieldValueSet
localization_priority: Normal
ms.openlocfilehash: 1f8c842f107b5090eb80bba9e614666f10d4dc0b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889694"
---
# <a name="fieldvalueset-resource"></a><span data-ttu-id="ac4e4-102">Recurso FieldValueSet</span><span class="sxs-lookup"><span data-stu-id="ac4e4-102">FieldValueSet resource</span></span>

<span data-ttu-id="ac4e4-103">Representa los valores de columna en un recurso [listItem](listitem.md).</span><span class="sxs-lookup"><span data-stu-id="ac4e4-103">Represents the column values in a [listItem](listitem.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ac4e4-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ac4e4-104">JSON representation</span></span>

<span data-ttu-id="ac4e4-105">A continuación se incluye una representación JSON del recurso **fieldValueSet**.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-105">Here is a JSON representation of a **fieldValueSet** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.fieldValueSet",
      "optionalProperties": ["Author", "AuthorLookupId", "Name", "Color", "Quantity" ],
       "baseType": "microsoft.graph.entity", "openType": true } -->

```json
{
    "Author": "Brad Cleaver",
    "AuthorLookupId": "13",
    "Name": "Kangaroos and Wallabies: A Deep Dive",
    "Color": "Red",
    "Quantity": 350,
}
```

## <a name="properties"></a><span data-ttu-id="ac4e4-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac4e4-106">Properties</span></span>

<span data-ttu-id="ac4e4-107">Cada campo visible para el usuario en el recurso **listItem** se devuelve como un par nombre-valor en el recurso **fieldValueSet**.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-107">Each user-visible field in the **listItem** is returned as a name-value pair in the **fieldValueSet**.</span></span>
<span data-ttu-id="ac4e4-108">El ejemplo anterior es de una lista que contiene cuatro columnas: **Author** (Autor), **Name** (Nombre), **Color** y **Quantity** (Cantidad).</span><span class="sxs-lookup"><span data-stu-id="ac4e4-108">The example above is for a list that contains four columns, **Author**, **Name**, **Color**, and **Quantity**.</span></span>

<span data-ttu-id="ac4e4-109">Los campos de búsqueda (como `Author`) no se devuelven de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-109">Lookup fields (like `Author` above) are not returned by default.</span></span>
<span data-ttu-id="ac4e4-110">En su lugar, el servidor devuelve un campo "LookupId" (como `AuthorLookupId`) que hace referencia al recurso listItem que se buscaba.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-110">Instead, the server returns a 'LookupId' field (like `AuthorLookupId` above) referencing the listItem targeted in the lookup.</span></span>
<span data-ttu-id="ac4e4-111">El nombre del campo "LookupId" es el nombre de campo original seguido de `LookupId`.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-111">The name of the 'LookupId' field is the original field name followed by `LookupId`.</span></span>

<span data-ttu-id="ac4e4-112">Se pueden solicitar hasta 12 campos de búsqueda en una única consulta.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-112">Up to 12 lookup fields may be requested in a single query.</span></span>
<span data-ttu-id="ac4e4-113">El servidor devolverá valores de búsqueda si la solicitud incluye una instrucción `select` con los campos que necesita.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-113">The server will return lookup values if your request includes a `select` statement with the fields you need.</span></span>
<span data-ttu-id="ac4e4-114">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ac4e4-114">Example:</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Author,BookTitle,PageCount)
```

<span data-ttu-id="ac4e4-115">Puede solicitar hasta 12 campos de búsqueda en una única consulta, además de cualquier número de campos normales.</span><span class="sxs-lookup"><span data-stu-id="ac4e4-115">You may request up to 12 lookup fields in a single query, plus any number of regular fields.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/FieldValueSet"
} -->
