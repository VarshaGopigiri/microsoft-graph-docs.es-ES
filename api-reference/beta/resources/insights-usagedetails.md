---
title: tipo de recurso usageDetails
description: Tipo complejo que contiene las propiedades de elementos utilizados. Obtener información sobre cuándo obtuvo acceso por última vez el recurso (ver) y modificar (Editar) por el usuario.
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: 466308ad1b6290c2b96335f94c586eb35c6cac28
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950023"
---
# <a name="usagedetails-resource-type"></a><span data-ttu-id="b324c-104">tipo de recurso usageDetails</span><span class="sxs-lookup"><span data-stu-id="b324c-104">usageDetails resource type</span></span>

> <span data-ttu-id="b324c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b324c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b324c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b324c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b324c-107">Tipo complejo que contiene las propiedades de los elementos [se usa](insights-used.md) .</span><span class="sxs-lookup"><span data-stu-id="b324c-107">Complex type containing properties of [Used](insights-used.md) items.</span></span> <span data-ttu-id="b324c-108">Obtener información sobre cuándo obtuvo acceso por última vez el recurso (ver) y modificar (Editar) por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b324c-108">Information on when the resource was last accessed (viewed) and modified (edited) by the user.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b324c-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b324c-109">JSON representation</span></span>

<span data-ttu-id="b324c-110">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b324c-110">Here is a JSON representation of the resource</span></span>

```json
{
  "lastAccessedDateTime": "DateTimeOffset",
  "lastModifiedDateTime": "DateTimeOffset"
}
```

## <a name="properties"></a><span data-ttu-id="b324c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b324c-111">Properties</span></span>

| <span data-ttu-id="b324c-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b324c-112">Property</span></span>              | <span data-ttu-id="b324c-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="b324c-113">Type</span></span>          | <span data-ttu-id="b324c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b324c-114">Description</span></span>  |
| -------------         |---------------| -------------|
| <span data-ttu-id="b324c-115">lastAccessedDateTime</span><span class="sxs-lookup"><span data-stu-id="b324c-115">lastAccessedDateTime</span></span>                  | <span data-ttu-id="b324c-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b324c-116">DateTimeOffset</span></span>        | <span data-ttu-id="b324c-117">Fecha y hora de que último acceso el recurso por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b324c-117">The date and time the resource was last accessed by the user.</span></span> <span data-ttu-id="b324c-118">La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC.</span><span class="sxs-lookup"><span data-stu-id="b324c-118">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="b324c-119">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`.</span><span class="sxs-lookup"><span data-stu-id="b324c-119">For example, midnight UTC on Jan 1, 2014 would look like this: `2014-01-01T00:00:00Z`.</span></span> <span data-ttu-id="b324c-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b324c-120">Read-only.</span></span>                      |
| <span data-ttu-id="b324c-121">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b324c-121">lastModifiedDateTime</span></span>              | <span data-ttu-id="b324c-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b324c-122">DateTimeOffset</span></span>        | <span data-ttu-id="b324c-123">La fecha y hora que se modificó por última vez el recurso por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b324c-123">The date and time the resource was last modified by the user.</span></span> <span data-ttu-id="b324c-124">La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC.</span><span class="sxs-lookup"><span data-stu-id="b324c-124">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="b324c-125">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`.</span><span class="sxs-lookup"><span data-stu-id="b324c-125">For example, midnight UTC on Jan 1, 2014 would look like this: `2014-01-01T00:00:00Z`.</span></span> <span data-ttu-id="b324c-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b324c-126">Read-only.</span></span>       |
