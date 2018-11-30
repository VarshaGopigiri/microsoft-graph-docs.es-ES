---
title: Tipo de recurso windowsUpdateActiveHoursInstall
description: Todavía no documentado
ms.openlocfilehash: c9647cda65d680629fda57e3dfdcbffb3d5d8625
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028723"
---
# <a name="windowsupdateactivehoursinstall-resource-type"></a><span data-ttu-id="8f4b4-103">Tipo de recurso windowsUpdateActiveHoursInstall</span><span class="sxs-lookup"><span data-stu-id="8f4b4-103">windowsUpdateActiveHoursInstall resource type</span></span>

> <span data-ttu-id="8f4b4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8f4b4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8f4b4-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8f4b4-105">Not yet documented</span></span>

<span data-ttu-id="8f4b4-106">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="8f4b4-106">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8f4b4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f4b4-107">Properties</span></span>
|<span data-ttu-id="8f4b4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f4b4-108">Property</span></span>|<span data-ttu-id="8f4b4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f4b4-109">Type</span></span>|<span data-ttu-id="8f4b4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f4b4-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8f4b4-111">activeHoursStart</span><span class="sxs-lookup"><span data-stu-id="8f4b4-111">activeHoursStart</span></span>|<span data-ttu-id="8f4b4-112">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="8f4b4-112">TimeOfDay</span></span>|<span data-ttu-id="8f4b4-113">Inicio de horas activas</span><span class="sxs-lookup"><span data-stu-id="8f4b4-113">Active Hours Start</span></span>|
|<span data-ttu-id="8f4b4-114">activeHoursEnd</span><span class="sxs-lookup"><span data-stu-id="8f4b4-114">activeHoursEnd</span></span>|<span data-ttu-id="8f4b4-115">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="8f4b4-115">TimeOfDay</span></span>|<span data-ttu-id="8f4b4-116">Fin de horas activas</span><span class="sxs-lookup"><span data-stu-id="8f4b4-116">Active Hours End</span></span>|

## <a name="relationships"></a><span data-ttu-id="8f4b4-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8f4b4-117">Relationships</span></span>
<span data-ttu-id="8f4b4-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8f4b4-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8f4b4-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8f4b4-119">JSON Representation</span></span>
<span data-ttu-id="8f4b4-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8f4b4-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUpdateActiveHoursInstall"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdateActiveHoursInstall",
  "activeHoursStart": "String (time of day)",
  "activeHoursEnd": "String (time of day)"
}
```



