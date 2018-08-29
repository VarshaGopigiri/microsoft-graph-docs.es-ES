---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: DateTimeColumn
ms.openlocfilehash: 6f2c14d5fa67fa80c869c20081250bfa55e0f5e4
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267832"
---
# <a name="datetimecolumn-resource-type"></a><span data-ttu-id="3a459-102">Tipo de recurso DateTimeColumn</span><span class="sxs-lookup"><span data-stu-id="3a459-102">DateTimeColumn resource type</span></span>

<span data-ttu-id="3a459-103">El recurso **dateTimeColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son fechas u horas.</span><span class="sxs-lookup"><span data-stu-id="3a459-103">The **dateTimeColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values are dates or times.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3a459-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a459-104">JSON representation</span></span>

<span data-ttu-id="3a459-105">A continuación se incluye una representación JSON de un recurso **dateTimeColumn**.</span><span class="sxs-lookup"><span data-stu-id="3a459-105">Here is a JSON representation of a **dateTimeColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.dateTimeColumn" } -->

```json
{
  "displayAs": "default | friendly | standard",
  "format": "dateOnly | dateTime"
}
```

## <a name="properties"></a><span data-ttu-id="3a459-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a459-106">Properties</span></span>

| <span data-ttu-id="3a459-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="3a459-107">Property name</span></span>      | <span data-ttu-id="3a459-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a459-108">Type</span></span>               | <span data-ttu-id="3a459-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a459-109">Description</span></span>
|:-------------------|:-------------------|:----------------------------------------------
| <span data-ttu-id="3a459-110">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="3a459-110">**displayAs**</span></span>      | <span data-ttu-id="3a459-111">cadena</span><span class="sxs-lookup"><span data-stu-id="3a459-111">string</span></span>             | <span data-ttu-id="3a459-112">Cómo se debe presentar el valor en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="3a459-112">How the value should be presented in the UX.</span></span> <span data-ttu-id="3a459-113">Debe ser `default`, `friendly` o `standard`.</span><span class="sxs-lookup"><span data-stu-id="3a459-113">Must be one of `default`, `friendly`, or `standard`.</span></span> <span data-ttu-id="3a459-114">Vea lo que se muestra a continuación para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="3a459-114">See below for more details.</span></span> <span data-ttu-id="3a459-115">Si no se especifica, se trata como `default`.</span><span class="sxs-lookup"><span data-stu-id="3a459-115">If unspecified, treated as `default`.</span></span>
| <span data-ttu-id="3a459-116">**format**</span><span class="sxs-lookup"><span data-stu-id="3a459-116">**format**</span></span>         | <span data-ttu-id="3a459-117">cadena</span><span class="sxs-lookup"><span data-stu-id="3a459-117">string</span></span>             | <span data-ttu-id="3a459-118">Indica si el valor debe presentarse solo como una fecha o como fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="3a459-118">Indicates whether the value should be presented as a date only or a date and time.</span></span> <span data-ttu-id="3a459-119">Debe ser `dateOnly` o `dateTime`</span><span class="sxs-lookup"><span data-stu-id="3a459-119">Must be one of `dateOnly` or `dateTime`</span></span>

## <a name="displayas-options"></a><span data-ttu-id="3a459-120">Opciones de displayAs</span><span class="sxs-lookup"><span data-stu-id="3a459-120">DisplayAs options</span></span>

| <span data-ttu-id="3a459-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3a459-121">Value</span></span>        | <span data-ttu-id="3a459-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a459-122">Description</span></span>
|:-------------|:--------------------------------------------------------------
| <span data-ttu-id="3a459-123">**default**</span><span class="sxs-lookup"><span data-stu-id="3a459-123">**default**</span></span>  | <span data-ttu-id="3a459-124">Usa la representación predeterminada de la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="3a459-124">Uses the default rendering in the UX.</span></span>
| <span data-ttu-id="3a459-125">**friendly**</span><span class="sxs-lookup"><span data-stu-id="3a459-125">**friendly**</span></span> | <span data-ttu-id="3a459-126">Usa una representación relativa descriptiva (p. ej.,</span><span class="sxs-lookup"><span data-stu-id="3a459-126">Uses a friendly relative representation (eg.</span></span> <span data-ttu-id="3a459-127">"hoy a las 3:00 p. m.")</span><span class="sxs-lookup"><span data-stu-id="3a459-127">"today at 3:00 PM")</span></span>
| <span data-ttu-id="3a459-128">**standard**</span><span class="sxs-lookup"><span data-stu-id="3a459-128">**standard**</span></span> | <span data-ttu-id="3a459-129">Usa la representación absoluta estándar (p. ej.</span><span class="sxs-lookup"><span data-stu-id="3a459-129">Uses the standard absolute representation (eg.</span></span> <span data-ttu-id="3a459-130">"5/10/2017 3:20 p. m.")</span><span class="sxs-lookup"><span data-stu-id="3a459-130">"5/10/2017 3:20 PM")</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/choicecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(checkBoxes,dropDownMenu,radioButtons) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/datetimecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(default,friendly,standard) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/datetimecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(dateOnly,dateTime) are in resource, but () are in table"
  ],
  "tocPath": "Resources/DateTimeColumn"
} -->
