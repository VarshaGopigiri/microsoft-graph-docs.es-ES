---
title: Tipo de recurso windowsUpdateScheduledInstall
description: Todavía no documentado
ms.openlocfilehash: 06e26bfb43691c8774e166a65b36d6ab872d44e1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030080"
---
# <a name="windowsupdatescheduledinstall-resource-type"></a><span data-ttu-id="94771-103">Tipo de recurso windowsUpdateScheduledInstall</span><span class="sxs-lookup"><span data-stu-id="94771-103">windowsUpdateScheduledInstall resource type</span></span>

> <span data-ttu-id="94771-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="94771-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="94771-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="94771-105">Not yet documented</span></span>

<span data-ttu-id="94771-106">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="94771-106">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="94771-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94771-107">Properties</span></span>
|<span data-ttu-id="94771-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="94771-108">Property</span></span>|<span data-ttu-id="94771-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="94771-109">Type</span></span>|<span data-ttu-id="94771-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="94771-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="94771-111">scheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="94771-111">scheduledInstallDay</span></span>|[<span data-ttu-id="94771-112">weeklySchedule</span><span class="sxs-lookup"><span data-stu-id="94771-112">weeklySchedule</span></span>](../resources/intune-deviceconfig-weeklyschedule.md)|<span data-ttu-id="94771-113">Programada instalar día de la semana.</span><span class="sxs-lookup"><span data-stu-id="94771-113">Scheduled Install Day in week.</span></span> <span data-ttu-id="94771-114">Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="94771-114">Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="94771-115">scheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="94771-115">scheduledInstallTime</span></span>|<span data-ttu-id="94771-116">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="94771-116">TimeOfDay</span></span>|<span data-ttu-id="94771-117">Hora de instalación programada durante el día</span><span class="sxs-lookup"><span data-stu-id="94771-117">Scheduled Install Time during day</span></span>|

## <a name="relationships"></a><span data-ttu-id="94771-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="94771-118">Relationships</span></span>
<span data-ttu-id="94771-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="94771-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="94771-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="94771-120">JSON Representation</span></span>
<span data-ttu-id="94771-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="94771-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdateScheduledInstall",
  "scheduledInstallDay": "String",
  "scheduledInstallTime": "String (time of day)"
}
```



