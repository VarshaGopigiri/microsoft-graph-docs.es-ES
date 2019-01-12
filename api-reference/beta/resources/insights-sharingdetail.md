---
title: tipo de recurso sharingDetail
description: 'Tipo complejo que contiene las propiedades de los elementos compartidos. '
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: add63a89a451b742778dda1d6d313d58f675a642
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918766"
---
# <a name="sharingdetail-resource-type"></a><span data-ttu-id="144ee-103">tipo de recurso sharingDetail</span><span class="sxs-lookup"><span data-stu-id="144ee-103">sharingDetail resource type</span></span>

> <span data-ttu-id="144ee-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="144ee-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="144ee-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="144ee-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="144ee-106">Tipo complejo que contiene las propiedades de los elementos [compartidos](insights-shared.md) .</span><span class="sxs-lookup"><span data-stu-id="144ee-106">Complex type containing properties of [Shared](insights-shared.md) items.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="144ee-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="144ee-107">JSON representation</span></span>
<span data-ttu-id="144ee-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="144ee-108">Here is a JSON representation of the resource</span></span>

```json
{
  "sharedDateTime": "dateTimeOffset",
  "sharingSubject": "string",
  "sharingType": "string",
  "sharedBy": "insightIdentity",
  "resourceReference": "resourceReference"
}
```

## <a name="properties"></a><span data-ttu-id="144ee-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="144ee-109">Properties</span></span>

| <span data-ttu-id="144ee-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="144ee-110">Property</span></span>              | <span data-ttu-id="144ee-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="144ee-111">Type</span></span>          | <span data-ttu-id="144ee-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="144ee-112">Description</span></span>  |
| -------------         |-----------    | -------------|
| <span data-ttu-id="144ee-113">sharedDateTime</span><span class="sxs-lookup"><span data-stu-id="144ee-113">sharedDateTime</span></span>        | <span data-ttu-id="144ee-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="144ee-114">DateTimeOffset</span></span>| <span data-ttu-id="144ee-115">La fecha y la hora que el archivo por última vez se ha compartido.</span><span class="sxs-lookup"><span data-stu-id="144ee-115">The date and time the file was last shared.</span></span> <span data-ttu-id="144ee-116">La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC.</span><span class="sxs-lookup"><span data-stu-id="144ee-116">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="144ee-117">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`.</span><span class="sxs-lookup"><span data-stu-id="144ee-117">For example, midnight UTC on Jan 1, 2014 would look like this: `2014-01-01T00:00:00Z`.</span></span> <span data-ttu-id="144ee-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="144ee-118">Read-only.</span></span>  |
| <span data-ttu-id="144ee-119">sharingSubject</span><span class="sxs-lookup"><span data-stu-id="144ee-119">sharingSubject</span></span>        | <span data-ttu-id="144ee-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="144ee-120">String</span></span>          | <span data-ttu-id="144ee-121">El asunto con el que se comparte el documento.</span><span class="sxs-lookup"><span data-stu-id="144ee-121">The subject with which the document was shared.</span></span> |
| <span data-ttu-id="144ee-122">sharingType</span><span class="sxs-lookup"><span data-stu-id="144ee-122">sharingType</span></span>             | <span data-ttu-id="144ee-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="144ee-123">String</span></span>        | <span data-ttu-id="144ee-124">Determina la forma en el documento se ha compartido, puede ser un "Vínculo", "Datos adjuntos", "Grupo", "Sitio".</span><span class="sxs-lookup"><span data-stu-id="144ee-124">Determines the way the document was shared, can be by a "Link", "Attachment", "Group", "Site".</span></span>     |
| <span data-ttu-id="144ee-125">sharedBy</span><span class="sxs-lookup"><span data-stu-id="144ee-125">sharedBy</span></span>                | [<span data-ttu-id="144ee-126">insightIdentity</span><span class="sxs-lookup"><span data-stu-id="144ee-126">insightIdentity</span></span>](insights-insightidentity.md)      | <span data-ttu-id="144ee-127">El usuario que comparte el documento.</span><span class="sxs-lookup"><span data-stu-id="144ee-127">The user who shared the document.</span></span>  |
| <span data-ttu-id="144ee-128">sharingReference</span><span class="sxs-lookup"><span data-stu-id="144ee-128">sharingReference</span></span>        | [<span data-ttu-id="144ee-129">resourceReference</span><span class="sxs-lookup"><span data-stu-id="144ee-129">resourceReference</span></span>](insights-resourcereference.md)      |  |
