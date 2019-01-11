---
title: tipo de recurso bookingReminder
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 1f1708d4ac9606ad5c862cb9b1bc73e1ddcfec4a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853868"
---
# <a name="bookingreminder-resource-type"></a><span data-ttu-id="9052d-104">tipo de recurso bookingReminder</span><span class="sxs-lookup"><span data-stu-id="9052d-104">bookingReminder resource type</span></span>

 > <span data-ttu-id="9052d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9052d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9052d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9052d-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="9052d-107">Representa cuándo y a quienes se debe enviar un recordatorio de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9052d-107">Represents when and to whom to send an email reminder.</span></span>


## <a name="properties"></a><span data-ttu-id="9052d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9052d-108">Properties</span></span>
| <span data-ttu-id="9052d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9052d-109">Property</span></span>     | <span data-ttu-id="9052d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9052d-110">Type</span></span>   |<span data-ttu-id="9052d-111">Description</span><span class="sxs-lookup"><span data-stu-id="9052d-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9052d-112">message</span><span class="sxs-lookup"><span data-stu-id="9052d-112">message</span></span>|<span data-ttu-id="9052d-113">String</span><span class="sxs-lookup"><span data-stu-id="9052d-113">String</span></span>|<span data-ttu-id="9052d-114">El mensaje en el aviso.</span><span class="sxs-lookup"><span data-stu-id="9052d-114">The message in the reminder.</span></span>|
|<span data-ttu-id="9052d-115">desplazamiento</span><span class="sxs-lookup"><span data-stu-id="9052d-115">offset</span></span>|<span data-ttu-id="9052d-116">Duración</span><span class="sxs-lookup"><span data-stu-id="9052d-116">Duration</span></span>|<span data-ttu-id="9052d-117">La cantidad de tiempo antes del inicio de una cita que se debe enviar el aviso.</span><span class="sxs-lookup"><span data-stu-id="9052d-117">The amount of time before the start of an appointment that the reminder should be sent.</span></span> <span data-ttu-id="9052d-118">Se mostrará en formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .</span><span class="sxs-lookup"><span data-stu-id="9052d-118">It's denoted in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format.</span></span>|
|<span data-ttu-id="9052d-119">destinatarios</span><span class="sxs-lookup"><span data-stu-id="9052d-119">recipients</span></span>|<span data-ttu-id="9052d-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="9052d-120">String</span></span>| <span data-ttu-id="9052d-121">Las personas que shouold recibir el aviso.</span><span class="sxs-lookup"><span data-stu-id="9052d-121">The persons who shouold receive the reminder.</span></span> <span data-ttu-id="9052d-122">Los valores posibles son: `allAttendees`, `staff` y `customer`.</span><span class="sxs-lookup"><span data-stu-id="9052d-122">Possible values are: `allAttendees`, `staff`, `customer`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9052d-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9052d-123">JSON representation</span></span>

<span data-ttu-id="9052d-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9052d-124">The following is a JSON representation of the resource.</span></span>

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
