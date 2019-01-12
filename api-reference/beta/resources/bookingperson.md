---
title: tipo de recurso bookingPerson
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: e39fbbf12909e7a4d29c95e22896df081522a7d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990113"
---
# <a name="bookingperson-resource-type"></a><span data-ttu-id="696c6-104">tipo de recurso bookingPerson</span><span class="sxs-lookup"><span data-stu-id="696c6-104">bookingPerson resource type</span></span>

 > <span data-ttu-id="696c6-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="696c6-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="696c6-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="696c6-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="696c6-107">Éste es un tipo base de una persona en una empresa de Microsoft Bookings, que puede ser un [bookingCustomer](bookingcustomer.md) o [bookingStaffMember](bookingstaffmember.md).</span><span class="sxs-lookup"><span data-stu-id="696c6-107">This is a base type for a person in a Microsoft Bookings business, which can be a [bookingCustomer](bookingcustomer.md) or [bookingStaffMember](bookingstaffmember.md).</span></span>

## <a name="properties"></a><span data-ttu-id="696c6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="696c6-108">Properties</span></span>
| <span data-ttu-id="696c6-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="696c6-109">Property</span></span>     | <span data-ttu-id="696c6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="696c6-110">Type</span></span>   |<span data-ttu-id="696c6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="696c6-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="696c6-112">displayName</span><span class="sxs-lookup"><span data-stu-id="696c6-112">displayName</span></span>|<span data-ttu-id="696c6-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="696c6-113">String</span></span>|<span data-ttu-id="696c6-114">Un nombre para la entidad derivada, las interfaces con los clientes.</span><span class="sxs-lookup"><span data-stu-id="696c6-114">A name for the derived entity, which interfaces with customers.</span></span>|
|<span data-ttu-id="696c6-115">emailAddress</span><span class="sxs-lookup"><span data-stu-id="696c6-115">emailAddress</span></span>|<span data-ttu-id="696c6-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="696c6-116">String</span></span>|<span data-ttu-id="696c6-117">La dirección de correo electrónico de la persona.</span><span class="sxs-lookup"><span data-stu-id="696c6-117">The email address of the person.</span></span>|
|<span data-ttu-id="696c6-118">id</span><span class="sxs-lookup"><span data-stu-id="696c6-118">id</span></span>|<span data-ttu-id="696c6-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="696c6-119">String</span></span>| <span data-ttu-id="696c6-120">El identificador de la entidad derivada.</span><span class="sxs-lookup"><span data-stu-id="696c6-120">The ID for the derived entity.</span></span> <span data-ttu-id="696c6-121">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="696c6-121">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="696c6-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="696c6-122">Relationships</span></span>
<span data-ttu-id="696c6-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="696c6-123">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="696c6-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="696c6-124">JSON representation</span></span>

<span data-ttu-id="696c6-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="696c6-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingPerson"
}-->

```json
{
  "displayName": "String",
  "emailAddress": "String",
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingPerson resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
