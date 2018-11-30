---
title: tipo de recurso windows10AppsForceUpdateSchedule
description: Programación de actualización de Windows 10 force para aplicaciones
ms.openlocfilehash: 89bbee05c3a76df6999c0d3d16caa591f903c45a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087052"
---
# <a name="windows10appsforceupdateschedule-resource-type"></a><span data-ttu-id="ca9b0-103">tipo de recurso windows10AppsForceUpdateSchedule</span><span class="sxs-lookup"><span data-stu-id="ca9b0-103">windows10AppsForceUpdateSchedule resource type</span></span>

> <span data-ttu-id="ca9b0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ca9b0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ca9b0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca9b0-107">Programación de actualización de Windows 10 force para aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ca9b0-107">Windows 10 force update schedule for Apps</span></span>
## <a name="properties"></a><span data-ttu-id="ca9b0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca9b0-108">Properties</span></span>
|<span data-ttu-id="ca9b0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca9b0-109">Property</span></span>|<span data-ttu-id="ca9b0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca9b0-110">Type</span></span>|<span data-ttu-id="ca9b0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca9b0-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ca9b0-112">startDateTime</span><span class="sxs-lookup"><span data-stu-id="ca9b0-112">startDateTime</span></span>|<span data-ttu-id="ca9b0-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ca9b0-113">DateTimeOffset</span></span>|<span data-ttu-id="ca9b0-114">Reinicie la hora de inicio para la fuerza.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-114">The start time for the force restart.</span></span>|
|<span data-ttu-id="ca9b0-115">recurrence</span><span class="sxs-lookup"><span data-stu-id="ca9b0-115">recurrence</span></span>|[<span data-ttu-id="ca9b0-116">windows10AppsUpdateRecurrence</span><span class="sxs-lookup"><span data-stu-id="ca9b0-116">windows10AppsUpdateRecurrence</span></span>](../resources/intune-deviceconfig-windows10appsupdaterecurrence.md)|<span data-ttu-id="ca9b0-117">Programación de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-117">Recurrence schedule.</span></span> <span data-ttu-id="ca9b0-118">Los valores posibles son: `none`, `daily`, `weekly` y `monthly`.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-118">Possible values are: `none`, `daily`, `weekly`, `monthly`.</span></span>|
|<span data-ttu-id="ca9b0-119">runImmediatelyIfAfterStartDateTime</span><span class="sxs-lookup"><span data-stu-id="ca9b0-119">runImmediatelyIfAfterStartDateTime</span></span>|<span data-ttu-id="ca9b0-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="ca9b0-120">Boolean</span></span>|<span data-ttu-id="ca9b0-121">Si es true, ejecuta la tarea inmediatamente si StartDateTime se encuentra en el pasado, else, se ejecuta a la siguiente repetición.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-121">If true, runs the task immediately if StartDateTime is in the past, else, runs at the next recurrence.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ca9b0-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ca9b0-122">Relationships</span></span>
<span data-ttu-id="ca9b0-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ca9b0-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ca9b0-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ca9b0-124">JSON Representation</span></span>
<span data-ttu-id="ca9b0-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca9b0-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10AppsForceUpdateSchedule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10AppsForceUpdateSchedule",
  "startDateTime": "String (timestamp)",
  "recurrence": "String",
  "runImmediatelyIfAfterStartDateTime": true
}
```





