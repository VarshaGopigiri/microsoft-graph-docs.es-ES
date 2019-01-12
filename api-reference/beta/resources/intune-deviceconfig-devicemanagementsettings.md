---
title: Tipo de recurso deviceManagementSettings
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4e92c8e88ecf620b4731bd3694dfb97e252d042f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973030"
---
# <a name="devicemanagementsettings-resource-type"></a><span data-ttu-id="be3f4-103">Tipo de recurso deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="be3f4-103">deviceManagementSettings resource type</span></span>

> <span data-ttu-id="be3f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="be3f4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="be3f4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="be3f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="be3f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="be3f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="be3f4-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="be3f4-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="be3f4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be3f4-108">Properties</span></span>
|<span data-ttu-id="be3f4-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be3f4-109">Property</span></span>|<span data-ttu-id="be3f4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="be3f4-110">Type</span></span>|<span data-ttu-id="be3f4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="be3f4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="be3f4-112">deviceComplianceCheckinThresholdDays</span><span class="sxs-lookup"><span data-stu-id="be3f4-112">deviceComplianceCheckinThresholdDays</span></span>|<span data-ttu-id="be3f4-113">Int32</span><span class="sxs-lookup"><span data-stu-id="be3f4-113">Int32</span></span>|<span data-ttu-id="be3f4-114">El número de días que se permite a un dispositivo continuar sin registrarse para seguir siendo compatible.</span><span class="sxs-lookup"><span data-stu-id="be3f4-114">The number of days a device is allowed to go without checking in to remain compliant.</span></span> <span data-ttu-id="be3f4-115">Valores válidos de 0 a 120</span><span class="sxs-lookup"><span data-stu-id="be3f4-115">Valid values 0 to 120</span></span>|
|<span data-ttu-id="be3f4-116">isScheduledActionEnabled</span><span class="sxs-lookup"><span data-stu-id="be3f4-116">isScheduledActionEnabled</span></span>|<span data-ttu-id="be3f4-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="be3f4-117">Boolean</span></span>|<span data-ttu-id="be3f4-118">Es la característica que está o no habilitada para la acción programada para la regla.</span><span class="sxs-lookup"><span data-stu-id="be3f4-118">Is feature enabled or not for scheduled action for rule.</span></span>|
|<span data-ttu-id="be3f4-119">secureByDefault</span><span class="sxs-lookup"><span data-stu-id="be3f4-119">secureByDefault</span></span>|<span data-ttu-id="be3f4-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="be3f4-120">Boolean</span></span>|<span data-ttu-id="be3f4-121">Cuando es true, el dispositivo debe ser no compatible cuando no hay ninguna directiva de cumplimiento dirigida</span><span class="sxs-lookup"><span data-stu-id="be3f4-121">Device should be noncompliant when there is no compliance policy targeted when this is true</span></span>|
|<span data-ttu-id="be3f4-122">enhancedJailBreak</span><span class="sxs-lookup"><span data-stu-id="be3f4-122">enhancedJailBreak</span></span>|<span data-ttu-id="be3f4-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="be3f4-123">Boolean</span></span>|<span data-ttu-id="be3f4-124">Es la característica habilitada o no para la detección de jailbreak de mejorada.</span><span class="sxs-lookup"><span data-stu-id="be3f4-124">Is feature enabled or not for enhanced jailbreak detection.</span></span>|
|<span data-ttu-id="be3f4-125">deviceInactivityBeforeRetirementInDay</span><span class="sxs-lookup"><span data-stu-id="be3f4-125">deviceInactivityBeforeRetirementInDay</span></span>|<span data-ttu-id="be3f4-126">Int32</span><span class="sxs-lookup"><span data-stu-id="be3f4-126">Int32</span></span>|<span data-ttu-id="be3f4-127">Cuando el dispositivo no busca un número especificado de días, es posible que se quiten los datos de la compañía y el dispositivo no estará en administración.</span><span class="sxs-lookup"><span data-stu-id="be3f4-127">When the device does not check in for specified number of days, the company data might be removed and the device will not be under management.</span></span> <span data-ttu-id="be3f4-128">Valores válidos 30 a 270</span><span class="sxs-lookup"><span data-stu-id="be3f4-128">Valid values 30 to 270</span></span>|

## <a name="relationships"></a><span data-ttu-id="be3f4-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="be3f4-129">Relationships</span></span>
<span data-ttu-id="be3f4-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="be3f4-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="be3f4-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="be3f4-131">JSON Representation</span></span>
<span data-ttu-id="be3f4-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="be3f4-132">Here is a JSON representation of the resource.</span></span>
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
  "secureByDefault": true,
  "enhancedJailBreak": true,
  "deviceInactivityBeforeRetirementInDay": 1024
}
```





