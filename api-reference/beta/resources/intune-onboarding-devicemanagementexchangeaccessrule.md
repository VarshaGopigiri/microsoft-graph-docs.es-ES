---
title: tipo de recurso deviceManagementExchangeAccessRule
description: Reglas de acceso de dispositivo en Exchange.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5d7f0e649d2c5f2f27a4623fa0f65cf43965f576
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855191"
---
# <a name="devicemanagementexchangeaccessrule-resource-type"></a><span data-ttu-id="80548-103">tipo de recurso deviceManagementExchangeAccessRule</span><span class="sxs-lookup"><span data-stu-id="80548-103">deviceManagementExchangeAccessRule resource type</span></span>

> <span data-ttu-id="80548-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="80548-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="80548-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="80548-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="80548-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80548-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80548-107">Reglas de acceso de dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="80548-107">Device Access Rules in Exchange.</span></span>
## <a name="properties"></a><span data-ttu-id="80548-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80548-108">Properties</span></span>
|<span data-ttu-id="80548-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80548-109">Property</span></span>|<span data-ttu-id="80548-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="80548-110">Type</span></span>|<span data-ttu-id="80548-111">Description</span><span class="sxs-lookup"><span data-stu-id="80548-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80548-112">deviceClass</span><span class="sxs-lookup"><span data-stu-id="80548-112">deviceClass</span></span>|[<span data-ttu-id="80548-113">deviceManagementExchangeDeviceClass</span><span class="sxs-lookup"><span data-stu-id="80548-113">deviceManagementExchangeDeviceClass</span></span>](../resources/intune-onboarding-devicemanagementexchangedeviceclass.md)|<span data-ttu-id="80548-114">Clase de dispositivo que se verán afectada por esta regla.</span><span class="sxs-lookup"><span data-stu-id="80548-114">Device Class which will be impacted by this rule.</span></span>|
|<span data-ttu-id="80548-115">accessLevel</span><span class="sxs-lookup"><span data-stu-id="80548-115">accessLevel</span></span>|[<span data-ttu-id="80548-116">deviceManagementExchangeAccessLevel</span><span class="sxs-lookup"><span data-stu-id="80548-116">deviceManagementExchangeAccessLevel</span></span>](../resources/intune-onboarding-devicemanagementexchangeaccesslevel.md)|<span data-ttu-id="80548-117">Nivel de acceso para Exchange concedido por esta regla.</span><span class="sxs-lookup"><span data-stu-id="80548-117">Access Level for Exchange granted by this rule.</span></span> <span data-ttu-id="80548-118">Los valores posibles son: `none`, `allow`, `block` y `quarantine`.</span><span class="sxs-lookup"><span data-stu-id="80548-118">Possible values are: `none`, `allow`, `block`, `quarantine`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="80548-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="80548-119">Relationships</span></span>
<span data-ttu-id="80548-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="80548-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="80548-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="80548-121">JSON Representation</span></span>
<span data-ttu-id="80548-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="80548-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementExchangeAccessRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeAccessRule",
  "deviceClass": {
    "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass",
    "name": "String",
    "type": "String"
  },
  "accessLevel": "String"
}
```





