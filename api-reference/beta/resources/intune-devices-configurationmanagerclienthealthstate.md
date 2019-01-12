---
title: tipo de recurso configurationManagerClientHealthState
description: Estado de mantenimiento de cliente de administrador de configuración
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4d202b5f672977e8bb1a5fe05ba56937005825ff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981745"
---
# <a name="configurationmanagerclienthealthstate-resource-type"></a><span data-ttu-id="9439b-103">tipo de recurso configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="9439b-103">configurationManagerClientHealthState resource type</span></span>

> <span data-ttu-id="9439b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9439b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9439b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9439b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9439b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9439b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9439b-107">Estado de mantenimiento de cliente de administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="9439b-107">Configuration manager client health state</span></span>
## <a name="properties"></a><span data-ttu-id="9439b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9439b-108">Properties</span></span>
|<span data-ttu-id="9439b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9439b-109">Property</span></span>|<span data-ttu-id="9439b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9439b-110">Type</span></span>|<span data-ttu-id="9439b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9439b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9439b-112">state</span><span class="sxs-lookup"><span data-stu-id="9439b-112">state</span></span>|[<span data-ttu-id="9439b-113">configurationManagerClientState</span><span class="sxs-lookup"><span data-stu-id="9439b-113">configurationManagerClientState</span></span>](../resources/intune-devices-configurationmanagerclientstate.md)|<span data-ttu-id="9439b-114">Estado de cliente de administrador de configuración actual.</span><span class="sxs-lookup"><span data-stu-id="9439b-114">Current configuration manager client state.</span></span> <span data-ttu-id="9439b-115">Los valores posibles son: `unknown`, `installed`, `healthy`, `installFailed`, `updateFailed` y `communicationError`.</span><span class="sxs-lookup"><span data-stu-id="9439b-115">Possible values are: `unknown`, `installed`, `healthy`, `installFailed`, `updateFailed`, `communicationError`.</span></span>|
|<span data-ttu-id="9439b-116">errorCode</span><span class="sxs-lookup"><span data-stu-id="9439b-116">errorCode</span></span>|<span data-ttu-id="9439b-117">Int32</span><span class="sxs-lookup"><span data-stu-id="9439b-117">Int32</span></span>|<span data-ttu-id="9439b-118">Código de error de estado de error.</span><span class="sxs-lookup"><span data-stu-id="9439b-118">Error code for failed state.</span></span>|
|<span data-ttu-id="9439b-119">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="9439b-119">lastSyncDateTime</span></span>|<span data-ttu-id="9439b-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9439b-120">DateTimeOffset</span></span>|<span data-ttu-id="9439b-121">Elija la última sincronización de fo de fecha y hora con la administración del Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="9439b-121">Datetime fo last sync with configuration manager management point.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9439b-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9439b-122">Relationships</span></span>
<span data-ttu-id="9439b-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9439b-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9439b-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9439b-124">JSON Representation</span></span>
<span data-ttu-id="9439b-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9439b-125">Here is a JSON representation of the resource.</span></span>
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





