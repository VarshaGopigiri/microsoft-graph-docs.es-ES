---
title: Tipo de recurso windowsUpdateScheduledInstall
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 55a53c169f60361af1f695aa07452c4e4a60bedf
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301648"
---
# <a name="windowsupdatescheduledinstall-resource-type"></a><span data-ttu-id="f82f0-103">Tipo de recurso windowsUpdateScheduledInstall</span><span class="sxs-lookup"><span data-stu-id="f82f0-103">windowsUpdateScheduledInstall resource type</span></span>

> <span data-ttu-id="f82f0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f82f0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f82f0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f82f0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f82f0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f82f0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f82f0-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f82f0-107">Not yet documented</span></span>

<span data-ttu-id="f82f0-108">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="f82f0-108">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="f82f0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f82f0-109">Properties</span></span>
|<span data-ttu-id="f82f0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f82f0-110">Property</span></span>|<span data-ttu-id="f82f0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f82f0-111">Type</span></span>|<span data-ttu-id="f82f0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f82f0-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f82f0-113">scheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="f82f0-113">scheduledInstallDay</span></span>|[<span data-ttu-id="f82f0-114">weeklySchedule</span><span class="sxs-lookup"><span data-stu-id="f82f0-114">weeklySchedule</span></span>](../resources/intune-deviceconfig-weeklyschedule.md)|<span data-ttu-id="f82f0-115">Programada instalar día de la semana.</span><span class="sxs-lookup"><span data-stu-id="f82f0-115">Scheduled Install Day in week.</span></span> <span data-ttu-id="f82f0-116">Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="f82f0-116">Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="f82f0-117">scheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="f82f0-117">scheduledInstallTime</span></span>|<span data-ttu-id="f82f0-118">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="f82f0-118">TimeOfDay</span></span>|<span data-ttu-id="f82f0-119">Hora de instalación programada durante el día</span><span class="sxs-lookup"><span data-stu-id="f82f0-119">Scheduled Install Time during day</span></span>|

## <a name="relationships"></a><span data-ttu-id="f82f0-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f82f0-120">Relationships</span></span>
<span data-ttu-id="f82f0-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f82f0-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f82f0-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f82f0-122">JSON Representation</span></span>
<span data-ttu-id="f82f0-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f82f0-123">Here is a JSON representation of the resource.</span></span>
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





