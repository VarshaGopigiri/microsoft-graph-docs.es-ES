---
title: Tipo de recurso windowsUpdateActiveHoursInstall
description: Todavía no documentado
ms.openlocfilehash: 7a40a791a9a00d7cfd60287bade1759592e1bcf2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089686"
---
# <a name="windowsupdateactivehoursinstall-resource-type"></a><span data-ttu-id="33407-103">Tipo de recurso windowsUpdateActiveHoursInstall</span><span class="sxs-lookup"><span data-stu-id="33407-103">windowsUpdateActiveHoursInstall resource type</span></span>

> <span data-ttu-id="33407-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="33407-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="33407-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="33407-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="33407-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="33407-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="33407-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="33407-107">Not yet documented</span></span>

<span data-ttu-id="33407-108">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="33407-108">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="33407-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33407-109">Properties</span></span>
|<span data-ttu-id="33407-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33407-110">Property</span></span>|<span data-ttu-id="33407-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="33407-111">Type</span></span>|<span data-ttu-id="33407-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="33407-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="33407-113">activeHoursStart</span><span class="sxs-lookup"><span data-stu-id="33407-113">activeHoursStart</span></span>|<span data-ttu-id="33407-114">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="33407-114">TimeOfDay</span></span>|<span data-ttu-id="33407-115">Inicio de horas activas</span><span class="sxs-lookup"><span data-stu-id="33407-115">Active Hours Start</span></span>|
|<span data-ttu-id="33407-116">activeHoursEnd</span><span class="sxs-lookup"><span data-stu-id="33407-116">activeHoursEnd</span></span>|<span data-ttu-id="33407-117">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="33407-117">TimeOfDay</span></span>|<span data-ttu-id="33407-118">Fin de horas activas</span><span class="sxs-lookup"><span data-stu-id="33407-118">Active Hours End</span></span>|

## <a name="relationships"></a><span data-ttu-id="33407-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="33407-119">Relationships</span></span>
<span data-ttu-id="33407-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="33407-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="33407-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="33407-121">JSON Representation</span></span>
<span data-ttu-id="33407-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="33407-122">Here is a JSON representation of the resource.</span></span>
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





