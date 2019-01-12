---
title: tipo de recurso bookingReminder
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 17cd444b8656c30e8f8966ab14571876ef9354fe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936700"
---
# <a name="bookingreminder-resource-type"></a><span data-ttu-id="a3423-104">tipo de recurso bookingReminder</span><span class="sxs-lookup"><span data-stu-id="a3423-104">bookingReminder resource type</span></span>

 > <span data-ttu-id="a3423-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a3423-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a3423-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a3423-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="a3423-107">Representa cuándo y a quienes se debe enviar un recordatorio de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a3423-107">Represents when and to whom to send an email reminder.</span></span>


## <a name="properties"></a><span data-ttu-id="a3423-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3423-108">Properties</span></span>
| <span data-ttu-id="a3423-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a3423-109">Property</span></span>     | <span data-ttu-id="a3423-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3423-110">Type</span></span>   |<span data-ttu-id="a3423-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3423-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a3423-112">message</span><span class="sxs-lookup"><span data-stu-id="a3423-112">message</span></span>|<span data-ttu-id="a3423-113">String</span><span class="sxs-lookup"><span data-stu-id="a3423-113">String</span></span>|<span data-ttu-id="a3423-114">El mensaje en el aviso.</span><span class="sxs-lookup"><span data-stu-id="a3423-114">The message in the reminder.</span></span>|
|<span data-ttu-id="a3423-115">desplazamiento</span><span class="sxs-lookup"><span data-stu-id="a3423-115">offset</span></span>|<span data-ttu-id="a3423-116">Duración</span><span class="sxs-lookup"><span data-stu-id="a3423-116">Duration</span></span>|<span data-ttu-id="a3423-117">La cantidad de tiempo antes del inicio de una cita que se debe enviar el aviso.</span><span class="sxs-lookup"><span data-stu-id="a3423-117">The amount of time before the start of an appointment that the reminder should be sent.</span></span> <span data-ttu-id="a3423-118">Se mostrará en formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .</span><span class="sxs-lookup"><span data-stu-id="a3423-118">It's denoted in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format.</span></span>|
|<span data-ttu-id="a3423-119">destinatarios</span><span class="sxs-lookup"><span data-stu-id="a3423-119">recipients</span></span>|<span data-ttu-id="a3423-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="a3423-120">String</span></span>| <span data-ttu-id="a3423-121">Las personas que shouold recibir el aviso.</span><span class="sxs-lookup"><span data-stu-id="a3423-121">The persons who shouold receive the reminder.</span></span> <span data-ttu-id="a3423-122">Los valores posibles son: `allAttendees`, `staff` y `customer`.</span><span class="sxs-lookup"><span data-stu-id="a3423-122">Possible values are: `allAttendees`, `staff`, `customer`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a3423-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a3423-123">JSON representation</span></span>

<span data-ttu-id="a3423-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a3423-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingReminder"
}-->

```json
{
  "message": "String",
  "offset": "String (timestamp)",
  "recipients": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingReminder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
