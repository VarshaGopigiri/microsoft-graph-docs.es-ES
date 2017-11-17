---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: DateTimeColumn
ms.openlocfilehash: ce5f06b6e0d88324813372c2431b62e6b9105bcb
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="datetimecolumn-resource-type"></a><span data-ttu-id="13a75-102">Tipo de recurso DateTimeColumn</span><span class="sxs-lookup"><span data-stu-id="13a75-102">DateTimeColumn resource type</span></span>

<span data-ttu-id="13a75-103">El recurso **dateTimeColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son fechas u horas.</span><span class="sxs-lookup"><span data-stu-id="13a75-103">The **dateTimeColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values are dates or times.</span></span>

## <a name="json-representation"></a><span data-ttu-id="13a75-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="13a75-104">JSON representation</span></span>

<span data-ttu-id="13a75-105">A continuación se incluye una representación JSON de un recurso **dateTimeColumn**.</span><span class="sxs-lookup"><span data-stu-id="13a75-105">Here is a JSON representation of a **driveItem** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.dateTimeColumn" } -->

```json
{
  "displayAs": "default | friendly | standard",
  "format": "dateOnly | dateTime"
}
```

## <a name="properties"></a><span data-ttu-id="13a75-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13a75-106">Properties</span></span>

| <span data-ttu-id="13a75-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="13a75-107">Property name</span></span>      | <span data-ttu-id="13a75-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="13a75-108">Type</span></span>               | <span data-ttu-id="13a75-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="13a75-109">Description</span></span>
|:-------------------|:-------------------|:----------------------------------------------
| <span data-ttu-id="13a75-110">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="13a75-110">**displayAs**</span></span>      | <span data-ttu-id="13a75-111">string</span><span class="sxs-lookup"><span data-stu-id="13a75-111">string</span></span>             | <span data-ttu-id="13a75-112">Cómo se debe presentar el valor en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="13a75-112">How the value should be presented in the UX.</span></span> <span data-ttu-id="13a75-113">Debe ser `default`, `friendly` o `standard`.</span><span class="sxs-lookup"><span data-stu-id="13a75-113">Must be one of `default`, `friendly`, or `standard`.</span></span> <span data-ttu-id="13a75-114">Vea lo que se muestra a continuación para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="13a75-114">Read below for more details.</span></span> <span data-ttu-id="13a75-115">Si no se especifica, se trata como `default`.</span><span class="sxs-lookup"><span data-stu-id="13a75-115">If unspecified, treated as `default`.</span></span>
| <span data-ttu-id="13a75-116">**format**</span><span class="sxs-lookup"><span data-stu-id="13a75-116">**format**</span></span>         | <span data-ttu-id="13a75-117">string</span><span class="sxs-lookup"><span data-stu-id="13a75-117">string</span></span>             | <span data-ttu-id="13a75-118">Indica si el valor debe presentarse solo como una fecha o como fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="13a75-118">Indicates whether the value should be presented as a date only or a date and time.</span></span> <span data-ttu-id="13a75-119">Debe ser `dateOnly` o `dateTime`</span><span class="sxs-lookup"><span data-stu-id="13a75-119">Must be one of `dateOnly` or `dateTime`</span></span>

## <a name="displayas-values"></a><span data-ttu-id="13a75-120">Valores displayAs</span><span class="sxs-lookup"><span data-stu-id="13a75-120">DisplayAs values</span></span>

| <span data-ttu-id="13a75-121">Valor</span><span class="sxs-lookup"><span data-stu-id="13a75-121">Value</span></span>        | <span data-ttu-id="13a75-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="13a75-122">Description</span></span>
|:-------------|:--------------------------------------------------------------
| <span data-ttu-id="13a75-123">**default**</span><span class="sxs-lookup"><span data-stu-id="13a75-123">**default**</span></span>  | <span data-ttu-id="13a75-124">Usa la representación predeterminada de la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="13a75-124">Uses the default rendering in the UX.</span></span>
| <span data-ttu-id="13a75-125">**friendly**</span><span class="sxs-lookup"><span data-stu-id="13a75-125">**friendly**</span></span> | <span data-ttu-id="13a75-126">Usa una representación relativa descriptiva (p. ej.,</span><span class="sxs-lookup"><span data-stu-id="13a75-126">Uses a friendly relative representation (eg.</span></span> <span data-ttu-id="13a75-127">"hoy a las 15:00")</span><span class="sxs-lookup"><span data-stu-id="13a75-127">"today at 3:00 PM")</span></span>
| <span data-ttu-id="13a75-128">**standard**</span><span class="sxs-lookup"><span data-stu-id="13a75-128">**Standard**</span></span> | <span data-ttu-id="13a75-129">Usa la representación absoluta estándar (p. ej.</span><span class="sxs-lookup"><span data-stu-id="13a75-129">Uses the standard absolute representation (eg.</span></span> <span data-ttu-id="13a75-130">"10/5/2017 15:20")</span><span class="sxs-lookup"><span data-stu-id="13a75-130">"5/10/2017 3:20 PM")</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DateTimeColumn"
} -->
