---
title: tipo de recurso bookingNamedEntity
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: abd5c9e85357caa6ba6cbbd52d67550a463e36e9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985784"
---
# <a name="bookingnamedentity-resource-type"></a><span data-ttu-id="b4239-104">tipo de recurso bookingNamedEntity</span><span class="sxs-lookup"><span data-stu-id="b4239-104">bookingNamedEntity resource type</span></span>

 > <span data-ttu-id="b4239-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b4239-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b4239-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b4239-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="b4239-107">Éste es un tipo base para las entidades de Microsoft Bookings que proporcionan un nombre para mostrar, por ejemplo, [bookingBusiness](bookingbusiness.md), [bookingPerson](bookingperson.md), [bookingService](bookingservice.md).</span><span class="sxs-lookup"><span data-stu-id="b4239-107">This is a base type for Microsoft Bookings entities that provide a display name, for example, [bookingBusiness](bookingbusiness.md), [bookingPerson](bookingperson.md), [bookingService](bookingservice.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b4239-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4239-108">Properties</span></span>
| <span data-ttu-id="b4239-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4239-109">Property</span></span>     | <span data-ttu-id="b4239-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4239-110">Type</span></span>   |<span data-ttu-id="b4239-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4239-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b4239-112">displayName</span><span class="sxs-lookup"><span data-stu-id="b4239-112">displayName</span></span>|<span data-ttu-id="b4239-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4239-113">String</span></span>|<span data-ttu-id="b4239-114">Un nombre para la entidad derivada, las interfaces con los clientes.</span><span class="sxs-lookup"><span data-stu-id="b4239-114">A name for the derived entity, which interfaces with customers.</span></span>|
|<span data-ttu-id="b4239-115">id</span><span class="sxs-lookup"><span data-stu-id="b4239-115">id</span></span>|<span data-ttu-id="b4239-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4239-116">String</span></span>| <span data-ttu-id="b4239-117">El identificador de la entidad derivada.</span><span class="sxs-lookup"><span data-stu-id="b4239-117">The ID for the derived entity.</span></span> <span data-ttu-id="b4239-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b4239-118">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b4239-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b4239-119">Relationships</span></span>
<span data-ttu-id="b4239-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b4239-120">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="b4239-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b4239-121">JSON representation</span></span>

<span data-ttu-id="b4239-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b4239-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingNamedEntity"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingNamedEntity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
