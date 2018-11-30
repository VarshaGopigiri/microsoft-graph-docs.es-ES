---
title: Tipo de recurso resetPasscodeActionResult
description: Resultado de la acción Restablecer código de acceso
ms.openlocfilehash: d4a2128becef011c7a03dd6325d562c1290c2e33
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085486"
---
# <a name="resetpasscodeactionresult-resource-type"></a><span data-ttu-id="1be96-103">Tipo de recurso resetPasscodeActionResult</span><span class="sxs-lookup"><span data-stu-id="1be96-103">resetPasscodeActionResult resource type</span></span>

> <span data-ttu-id="1be96-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1be96-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1be96-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1be96-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1be96-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1be96-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1be96-107">Resultado de la acción Restablecer código de acceso</span><span class="sxs-lookup"><span data-stu-id="1be96-107">Reset passcode action result</span></span>

<span data-ttu-id="1be96-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="1be96-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="1be96-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1be96-109">Properties</span></span>
|<span data-ttu-id="1be96-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1be96-110">Property</span></span>|<span data-ttu-id="1be96-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1be96-111">Type</span></span>|<span data-ttu-id="1be96-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1be96-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1be96-113">actionName</span><span class="sxs-lookup"><span data-stu-id="1be96-113">actionName</span></span>|<span data-ttu-id="1be96-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="1be96-114">String</span></span>|<span data-ttu-id="1be96-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="1be96-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="1be96-116">actionState</span><span class="sxs-lookup"><span data-stu-id="1be96-116">actionState</span></span>|[<span data-ttu-id="1be96-117">actionState</span><span class="sxs-lookup"><span data-stu-id="1be96-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="1be96-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="1be96-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="1be96-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="1be96-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="1be96-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="1be96-120">startDateTime</span></span>|<span data-ttu-id="1be96-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1be96-121">DateTimeOffset</span></span>|<span data-ttu-id="1be96-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="1be96-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="1be96-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="1be96-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="1be96-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1be96-124">DateTimeOffset</span></span>|<span data-ttu-id="1be96-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="1be96-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="1be96-126">código de acceso</span><span class="sxs-lookup"><span data-stu-id="1be96-126">passcode</span></span>|<span data-ttu-id="1be96-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="1be96-127">String</span></span>|<span data-ttu-id="1be96-128">Código de acceso recién generado para el dispositivo</span><span class="sxs-lookup"><span data-stu-id="1be96-128">Newly generated passcode for the device</span></span> |

## <a name="relationships"></a><span data-ttu-id="1be96-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1be96-129">Relationships</span></span>
<span data-ttu-id="1be96-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1be96-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1be96-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1be96-131">JSON Representation</span></span>
<span data-ttu-id="1be96-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1be96-132">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.resetPasscodeActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.resetPasscodeActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "passcode": "String"
}
```





