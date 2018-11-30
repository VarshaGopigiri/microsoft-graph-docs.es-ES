---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
ms.openlocfilehash: 659ece2eab255fe7b55a258b0980eda4e7bde5b2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083160"
---
# <a name="choicecolumn-resource-type"></a><span data-ttu-id="c538a-102">Tipo de recurso ChoiceColumn</span><span class="sxs-lookup"><span data-stu-id="c538a-102">ChoiceColumn resource type</span></span>

> <span data-ttu-id="c538a-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c538a-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c538a-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c538a-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c538a-105">El recurso **choiceColumn** en un recurso [columnDefinition](columndefinition.md) indica que se pueden seleccionar los valores de la columna de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="c538a-105">The **choiceColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values can be selected from a list of choices.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c538a-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c538a-106">JSON representation</span></span>

<span data-ttu-id="c538a-107">A continuación se incluye una representación JSON de un recurso **ChoiceColumn**.</span><span class="sxs-lookup"><span data-stu-id="c538a-107">Here is a JSON representation of a **choiceColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.choiceColumn" } -->

```json
{
  "allowTextEntry": true,
  "choices": ["red", "blue", "green"],
  "displayAs": "checkBoxes | dropDownMenu | radioButtons"
}
```

## <a name="properties"></a><span data-ttu-id="c538a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c538a-108">Properties</span></span>

| <span data-ttu-id="c538a-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="c538a-109">Property name</span></span>      | <span data-ttu-id="c538a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c538a-110">Type</span></span>               | <span data-ttu-id="c538a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c538a-111">Description</span></span>
|:-------------------|:-------------------|:----------------------------------------------
| <span data-ttu-id="c538a-112">**allowTextEntry**</span><span class="sxs-lookup"><span data-stu-id="c538a-112">**allowTextEntry**</span></span> | <span data-ttu-id="c538a-113">boolean</span><span class="sxs-lookup"><span data-stu-id="c538a-113">boolean</span></span>            | <span data-ttu-id="c538a-114">Si es true, permite valores personalizados que no están en las opciones configuradas.</span><span class="sxs-lookup"><span data-stu-id="c538a-114">If true, allows custom values that aren't in the configured choices.</span></span>
| <span data-ttu-id="c538a-115">**choices**</span><span class="sxs-lookup"><span data-stu-id="c538a-115">**choices**</span></span>        | <span data-ttu-id="c538a-116">collection(string)</span><span class="sxs-lookup"><span data-stu-id="c538a-116">collection(string)</span></span> | <span data-ttu-id="c538a-117">La lista de valores disponibles para esta columna.</span><span class="sxs-lookup"><span data-stu-id="c538a-117">The list of values available for this column.</span></span>
| <span data-ttu-id="c538a-118">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="c538a-118">**displayAs**</span></span>      | <span data-ttu-id="c538a-119">string</span><span class="sxs-lookup"><span data-stu-id="c538a-119">string</span></span>             | <span data-ttu-id="c538a-120">Cómo se deben mostrar las opciones en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="c538a-120">How the choices are to be presented in the UX.</span></span> <span data-ttu-id="c538a-121">Debe ser `checkBoxes`, `dropDownMenu` o `radioButtons`</span><span class="sxs-lookup"><span data-stu-id="c538a-121">Must be one of `checkBoxes`, `dropDownMenu`, or `radioButtons`</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ChoiceColumn"
} -->
