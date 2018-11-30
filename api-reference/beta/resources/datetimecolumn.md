---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: DateTimeColumn
ms.openlocfilehash: 9854ad35c602ff474604f2ca88e7182c325e797d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083865"
---
# <a name="datetimecolumn-resource-type"></a><span data-ttu-id="9b7fc-102">Tipo de recurso DateTimeColumn</span><span class="sxs-lookup"><span data-stu-id="9b7fc-102">DateTimeColumn resource type</span></span>

> <span data-ttu-id="9b7fc-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b7fc-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9b7fc-105">El recurso **dateTimeColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son fechas u horas.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-105">The **dateTimeColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are dates or times.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9b7fc-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b7fc-106">JSON representation</span></span>

<span data-ttu-id="9b7fc-107">A continuación se incluye una representación JSON de un recurso **dateTimeColumn**.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-107">Here is a JSON representation of a **dateTimeColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.dateTimeColumn" } -->

```json
{
  "displayAs": "default | friendly | standard",
  "format": "dateOnly | dateTime"
}
```

## <a name="properties"></a><span data-ttu-id="9b7fc-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b7fc-108">Properties</span></span>

| <span data-ttu-id="9b7fc-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="9b7fc-109">Property name</span></span>      | <span data-ttu-id="9b7fc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b7fc-110">Type</span></span>               | <span data-ttu-id="9b7fc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b7fc-111">Description</span></span>
|:-------------------|:-------------------|:----------------------------------------------
| <span data-ttu-id="9b7fc-112">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="9b7fc-112">**displayAs**</span></span>      | <span data-ttu-id="9b7fc-113">string</span><span class="sxs-lookup"><span data-stu-id="9b7fc-113">string</span></span>             | <span data-ttu-id="9b7fc-114">Cómo se debe presentar el valor en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-114">How the value should be presented in the UX.</span></span> <span data-ttu-id="9b7fc-115">Debe ser `default`, `friendly` o `standard`.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-115">Must be one of `default`, `friendly`, or `standard`.</span></span> <span data-ttu-id="9b7fc-116">Vea lo que se muestra a continuación para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-116">See below for more details.</span></span> <span data-ttu-id="9b7fc-117">Si no se especifica, se trata como `default`.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-117">If unspecified, treated as `default`.</span></span>
| <span data-ttu-id="9b7fc-118">**format**</span><span class="sxs-lookup"><span data-stu-id="9b7fc-118">**format**</span></span>         | <span data-ttu-id="9b7fc-119">string</span><span class="sxs-lookup"><span data-stu-id="9b7fc-119">string</span></span>             | <span data-ttu-id="9b7fc-120">Indica si el valor debe presentarse solo como una fecha o como fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-120">Indicates whether the value should be presented as a date only or a date and time.</span></span> <span data-ttu-id="9b7fc-121">Debe ser `dateOnly` o `dateTime`</span><span class="sxs-lookup"><span data-stu-id="9b7fc-121">Must be one of `dateOnly` or `dateTime`</span></span>

## <a name="displayas-values"></a><span data-ttu-id="9b7fc-122">Valores displayAs</span><span class="sxs-lookup"><span data-stu-id="9b7fc-122">DisplayAs values</span></span>

| <span data-ttu-id="9b7fc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9b7fc-123">Value</span></span>        | <span data-ttu-id="9b7fc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b7fc-124">Description</span></span>
|:-------------|:--------------------------------------------------------------
| <span data-ttu-id="9b7fc-125">**default**</span><span class="sxs-lookup"><span data-stu-id="9b7fc-125">**default**</span></span>  | <span data-ttu-id="9b7fc-126">Usa la representación predeterminada de la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-126">Uses the default rendering in the UX.</span></span>
| <span data-ttu-id="9b7fc-127">**friendly**</span><span class="sxs-lookup"><span data-stu-id="9b7fc-127">**friendly**</span></span> | <span data-ttu-id="9b7fc-128">Usa una representación relativa descriptiva (p. ej.,</span><span class="sxs-lookup"><span data-stu-id="9b7fc-128">Uses a friendly relative representation (eg.</span></span> <span data-ttu-id="9b7fc-129">"hoy a las 3:00 p. m.")</span><span class="sxs-lookup"><span data-stu-id="9b7fc-129">"today at 3:00 PM")</span></span>
| <span data-ttu-id="9b7fc-130">**standard**</span><span class="sxs-lookup"><span data-stu-id="9b7fc-130">**standard**</span></span> | <span data-ttu-id="9b7fc-131">Usa la representación absoluta estándar (p. ej.</span><span class="sxs-lookup"><span data-stu-id="9b7fc-131">Uses the standard absolute representation (eg.</span></span> <span data-ttu-id="9b7fc-132">"5/10/2017 3:20 p. m.")</span><span class="sxs-lookup"><span data-stu-id="9b7fc-132">"5/10/2017 3:20 PM")</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DateTimeColumn"
} -->
