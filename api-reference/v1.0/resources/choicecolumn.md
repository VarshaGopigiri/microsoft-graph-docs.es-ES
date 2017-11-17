---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
ms.openlocfilehash: c266550e8918603c3ee6104818c0aa721f1281d9
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="choicecolumn-resource-type"></a><span data-ttu-id="bd8f5-102">Tipo de recurso ChoiceColumn</span><span class="sxs-lookup"><span data-stu-id="bd8f5-102">ChoiceColumn resource type</span></span>

<span data-ttu-id="bd8f5-103">El recurso **choiceColumn** en un recurso [columnDefinition](columnDefinition.md) indica que se pueden seleccionar los valores de la columna de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="bd8f5-103">The **choiceColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values can be selected from a list of choices.</span></span>

## <a name="json-representation"></a><span data-ttu-id="bd8f5-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bd8f5-104">JSON representation</span></span>

<span data-ttu-id="bd8f5-105">A continuación se incluye una representación JSON de un recurso **ChoiceColumn**.</span><span class="sxs-lookup"><span data-stu-id="bd8f5-105">Here is a JSON representation of a **driveItem** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.choiceColumn" } -->

```json
{
  "allowTextEntry": true,
  "choices": ["red", "blue", "green"],
  "displayAs": "checkBoxes | dropDownMenu | radioButtons"
}
```

## <a name="properties"></a><span data-ttu-id="bd8f5-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd8f5-106">Properties</span></span>

| <span data-ttu-id="bd8f5-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="bd8f5-107">Property name</span></span>      | <span data-ttu-id="bd8f5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd8f5-108">Type</span></span>               | <span data-ttu-id="bd8f5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd8f5-109">Description</span></span>
|:-------------------|:-------------------|:----------------------------------------------
| <span data-ttu-id="bd8f5-110">**allowTextEntry**</span><span class="sxs-lookup"><span data-stu-id="bd8f5-110">**allowTextEntry**</span></span> | <span data-ttu-id="bd8f5-111">boolean</span><span class="sxs-lookup"><span data-stu-id="bd8f5-111">boolean</span></span>            | <span data-ttu-id="bd8f5-112">Si es true, permite valores personalizados que no están en las opciones configuradas.</span><span class="sxs-lookup"><span data-stu-id="bd8f5-112">If true, allows custom values that aren't in the configured choices.</span></span>
| <span data-ttu-id="bd8f5-113">**choices**</span><span class="sxs-lookup"><span data-stu-id="bd8f5-113">**CHOICES**</span></span>        | <span data-ttu-id="bd8f5-114">collection(string)</span><span class="sxs-lookup"><span data-stu-id="bd8f5-114">Collection(String)</span></span> | <span data-ttu-id="bd8f5-115">La lista de valores disponibles para esta columna.</span><span class="sxs-lookup"><span data-stu-id="bd8f5-115">The list of values available for this column.</span></span>
| <span data-ttu-id="bd8f5-116">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="bd8f5-116">**displayAs**</span></span>      | <span data-ttu-id="bd8f5-117">string</span><span class="sxs-lookup"><span data-stu-id="bd8f5-117">string</span></span>             | <span data-ttu-id="bd8f5-118">Cómo se deben mostrar las opciones en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="bd8f5-118">How the choices are to be presented in the UX.</span></span> <span data-ttu-id="bd8f5-119">Debe ser `checkBoxes`, `dropDownMenu` o `radioButtons`</span><span class="sxs-lookup"><span data-stu-id="bd8f5-119">Must be one of `checkBoxes`, `dropDownMenu`, or `radioButtons`</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ChoiceColumn"
} -->
