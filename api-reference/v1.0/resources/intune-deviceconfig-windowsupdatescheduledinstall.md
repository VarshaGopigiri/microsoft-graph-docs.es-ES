---
title: Tipo de recurso windowsUpdateScheduledInstall
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 19e0ced371108103398e26c6067f4ce3b3ab67e7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806408"
---
# <a name="windowsupdatescheduledinstall-resource-type"></a><span data-ttu-id="0b79b-103">Tipo de recurso windowsUpdateScheduledInstall</span><span class="sxs-lookup"><span data-stu-id="0b79b-103">windowsUpdateScheduledInstall resource type</span></span>

> <span data-ttu-id="0b79b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0b79b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0b79b-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0b79b-105">Not yet documented</span></span>

<span data-ttu-id="0b79b-106">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="0b79b-106">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="0b79b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b79b-107">Properties</span></span>
|<span data-ttu-id="0b79b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b79b-108">Property</span></span>|<span data-ttu-id="0b79b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b79b-109">Type</span></span>|<span data-ttu-id="0b79b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b79b-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0b79b-111">scheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="0b79b-111">scheduledInstallDay</span></span>|[<span data-ttu-id="0b79b-112">weeklySchedule</span><span class="sxs-lookup"><span data-stu-id="0b79b-112">weeklySchedule</span></span>](../resources/intune-deviceconfig-weeklyschedule.md)|<span data-ttu-id="0b79b-113">Programada instalar día de la semana.</span><span class="sxs-lookup"><span data-stu-id="0b79b-113">Scheduled Install Day in week.</span></span> <span data-ttu-id="0b79b-114">Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="0b79b-114">Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="0b79b-115">scheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="0b79b-115">scheduledInstallTime</span></span>|<span data-ttu-id="0b79b-116">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="0b79b-116">TimeOfDay</span></span>|<span data-ttu-id="0b79b-117">Hora de instalación programada durante el día</span><span class="sxs-lookup"><span data-stu-id="0b79b-117">Scheduled Install Time during day</span></span>|

## <a name="relationships"></a><span data-ttu-id="0b79b-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0b79b-118">Relationships</span></span>
<span data-ttu-id="0b79b-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0b79b-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0b79b-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0b79b-120">JSON Representation</span></span>
<span data-ttu-id="0b79b-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0b79b-121">Here is a JSON representation of the resource.</span></span>
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



