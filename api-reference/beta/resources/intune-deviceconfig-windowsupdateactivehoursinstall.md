---
title: Tipo de recurso windowsUpdateActiveHoursInstall
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 797cfc0f9279f0ab232991a95714d31ce37211a3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818427"
---
# <a name="windowsupdateactivehoursinstall-resource-type"></a><span data-ttu-id="4f589-103">Tipo de recurso windowsUpdateActiveHoursInstall</span><span class="sxs-lookup"><span data-stu-id="4f589-103">windowsUpdateActiveHoursInstall resource type</span></span>

> <span data-ttu-id="4f589-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4f589-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4f589-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4f589-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4f589-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4f589-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4f589-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4f589-107">Not yet documented</span></span>

<span data-ttu-id="4f589-108">Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="4f589-108">Inherits from [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="4f589-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f589-109">Properties</span></span>
|<span data-ttu-id="4f589-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4f589-110">Property</span></span>|<span data-ttu-id="4f589-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f589-111">Type</span></span>|<span data-ttu-id="4f589-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f589-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4f589-113">activeHoursStart</span><span class="sxs-lookup"><span data-stu-id="4f589-113">activeHoursStart</span></span>|<span data-ttu-id="4f589-114">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="4f589-114">TimeOfDay</span></span>|<span data-ttu-id="4f589-115">Inicio de horas activas</span><span class="sxs-lookup"><span data-stu-id="4f589-115">Active Hours Start</span></span>|
|<span data-ttu-id="4f589-116">activeHoursEnd</span><span class="sxs-lookup"><span data-stu-id="4f589-116">activeHoursEnd</span></span>|<span data-ttu-id="4f589-117">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="4f589-117">TimeOfDay</span></span>|<span data-ttu-id="4f589-118">Fin de horas activas</span><span class="sxs-lookup"><span data-stu-id="4f589-118">Active Hours End</span></span>|

## <a name="relationships"></a><span data-ttu-id="4f589-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4f589-119">Relationships</span></span>
<span data-ttu-id="4f589-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4f589-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4f589-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4f589-121">JSON Representation</span></span>
<span data-ttu-id="4f589-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4f589-122">Here is a JSON representation of the resource.</span></span>
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





