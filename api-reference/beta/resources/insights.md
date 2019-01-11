---
title: tipo de recurso de conocimientos
description: Perspectivas son relaciones calculadas utilizando análisis avanzado y técnicas de aprendizaje de una máquina. Por ejemplo, puede identificar documentos de OneDrive tendencias alrededor de los usuarios.
author: simonhult
localization_priority: Priority
ms.openlocfilehash: 9d7a1f141e3b6834edfa784a509a2de7968650d1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878095"
---
# <a name="insights-resource-type"></a><span data-ttu-id="f3b56-104">tipo de recurso de conocimientos</span><span class="sxs-lookup"><span data-stu-id="f3b56-104">insights resource type</span></span>

> <span data-ttu-id="f3b56-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3b56-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3b56-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3b56-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f3b56-107">Perspectivas son relaciones calculadas utilizando análisis avanzado y técnicas de aprendizaje de una máquina.</span><span class="sxs-lookup"><span data-stu-id="f3b56-107">Insights are relationships calculated using advanced analytics and machine learning techniques.</span></span> <span data-ttu-id="f3b56-108">Por ejemplo, puede identificar documentos de OneDrive tendencias alrededor de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f3b56-108">You can, for example, identify OneDrive documents trending around users.</span></span>

<span data-ttu-id="f3b56-109">Perspectivas se devuelven por las API siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3b56-109">Insights are returned by the following APIs:</span></span>

- <span data-ttu-id="f3b56-110">[Tendencias](insights-trending.md) de - devuelve documentos de OneDrive y de los sitios de SharePoint tendencias alrededor de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f3b56-110">[Trending](insights-trending.md) - returns documents from OneDrive and from SharePoint sites trending around a user.</span></span>
- <span data-ttu-id="f3b56-111">[Se usa](insights-used.md) - devuelve documentos, ver y modificar por un usuario.</span><span class="sxs-lookup"><span data-stu-id="f3b56-111">[Used](insights-used.md) - returns documents viewed and modified by a user.</span></span> <span data-ttu-id="f3b56-112">Incluye documentos que el usuario usado en OneDrive para la empresa, SharePoint, que se abren como datos adjuntos de correo electrónico y como datos adjuntos de vínculo de orígenes como cuadro de lista desplegable y unidad de Google.</span><span class="sxs-lookup"><span data-stu-id="f3b56-112">Includes documents the user used in OneDrive for Business, SharePoint, opened as email attachments, and as link attachments from sources like Box, DropBox and Google Drive.</span></span>
- <span data-ttu-id="f3b56-113">[Shared](insights-shared.md) - devuelve documentos compartidos con un usuario.</span><span class="sxs-lookup"><span data-stu-id="f3b56-113">[Shared](insights-shared.md) - returns documents shared with a user.</span></span> <span data-ttu-id="f3b56-114">Documentos se pueden compartir como datos adjuntos de correo electrónico o como OneDrive for Business vincula enviados en correos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="f3b56-114">Documents can be shared as email attachments or as OneDrive for Business links sent in emails.</span></span>

<span data-ttu-id="f3b56-115">Se devuelve cada insight con un `resourceVisualization` y `resourceReference` el tipo de valor de tipo complejo (CVT).</span><span class="sxs-lookup"><span data-stu-id="f3b56-115">Each insight is returned with a `resourceVisualization` and `resourceReference` complex value type (CVT).</span></span> <span data-ttu-id="f3b56-116">El resourceVisualization CVT contiene propiedades como `title` y `previewImageUrl`.</span><span class="sxs-lookup"><span data-stu-id="f3b56-116">The resourceVisualization CVT contains properties such as `title` and `previewImageUrl`.</span></span> <span data-ttu-id="f3b56-117">Microsoft utiliza las propiedades de visualización para representar los archivos en experiencias como Office profundizar.</span><span class="sxs-lookup"><span data-stu-id="f3b56-117">Microsoft uses the visualization properties to render the files in experiences like Office Delve.</span></span>

## <a name="relationships"></a><span data-ttu-id="f3b56-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f3b56-118">Relationships</span></span>

| <span data-ttu-id="f3b56-119">Relación</span><span class="sxs-lookup"><span data-stu-id="f3b56-119">Relationship</span></span>      | <span data-ttu-id="f3b56-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3b56-120">Type</span></span>          | <span data-ttu-id="f3b56-121">Description</span><span class="sxs-lookup"><span data-stu-id="f3b56-121">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="f3b56-122">tendencias</span><span class="sxs-lookup"><span data-stu-id="f3b56-122">trending</span></span>      | <span data-ttu-id="f3b56-123">Colección de [tendencias](insights-trending.md)</span><span class="sxs-lookup"><span data-stu-id="f3b56-123">[Trending](insights-trending.md) collection</span></span>       | <span data-ttu-id="f3b56-124">Identificación de documentos de tendencias de relación calculada.</span><span class="sxs-lookup"><span data-stu-id="f3b56-124">Calculated relationship identifying trending documents.</span></span> <span data-ttu-id="f3b56-125">Tendencias de documentos pueden almacenarse en OneDrive o en sitios de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f3b56-125">Trending documents can be stored in OneDrive or in SharePoint sites.</span></span>   |
| <span data-ttu-id="f3b56-126">used</span><span class="sxs-lookup"><span data-stu-id="f3b56-126">used</span></span>      | <span data-ttu-id="f3b56-127">Colección [se usa](insights-used.md)</span><span class="sxs-lookup"><span data-stu-id="f3b56-127">[Used](insights-used.md) collection</span></span>       | <span data-ttu-id="f3b56-128">Calcula la relación de identificación de documentos, ver y modificar por un usuario.</span><span class="sxs-lookup"><span data-stu-id="f3b56-128">Calculated relationship identifying documents viewed and modified by a user.</span></span> <span data-ttu-id="f3b56-129">Incluye documentos que el usuario usado en OneDrive para la empresa, SharePoint, que se abren como datos adjuntos de correo electrónico y como datos adjuntos de vínculo de orígenes como cuadro de lista desplegable y unidad de Google.</span><span class="sxs-lookup"><span data-stu-id="f3b56-129">Includes documents the user used in OneDrive for Business, SharePoint, opened as email attachments, and as link attachments from sources like Box, DropBox and Google Drive.</span></span>  |
| <span data-ttu-id="f3b56-130">compartido</span><span class="sxs-lookup"><span data-stu-id="f3b56-130">shared</span></span>        | <span data-ttu-id="f3b56-131">Colección [compartidos](insights-shared.md)</span><span class="sxs-lookup"><span data-stu-id="f3b56-131">[Shared](insights-shared.md) collection</span></span>       | <span data-ttu-id="f3b56-132">Identificación de documentos compartidos con un usuario de relación calculada.</span><span class="sxs-lookup"><span data-stu-id="f3b56-132">Calculated relationship identifying documents shared with a user.</span></span> <span data-ttu-id="f3b56-133">Documentos se pueden compartir como datos adjuntos de correo electrónico o como OneDrive for Business vincula enviados en correos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="f3b56-133">Documents can be shared as email attachments or as OneDrive for Business links sent in emails.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="f3b56-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f3b56-134">JSON representation</span></span>

<span data-ttu-id="f3b56-135">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f3b56-135">Here is a JSON representation of the resource</span></span>
```json
{
  "trending": [ { "@odata.type": "microsoft.graph.trending" } ],
  "used": [ { "@odata.type": "microsoft.graph.used" } ],
  "shared": [ { "@odata.type": "microsoft.graph.shared" } ]
}
```
