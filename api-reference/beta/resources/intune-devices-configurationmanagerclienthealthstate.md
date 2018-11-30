---
title: tipo de recurso configurationManagerClientHealthState
description: Estado de mantenimiento de cliente de administrador de configuración
ms.openlocfilehash: f2724f5d230ee539720e105daf1758bf727bee26
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084520"
---
# <a name="configurationmanagerclienthealthstate-resource-type"></a><span data-ttu-id="75097-103">tipo de recurso configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="75097-103">configurationManagerClientHealthState resource type</span></span>

> <span data-ttu-id="75097-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75097-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75097-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75097-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="75097-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75097-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75097-107">Estado de mantenimiento de cliente de administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="75097-107">Configuration manager client health state</span></span>
## <a name="properties"></a><span data-ttu-id="75097-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75097-108">Properties</span></span>
|<span data-ttu-id="75097-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75097-109">Property</span></span>|<span data-ttu-id="75097-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="75097-110">Type</span></span>|<span data-ttu-id="75097-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="75097-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75097-112">state</span><span class="sxs-lookup"><span data-stu-id="75097-112">state</span></span>|[<span data-ttu-id="75097-113">configurationManagerClientState</span><span class="sxs-lookup"><span data-stu-id="75097-113">configurationManagerClientState</span></span>](../resources/intune-devices-configurationmanagerclientstate.md)|<span data-ttu-id="75097-114">Estado de cliente de administrador de configuración actual.</span><span class="sxs-lookup"><span data-stu-id="75097-114">Current configuration manager client state.</span></span> <span data-ttu-id="75097-115">Los valores posibles son: `unknown`, `installed`, `healthy`, `installFailed`, `updateFailed` y `communicationError`.</span><span class="sxs-lookup"><span data-stu-id="75097-115">Possible values are: `unknown`, `installed`, `healthy`, `installFailed`, `updateFailed`, `communicationError`.</span></span>|
|<span data-ttu-id="75097-116">errorCode</span><span class="sxs-lookup"><span data-stu-id="75097-116">errorCode</span></span>|<span data-ttu-id="75097-117">Int32</span><span class="sxs-lookup"><span data-stu-id="75097-117">Int32</span></span>|<span data-ttu-id="75097-118">Código de error de estado de error.</span><span class="sxs-lookup"><span data-stu-id="75097-118">Error code for failed state.</span></span>|
|<span data-ttu-id="75097-119">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="75097-119">lastSyncDateTime</span></span>|<span data-ttu-id="75097-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="75097-120">DateTimeOffset</span></span>|<span data-ttu-id="75097-121">Elija la última sincronización de fo de fecha y hora con la administración del Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="75097-121">Datetime fo last sync with configuration manager management point.</span></span>|

## <a name="relationships"></a><span data-ttu-id="75097-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="75097-122">Relationships</span></span>
<span data-ttu-id="75097-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="75097-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="75097-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75097-124">JSON Representation</span></span>
<span data-ttu-id="75097-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75097-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.configurationManagerClientHealthState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.configurationManagerClientHealthState",
  "state": "String",
  "errorCode": 1024,
  "lastSyncDateTime": "String (timestamp)"
}
```





