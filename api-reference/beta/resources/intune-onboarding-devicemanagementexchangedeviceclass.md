---
title: tipo de recurso deviceManagementExchangeDeviceClass
description: Clase de dispositivo en Exchange.
ms.openlocfilehash: 53234a97ffd2581eea1a4c480161ec9243a710d0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089898"
---
# <a name="devicemanagementexchangedeviceclass-resource-type"></a><span data-ttu-id="f686c-103">tipo de recurso deviceManagementExchangeDeviceClass</span><span class="sxs-lookup"><span data-stu-id="f686c-103">deviceManagementExchangeDeviceClass resource type</span></span>

> <span data-ttu-id="f686c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f686c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f686c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f686c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f686c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f686c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f686c-107">Clase de dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f686c-107">Device Class in Exchange.</span></span>
## <a name="properties"></a><span data-ttu-id="f686c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f686c-108">Properties</span></span>
|<span data-ttu-id="f686c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f686c-109">Property</span></span>|<span data-ttu-id="f686c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f686c-110">Type</span></span>|<span data-ttu-id="f686c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f686c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f686c-112">name</span><span class="sxs-lookup"><span data-stu-id="f686c-112">name</span></span>|<span data-ttu-id="f686c-113">String</span><span class="sxs-lookup"><span data-stu-id="f686c-113">String</span></span>|<span data-ttu-id="f686c-114">Nombre de la clase de dispositivo que se verán afectada por esta regla.</span><span class="sxs-lookup"><span data-stu-id="f686c-114">Name of the device class which will be impacted by this rule.</span></span>|
|<span data-ttu-id="f686c-115">type</span><span class="sxs-lookup"><span data-stu-id="f686c-115">type</span></span>|[<span data-ttu-id="f686c-116">deviceManagementExchangeAccessRuleType</span><span class="sxs-lookup"><span data-stu-id="f686c-116">deviceManagementExchangeAccessRuleType</span></span>](../resources/intune-onboarding-devicemanagementexchangeaccessruletype.md)|<span data-ttu-id="f686c-117">Tipo de dispositivo que se ve afectado por esta regla de familia, por ejemplo, el modelo.</span><span class="sxs-lookup"><span data-stu-id="f686c-117">Type of device which is impacted by this rule e.g. Model, Family.</span></span> <span data-ttu-id="f686c-118">Los valores posibles son: `family` y `model`.</span><span class="sxs-lookup"><span data-stu-id="f686c-118">Possible values are: `family`, `model`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f686c-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f686c-119">Relationships</span></span>
<span data-ttu-id="f686c-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f686c-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f686c-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f686c-121">JSON Representation</span></span>
<span data-ttu-id="f686c-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f686c-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeDeviceClass",
  "name": "String",
  "type": "String"
}
```





