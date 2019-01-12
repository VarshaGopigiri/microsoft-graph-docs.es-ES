---
title: Tipo de recurso deviceManagementSettings
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fda8ac13e97f7c5dd6ed1efda0443b2f898c91c8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959016"
---
# <a name="devicemanagementsettings-resource-type"></a><span data-ttu-id="5bb0e-103">Tipo de recurso deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="5bb0e-103">deviceManagementSettings resource type</span></span>

> <span data-ttu-id="5bb0e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5bb0e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5bb0e-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5bb0e-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="5bb0e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5bb0e-106">Properties</span></span>
|<span data-ttu-id="5bb0e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5bb0e-107">Property</span></span>|<span data-ttu-id="5bb0e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bb0e-108">Type</span></span>|<span data-ttu-id="5bb0e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bb0e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5bb0e-110">deviceComplianceCheckinThresholdDays</span><span class="sxs-lookup"><span data-stu-id="5bb0e-110">deviceComplianceCheckinThresholdDays</span></span>|<span data-ttu-id="5bb0e-111">Int32</span><span class="sxs-lookup"><span data-stu-id="5bb0e-111">Int32</span></span>|<span data-ttu-id="5bb0e-112">El número de días que se permite a un dispositivo continuar sin registrarse para seguir siendo compatible.</span><span class="sxs-lookup"><span data-stu-id="5bb0e-112">The number of days a device is allowed to go without checking in to remain compliant.</span></span> <span data-ttu-id="5bb0e-113">Valores válidos de 0 a 120</span><span class="sxs-lookup"><span data-stu-id="5bb0e-113">Valid values 0 to 120</span></span>|
|<span data-ttu-id="5bb0e-114">isScheduledActionEnabled</span><span class="sxs-lookup"><span data-stu-id="5bb0e-114">isScheduledActionEnabled</span></span>|<span data-ttu-id="5bb0e-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="5bb0e-115">Boolean</span></span>|<span data-ttu-id="5bb0e-116">Es la característica que está o no habilitada para la acción programada para la regla.</span><span class="sxs-lookup"><span data-stu-id="5bb0e-116">Is feature enabled or not for scheduled action for rule.</span></span>|
|<span data-ttu-id="5bb0e-117">secureByDefault</span><span class="sxs-lookup"><span data-stu-id="5bb0e-117">secureByDefault</span></span>|<span data-ttu-id="5bb0e-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="5bb0e-118">Boolean</span></span>|<span data-ttu-id="5bb0e-119">Cuando es true, el dispositivo debe ser no compatible cuando no hay ninguna directiva de cumplimiento dirigida</span><span class="sxs-lookup"><span data-stu-id="5bb0e-119">Device should be noncompliant when there is no compliance policy targeted when this is true</span></span>|

## <a name="relationships"></a><span data-ttu-id="5bb0e-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5bb0e-120">Relationships</span></span>
<span data-ttu-id="5bb0e-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5bb0e-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5bb0e-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5bb0e-122">JSON Representation</span></span>
<span data-ttu-id="5bb0e-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5bb0e-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementSettings",
  "deviceComplianceCheckinThresholdDays": 1024,
  "isScheduledActionEnabled": true,
  "secureByDefault": true
}
```



