---
title: tipo de recurso hourlySchedule
description: Cada hora, ejecute la programación de una secuencia de comandos de administración de dispositivo periódica.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 004481786fd21ad04e0adbe4e16d3174fc6cc2f4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951890"
---
# <a name="hourlyschedule-resource-type"></a><span data-ttu-id="8a495-103">tipo de recurso hourlySchedule</span><span class="sxs-lookup"><span data-stu-id="8a495-103">hourlySchedule resource type</span></span>

> <span data-ttu-id="8a495-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a495-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a495-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a495-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8a495-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a495-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a495-107">Cada hora, ejecute la programación de una secuencia de comandos de administración de dispositivo periódica.</span><span class="sxs-lookup"><span data-stu-id="8a495-107">Hourly run schedule of a recurring device management script.</span></span>

<span data-ttu-id="8a495-108">Hereda de [runSchedule](../resources/intune-devices-runschedule.md)</span><span class="sxs-lookup"><span data-stu-id="8a495-108">Inherits from [runSchedule](../resources/intune-devices-runschedule.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8a495-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a495-109">Properties</span></span>
|<span data-ttu-id="8a495-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a495-110">Property</span></span>|<span data-ttu-id="8a495-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a495-111">Type</span></span>|<span data-ttu-id="8a495-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a495-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a495-113">interval</span><span class="sxs-lookup"><span data-stu-id="8a495-113">interval</span></span>|<span data-ttu-id="8a495-114">Int32</span><span class="sxs-lookup"><span data-stu-id="8a495-114">Int32</span></span>|<span data-ttu-id="8a495-115">Intervalo en el número de horas</span><span class="sxs-lookup"><span data-stu-id="8a495-115">Interval in number of hours</span></span>|

## <a name="relationships"></a><span data-ttu-id="8a495-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8a495-116">Relationships</span></span>
<span data-ttu-id="8a495-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8a495-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8a495-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8a495-118">JSON Representation</span></span>
<span data-ttu-id="8a495-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8a495-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.hourlySchedule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.hourlySchedule",
  "interval": 1024
}
```





