---
title: tipo de recurso dailySchedule
description: Programación diaria de ejecución de una secuencia de comandos de administración de dispositivo periódica.
ms.openlocfilehash: 5d517b0bcd15f041b934a0ca936075bc6d3d3741
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088813"
---
# <a name="dailyschedule-resource-type"></a><span data-ttu-id="5ed91-103">tipo de recurso dailySchedule</span><span class="sxs-lookup"><span data-stu-id="5ed91-103">dailySchedule resource type</span></span>

> <span data-ttu-id="5ed91-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ed91-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ed91-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ed91-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5ed91-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5ed91-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5ed91-107">Programación diaria de ejecución de una secuencia de comandos de administración de dispositivo periódica.</span><span class="sxs-lookup"><span data-stu-id="5ed91-107">Daily run schedule of a recurring device management script.</span></span>

<span data-ttu-id="5ed91-108">Hereda de [runSchedule](../resources/intune-devices-runschedule.md)</span><span class="sxs-lookup"><span data-stu-id="5ed91-108">Inherits from [runSchedule](../resources/intune-devices-runschedule.md)</span></span>

## <a name="properties"></a><span data-ttu-id="5ed91-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ed91-109">Properties</span></span>
|<span data-ttu-id="5ed91-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ed91-110">Property</span></span>|<span data-ttu-id="5ed91-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ed91-111">Type</span></span>|<span data-ttu-id="5ed91-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ed91-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5ed91-113">interval</span><span class="sxs-lookup"><span data-stu-id="5ed91-113">interval</span></span>|<span data-ttu-id="5ed91-114">Int32</span><span class="sxs-lookup"><span data-stu-id="5ed91-114">Int32</span></span>|<span data-ttu-id="5ed91-115">Intervalo en número de días</span><span class="sxs-lookup"><span data-stu-id="5ed91-115">Interval in number of days</span></span>|

## <a name="relationships"></a><span data-ttu-id="5ed91-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5ed91-116">Relationships</span></span>
<span data-ttu-id="5ed91-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5ed91-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5ed91-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5ed91-118">JSON Representation</span></span>
<span data-ttu-id="5ed91-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5ed91-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.dailySchedule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.dailySchedule",
  "interval": 1024
}
```




