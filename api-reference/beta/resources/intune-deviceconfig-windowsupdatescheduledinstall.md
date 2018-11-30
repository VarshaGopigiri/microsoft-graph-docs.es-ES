---
title: Tipo de recurso windowsUpdateScheduledInstall
description: Todavía no documentado
ms.openlocfilehash: 9f39a9716efed39529c54eaddc62cde075b51954
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085208"
---
# <a name="windowsupdatescheduledinstall-resource-type"></a><span data-ttu-id="01fab-103">Tipo de recurso windowsUpdateScheduledInstall</span><span class="sxs-lookup"><span data-stu-id="01fab-103">windowsUpdateScheduledInstall resource type</span></span>

> <span data-ttu-id="01fab-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01fab-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01fab-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01fab-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="01fab-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01fab-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01fab-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01fab-107">Not yet documented</span></span>

<span data-ttu-id="01fab-108">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="01fab-108">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="01fab-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01fab-109">Properties</span></span>
|<span data-ttu-id="01fab-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01fab-110">Property</span></span>|<span data-ttu-id="01fab-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="01fab-111">Type</span></span>|<span data-ttu-id="01fab-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="01fab-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01fab-113">scheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="01fab-113">scheduledInstallDay</span></span>|[<span data-ttu-id="01fab-114">weeklySchedule</span><span class="sxs-lookup"><span data-stu-id="01fab-114">weeklySchedule</span></span>](../resources/intune-deviceconfig-weeklyschedule.md)|<span data-ttu-id="01fab-115">Programada instalar día de la semana.</span><span class="sxs-lookup"><span data-stu-id="01fab-115">Scheduled Install Day in week.</span></span> <span data-ttu-id="01fab-116">Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="01fab-116">Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="01fab-117">scheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="01fab-117">scheduledInstallTime</span></span>|<span data-ttu-id="01fab-118">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="01fab-118">TimeOfDay</span></span>|<span data-ttu-id="01fab-119">Hora de instalación programada durante el día</span><span class="sxs-lookup"><span data-stu-id="01fab-119">Scheduled Install Time during day</span></span>|

## <a name="relationships"></a><span data-ttu-id="01fab-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="01fab-120">Relationships</span></span>
<span data-ttu-id="01fab-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="01fab-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="01fab-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="01fab-122">JSON Representation</span></span>
<span data-ttu-id="01fab-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="01fab-123">Here is a JSON representation of the resource.</span></span>
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





