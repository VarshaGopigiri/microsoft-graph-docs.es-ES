---
title: Tipo de recurso deviceManagementSettings
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 9e444f0a92a2e28dfa571c51f08c886537701f3a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343613"
---
# <a name="devicemanagementsettings-resource-type"></a><span data-ttu-id="2c7c2-103">Tipo de recurso deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="2c7c2-103">deviceManagementSettings resource type</span></span>

> <span data-ttu-id="2c7c2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2c7c2-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2c7c2-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="2c7c2-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c7c2-106">Properties</span></span>
|<span data-ttu-id="2c7c2-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c7c2-107">Property</span></span>|<span data-ttu-id="2c7c2-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c7c2-108">Type</span></span>|<span data-ttu-id="2c7c2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c7c2-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2c7c2-110">deviceComplianceCheckinThresholdDays</span><span class="sxs-lookup"><span data-stu-id="2c7c2-110">deviceComplianceCheckinThresholdDays</span></span>|<span data-ttu-id="2c7c2-111">Int32</span><span class="sxs-lookup"><span data-stu-id="2c7c2-111">Int32</span></span>|<span data-ttu-id="2c7c2-112">El número de días que se permite a un dispositivo continuar sin registrarse para seguir siendo compatible.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-112">The number of days a device is allowed to go without checking in to remain compliant.</span></span> <span data-ttu-id="2c7c2-113">Valores válidos de 0 a 120</span><span class="sxs-lookup"><span data-stu-id="2c7c2-113">Valid values 0 to 120</span></span>|
|<span data-ttu-id="2c7c2-114">isScheduledActionEnabled</span><span class="sxs-lookup"><span data-stu-id="2c7c2-114">isScheduledActionEnabled</span></span>|<span data-ttu-id="2c7c2-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="2c7c2-115">Boolean</span></span>|<span data-ttu-id="2c7c2-116">Es la característica que está o no habilitada para la acción programada para la regla.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-116">Is feature enabled or not for scheduled action for rule.</span></span>|
|<span data-ttu-id="2c7c2-117">secureByDefault</span><span class="sxs-lookup"><span data-stu-id="2c7c2-117">secureByDefault</span></span>|<span data-ttu-id="2c7c2-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="2c7c2-118">Boolean</span></span>|<span data-ttu-id="2c7c2-119">Cuando es true, el dispositivo debe ser no compatible cuando no hay ninguna directiva de cumplimiento dirigida</span><span class="sxs-lookup"><span data-stu-id="2c7c2-119">Device should be noncompliant when there is no compliance policy targeted when this is true</span></span>|

## <a name="relationships"></a><span data-ttu-id="2c7c2-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2c7c2-120">Relationships</span></span>
<span data-ttu-id="2c7c2-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2c7c2-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2c7c2-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2c7c2-122">JSON Representation</span></span>
<span data-ttu-id="2c7c2-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-123">Here is a JSON representation of the resource.</span></span>
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



