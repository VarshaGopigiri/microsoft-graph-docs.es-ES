---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
localization_priority: Normal
ms.openlocfilehash: 2e0798f558ace72f59a6acccc0cc8ce3eb6e2291
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842549"
---
# <a name="choicecolumn-resource-type"></a><span data-ttu-id="24060-102">Tipo de recurso ChoiceColumn</span><span class="sxs-lookup"><span data-stu-id="24060-102">ChoiceColumn resource type</span></span>

> <span data-ttu-id="24060-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="24060-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="24060-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="24060-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="24060-105">El recurso **choiceColumn** en un recurso [columnDefinition](columndefinition.md) indica que se pueden seleccionar los valores de la columna de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="24060-105">The **choiceColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values can be selected from a list of choices.</span></span>

## <a name="json-representation"></a><span data-ttu-id="24060-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="24060-106">JSON representation</span></span>

<span data-ttu-id="24060-107">A continuación se incluye una representación JSON de un recurso **ChoiceColumn**.</span><span class="sxs-lookup"><span data-stu-id="24060-107">Here is a JSON representation of a **choiceColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.choiceColumn" } -->

```json
{
  "allowTextEntry": true,
  "choices": ["red", "blue", "green"],
  "displayAs": "checkBoxes | dropDownMenu | radioButtons"
}
```

## <a name="properties"></a><span data-ttu-id="24060-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24060-108">Properties</span></span>

| <span data-ttu-id="24060-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="24060-109">Property name</span></span>      | <span data-ttu-id="24060-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="24060-110">Type</span></span>               | <span data-ttu-id="24060-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="24060-111">Description</span></span>
|:-------------------|:-------------------|:----------------------------------------------
| <span data-ttu-id="24060-112">**allowTextEntry**</span><span class="sxs-lookup"><span data-stu-id="24060-112">**allowTextEntry**</span></span> | <span data-ttu-id="24060-113">boolean</span><span class="sxs-lookup"><span data-stu-id="24060-113">boolean</span></span>            | <span data-ttu-id="24060-114">Si es true, permite valores personalizados que no están en las opciones configuradas.</span><span class="sxs-lookup"><span data-stu-id="24060-114">If true, allows custom values that aren't in the configured choices.</span></span>
| <span data-ttu-id="24060-115">**choices**</span><span class="sxs-lookup"><span data-stu-id="24060-115">**choices**</span></span>        | <span data-ttu-id="24060-116">collection(string)</span><span class="sxs-lookup"><span data-stu-id="24060-116">collection(string)</span></span> | <span data-ttu-id="24060-117">La lista de valores disponibles para esta columna.</span><span class="sxs-lookup"><span data-stu-id="24060-117">The list of values available for this column.</span></span>
| <span data-ttu-id="24060-118">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="24060-118">**displayAs**</span></span>      | <span data-ttu-id="24060-119">string</span><span class="sxs-lookup"><span data-stu-id="24060-119">string</span></span>             | <span data-ttu-id="24060-120">Cómo se deben mostrar las opciones en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="24060-120">How the choices are to be presented in the UX.</span></span> <span data-ttu-id="24060-121">Debe ser `checkBoxes`, `dropDownMenu` o `radioButtons`</span><span class="sxs-lookup"><span data-stu-id="24060-121">Must be one of `checkBoxes`, `dropDownMenu`, or `radioButtons`</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ChoiceColumn"
} -->
