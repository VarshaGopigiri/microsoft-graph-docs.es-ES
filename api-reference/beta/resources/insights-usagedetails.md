---
title: tipo de recurso usageDetails
description: Tipo complejo que contiene las propiedades de elementos utilizados. Obtener información sobre cuándo obtuvo acceso por última vez el recurso (ver) y modificar (Editar) por el usuario.
ms.openlocfilehash: c74b1436abcfa4993728371a79d2371a667a16d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083035"
---
# <a name="usagedetails-resource-type"></a><span data-ttu-id="b84d9-104">tipo de recurso usageDetails</span><span class="sxs-lookup"><span data-stu-id="b84d9-104">usageDetails resource type</span></span>

> <span data-ttu-id="b84d9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b84d9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b84d9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b84d9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b84d9-107">Tipo complejo que contiene las propiedades de los elementos [se usa](insights-used.md) .</span><span class="sxs-lookup"><span data-stu-id="b84d9-107">Complex type containing properties of [Used](insights-used.md) items.</span></span> <span data-ttu-id="b84d9-108">Obtener información sobre cuándo obtuvo acceso por última vez el recurso (ver) y modificar (Editar) por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b84d9-108">Information on when the resource was last accessed (viewed) and modified (edited) by the user.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b84d9-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b84d9-109">JSON representation</span></span>

<span data-ttu-id="b84d9-110">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b84d9-110">Here is a JSON representation of the resource</span></span>

```json
{
  "lastAccessedDateTime": "DateTimeOffset",
  "lastModifiedDateTime": "DateTimeOffset"
}
```

## <a name="properties"></a><span data-ttu-id="b84d9-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b84d9-111">Properties</span></span>

| <span data-ttu-id="b84d9-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b84d9-112">Property</span></span>              | <span data-ttu-id="b84d9-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="b84d9-113">Type</span></span>          | <span data-ttu-id="b84d9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b84d9-114">Description</span></span>  |
| -------------         |---------------| -------------|
| <span data-ttu-id="b84d9-115">lastAccessedDateTime</span><span class="sxs-lookup"><span data-stu-id="b84d9-115">lastAccessedDateTime</span></span>                  | <span data-ttu-id="b84d9-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b84d9-116">DateTimeOffset</span></span>        | <span data-ttu-id="b84d9-117">Fecha y hora de que último acceso el recurso por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b84d9-117">The date and time the resource was last accessed by the user.</span></span> <span data-ttu-id="b84d9-118">La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC.</span><span class="sxs-lookup"><span data-stu-id="b84d9-118">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="b84d9-119">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`.</span><span class="sxs-lookup"><span data-stu-id="b84d9-119">For example, midnight UTC on Jan 1, 2014 would look like this: `2014-01-01T00:00:00Z`.</span></span> <span data-ttu-id="b84d9-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b84d9-120">Read-only.</span></span>                      |
| <span data-ttu-id="b84d9-121">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b84d9-121">lastModifiedDateTime</span></span>              | <span data-ttu-id="b84d9-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b84d9-122">DateTimeOffset</span></span>        | <span data-ttu-id="b84d9-123">La fecha y hora que se modificó por última vez el recurso por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b84d9-123">The date and time the resource was last modified by the user.</span></span> <span data-ttu-id="b84d9-124">La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC.</span><span class="sxs-lookup"><span data-stu-id="b84d9-124">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="b84d9-125">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`.</span><span class="sxs-lookup"><span data-stu-id="b84d9-125">For example, midnight UTC on Jan 1, 2014 would look like this: `2014-01-01T00:00:00Z`.</span></span> <span data-ttu-id="b84d9-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b84d9-126">Read-only.</span></span>       |