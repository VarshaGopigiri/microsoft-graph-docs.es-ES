---
title: tipo de recurso bookingPerson
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 606e0e0d1d851fac16b25310b278ca524124eb00
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845580"
---
# <a name="bookingperson-resource-type"></a><span data-ttu-id="e2c5a-104">tipo de recurso bookingPerson</span><span class="sxs-lookup"><span data-stu-id="e2c5a-104">bookingPerson resource type</span></span>

 > <span data-ttu-id="e2c5a-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e2c5a-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="e2c5a-107">Éste es un tipo base de una persona en una empresa de Microsoft Bookings, que puede ser un [bookingCustomer](bookingcustomer.md) o [bookingStaffMember](bookingstaffmember.md).</span><span class="sxs-lookup"><span data-stu-id="e2c5a-107">This is a base type for a person in a Microsoft Bookings business, which can be a [bookingCustomer](bookingcustomer.md) or [bookingStaffMember](bookingstaffmember.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e2c5a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2c5a-108">Properties</span></span>
| <span data-ttu-id="e2c5a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2c5a-109">Property</span></span>     | <span data-ttu-id="e2c5a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-110">Type</span></span>   |<span data-ttu-id="e2c5a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2c5a-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e2c5a-112">displayName</span><span class="sxs-lookup"><span data-stu-id="e2c5a-112">displayName</span></span>|<span data-ttu-id="e2c5a-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2c5a-113">String</span></span>|<span data-ttu-id="e2c5a-114">Un nombre para la entidad derivada, las interfaces con los clientes.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-114">A name for the derived entity, which interfaces with customers.</span></span>|
|<span data-ttu-id="e2c5a-115">emailAddress</span><span class="sxs-lookup"><span data-stu-id="e2c5a-115">emailAddress</span></span>|<span data-ttu-id="e2c5a-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2c5a-116">String</span></span>|<span data-ttu-id="e2c5a-117">La dirección de correo electrónico de la persona.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-117">The email address of the person.</span></span>|
|<span data-ttu-id="e2c5a-118">id</span><span class="sxs-lookup"><span data-stu-id="e2c5a-118">id</span></span>|<span data-ttu-id="e2c5a-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2c5a-119">String</span></span>| <span data-ttu-id="e2c5a-120">El identificador de la entidad derivada.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-120">The ID for the derived entity.</span></span> <span data-ttu-id="e2c5a-121">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-121">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e2c5a-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e2c5a-122">Relationships</span></span>
<span data-ttu-id="e2c5a-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e2c5a-123">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e2c5a-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2c5a-124">JSON representation</span></span>

<span data-ttu-id="e2c5a-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e2c5a-125">The following is a JSON representation of the resource.</span></span>

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
