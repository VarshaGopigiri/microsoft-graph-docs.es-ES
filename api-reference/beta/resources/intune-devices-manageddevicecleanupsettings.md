---
title: tipo de recurso managedDeviceCleanupSettings
description: Definir la regla cuando el administrador desea que los dispositivos limpiar.
ms.openlocfilehash: f7782ac9d6571b58c8ed1e7964637736fcb5f3d4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087173"
---
# <a name="manageddevicecleanupsettings-resource-type"></a><span data-ttu-id="5c752-103">tipo de recurso managedDeviceCleanupSettings</span><span class="sxs-lookup"><span data-stu-id="5c752-103">managedDeviceCleanupSettings resource type</span></span>

> <span data-ttu-id="5c752-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5c752-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5c752-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5c752-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5c752-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c752-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c752-107">Definir la regla cuando el administrador desea que los dispositivos limpiar.</span><span class="sxs-lookup"><span data-stu-id="5c752-107">Define the rule when the admin wants the devices to be cleaned up.</span></span>
## <a name="properties"></a><span data-ttu-id="5c752-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c752-108">Properties</span></span>
|<span data-ttu-id="5c752-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c752-109">Property</span></span>|<span data-ttu-id="5c752-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c752-110">Type</span></span>|<span data-ttu-id="5c752-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c752-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c752-112">deviceInactivityBeforeRetirementInDays</span><span class="sxs-lookup"><span data-stu-id="5c752-112">deviceInactivityBeforeRetirementInDays</span></span>|<span data-ttu-id="5c752-113">String</span><span class="sxs-lookup"><span data-stu-id="5c752-113">String</span></span>|<span data-ttu-id="5c752-114">Número de días cuando el dispositivo no ha contactado Intune.</span><span class="sxs-lookup"><span data-stu-id="5c752-114">Number of days when the device has not contacted Intune.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5c752-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5c752-115">Relationships</span></span>
<span data-ttu-id="5c752-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5c752-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5c752-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5c752-117">JSON Representation</span></span>
<span data-ttu-id="5c752-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5c752-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedDeviceCleanupSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceCleanupSettings",
  "deviceInactivityBeforeRetirementInDays": "String"
}
```




