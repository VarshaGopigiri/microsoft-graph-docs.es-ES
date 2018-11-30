---
title: tipo de recurso bookingReminder
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: f5f7b30c296433dd96ffa14a75e3f0286e8a16a1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087342"
---
# <a name="bookingreminder-resource-type"></a><span data-ttu-id="89cd5-104">tipo de recurso bookingReminder</span><span class="sxs-lookup"><span data-stu-id="89cd5-104">bookingReminder resource type</span></span>

 > <span data-ttu-id="89cd5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="89cd5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="89cd5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="89cd5-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="89cd5-107">Representa cuándo y a quienes se debe enviar un recordatorio de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="89cd5-107">Represents when and to whom to send an email reminder.</span></span>


## <a name="properties"></a><span data-ttu-id="89cd5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89cd5-108">Properties</span></span>
| <span data-ttu-id="89cd5-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89cd5-109">Property</span></span>     | <span data-ttu-id="89cd5-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="89cd5-110">Type</span></span>   |<span data-ttu-id="89cd5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="89cd5-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="89cd5-112">message</span><span class="sxs-lookup"><span data-stu-id="89cd5-112">message</span></span>|<span data-ttu-id="89cd5-113">String</span><span class="sxs-lookup"><span data-stu-id="89cd5-113">String</span></span>|<span data-ttu-id="89cd5-114">El mensaje en el aviso.</span><span class="sxs-lookup"><span data-stu-id="89cd5-114">The message in the reminder.</span></span>|
|<span data-ttu-id="89cd5-115">desplazamiento</span><span class="sxs-lookup"><span data-stu-id="89cd5-115">offset</span></span>|<span data-ttu-id="89cd5-116">Duración</span><span class="sxs-lookup"><span data-stu-id="89cd5-116">Duration</span></span>|<span data-ttu-id="89cd5-117">La cantidad de tiempo antes del inicio de una cita que se debe enviar el aviso.</span><span class="sxs-lookup"><span data-stu-id="89cd5-117">The amount of time before the start of an appointment that the reminder should be sent.</span></span> <span data-ttu-id="89cd5-118">Se mostrará en formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .</span><span class="sxs-lookup"><span data-stu-id="89cd5-118">It's denoted in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format.</span></span>|
|<span data-ttu-id="89cd5-119">destinatarios</span><span class="sxs-lookup"><span data-stu-id="89cd5-119">recipients</span></span>|<span data-ttu-id="89cd5-120">String</span><span class="sxs-lookup"><span data-stu-id="89cd5-120">String</span></span>| <span data-ttu-id="89cd5-121">Las personas que shouold recibir el aviso.</span><span class="sxs-lookup"><span data-stu-id="89cd5-121">The persons who shouold receive the reminder.</span></span> <span data-ttu-id="89cd5-122">Los valores posibles son: `allAttendees`, `staff` y `customer`.</span><span class="sxs-lookup"><span data-stu-id="89cd5-122">Possible values are: `allAttendees`, `staff`, `customer`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="89cd5-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="89cd5-123">JSON representation</span></span>

<span data-ttu-id="89cd5-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="89cd5-124">The following is a JSON representation of the resource.</span></span>

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