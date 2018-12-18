---
title: Tipo de recurso windowsUpdateScheduledInstall
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 4a8943fa0275d8b9e5a668be207c90304f22a327
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340918"
---
# <a name="windowsupdatescheduledinstall-resource-type"></a><span data-ttu-id="10f0c-103">Tipo de recurso windowsUpdateScheduledInstall</span><span class="sxs-lookup"><span data-stu-id="10f0c-103">windowsUpdateScheduledInstall resource type</span></span>

> <span data-ttu-id="10f0c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="10f0c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="10f0c-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="10f0c-105">Not yet documented</span></span>

<span data-ttu-id="10f0c-106">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="10f0c-106">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="10f0c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10f0c-107">Properties</span></span>
|<span data-ttu-id="10f0c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10f0c-108">Property</span></span>|<span data-ttu-id="10f0c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="10f0c-109">Type</span></span>|<span data-ttu-id="10f0c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="10f0c-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="10f0c-111">scheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="10f0c-111">scheduledInstallDay</span></span>|[<span data-ttu-id="10f0c-112">weeklySchedule</span><span class="sxs-lookup"><span data-stu-id="10f0c-112">weeklySchedule</span></span>](../resources/intune-deviceconfig-weeklyschedule.md)|<span data-ttu-id="10f0c-113">Programada instalar día de la semana.</span><span class="sxs-lookup"><span data-stu-id="10f0c-113">Scheduled Install Day in week.</span></span> <span data-ttu-id="10f0c-114">Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="10f0c-114">Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="10f0c-115">scheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="10f0c-115">scheduledInstallTime</span></span>|<span data-ttu-id="10f0c-116">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="10f0c-116">TimeOfDay</span></span>|<span data-ttu-id="10f0c-117">Hora de instalación programada durante el día</span><span class="sxs-lookup"><span data-stu-id="10f0c-117">Scheduled Install Time during day</span></span>|

## <a name="relationships"></a><span data-ttu-id="10f0c-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="10f0c-118">Relationships</span></span>
<span data-ttu-id="10f0c-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="10f0c-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="10f0c-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="10f0c-120">JSON Representation</span></span>
<span data-ttu-id="10f0c-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="10f0c-121">Here is a JSON representation of the resource.</span></span>
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



