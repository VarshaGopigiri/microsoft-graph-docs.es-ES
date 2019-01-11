---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
localization_priority: Normal
ms.openlocfilehash: 3640e68902485215dda575cc93407f019007ee18
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826582"
---
# <a name="choicecolumn-resource-type"></a><span data-ttu-id="6ca3f-102">Tipo de recurso ChoiceColumn</span><span class="sxs-lookup"><span data-stu-id="6ca3f-102">ChoiceColumn resource type</span></span>

<span data-ttu-id="6ca3f-103">El recurso **choiceColumn** en un recurso [columnDefinition](columndefinition.md) indica que se pueden seleccionar los valores de la columna de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-103">The **choiceColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values can be selected from a list of choices.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6ca3f-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6ca3f-104">JSON representation</span></span>

<span data-ttu-id="6ca3f-105">A continuación se incluye una representación JSON de un recurso **ChoiceColumn**.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-105">Here is a JSON representation of a **choiceColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.choiceColumn" } -->

```json
{
  "allowTextEntry": true,
  "choices": ["red", "blue", "green"],
  "displayAs": "checkBoxes | dropDownMenu | radioButtons"
}
```

## <a name="properties"></a><span data-ttu-id="6ca3f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ca3f-106">Properties</span></span>

| <span data-ttu-id="6ca3f-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="6ca3f-107">Property name</span></span>      | <span data-ttu-id="6ca3f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ca3f-108">Type</span></span>               | <span data-ttu-id="6ca3f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ca3f-109">Description</span></span>
|:-------------------|:-------------------|:----------------------------------------------
| <span data-ttu-id="6ca3f-110">**allowTextEntry**</span><span class="sxs-lookup"><span data-stu-id="6ca3f-110">**allowTextEntry**</span></span> | <span data-ttu-id="6ca3f-111">boolean</span><span class="sxs-lookup"><span data-stu-id="6ca3f-111">boolean</span></span>            | <span data-ttu-id="6ca3f-112">Si es true, permite valores personalizados que no están en las opciones configuradas.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-112">If true, allows custom values that aren't in the configured choices.</span></span>
| <span data-ttu-id="6ca3f-113">**choices**</span><span class="sxs-lookup"><span data-stu-id="6ca3f-113">**choices**</span></span>        | <span data-ttu-id="6ca3f-114">collection(string)</span><span class="sxs-lookup"><span data-stu-id="6ca3f-114">collection(string)</span></span> | <span data-ttu-id="6ca3f-115">La lista de valores disponibles para esta columna.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-115">The list of values available for this column.</span></span>
| <span data-ttu-id="6ca3f-116">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="6ca3f-116">**displayAs**</span></span>      | <span data-ttu-id="6ca3f-117">string</span><span class="sxs-lookup"><span data-stu-id="6ca3f-117">string</span></span>             | <span data-ttu-id="6ca3f-118">Cómo se deben mostrar las opciones en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-118">How the choices are to be presented in the UX.</span></span> <span data-ttu-id="6ca3f-119">Debe ser `checkBoxes`, `dropDownMenu` o `radioButtons`</span><span class="sxs-lookup"><span data-stu-id="6ca3f-119">Must be one of `checkBoxes`, `dropDownMenu`, or `radioButtons`</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/choicecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(checkBoxes,dropDownMenu,radioButtons) are in resource, but () are in table"
  ],
  "tocPath": "Resources/ChoiceColumn"
} -->
