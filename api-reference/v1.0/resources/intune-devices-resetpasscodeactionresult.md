---
title: Tipo de recurso resetPasscodeActionResult
description: Resultado de la acción Restablecer código de acceso
ms.openlocfilehash: 6b951a75b93b4e625fb61110ba909632c051b0f5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030052"
---
# <a name="resetpasscodeactionresult-resource-type"></a><span data-ttu-id="959a4-103">Tipo de recurso resetPasscodeActionResult</span><span class="sxs-lookup"><span data-stu-id="959a4-103">resetPasscodeActionResult resource type</span></span>

> <span data-ttu-id="959a4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="959a4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="959a4-105">Resultado de la acción Restablecer código de acceso</span><span class="sxs-lookup"><span data-stu-id="959a4-105">Reset passcode action result</span></span>

<span data-ttu-id="959a4-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="959a4-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="959a4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="959a4-107">Properties</span></span>
|<span data-ttu-id="959a4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="959a4-108">Property</span></span>|<span data-ttu-id="959a4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="959a4-109">Type</span></span>|<span data-ttu-id="959a4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="959a4-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="959a4-111">actionName</span><span class="sxs-lookup"><span data-stu-id="959a4-111">actionName</span></span>|<span data-ttu-id="959a4-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="959a4-112">String</span></span>|<span data-ttu-id="959a4-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="959a4-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="959a4-114">actionState</span><span class="sxs-lookup"><span data-stu-id="959a4-114">actionState</span></span>|[<span data-ttu-id="959a4-115">actionState</span><span class="sxs-lookup"><span data-stu-id="959a4-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="959a4-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="959a4-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="959a4-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="959a4-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="959a4-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="959a4-118">startDateTime</span></span>|<span data-ttu-id="959a4-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="959a4-119">DateTimeOffset</span></span>|<span data-ttu-id="959a4-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="959a4-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="959a4-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="959a4-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="959a4-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="959a4-122">DateTimeOffset</span></span>|<span data-ttu-id="959a4-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="959a4-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="959a4-124">código de acceso</span><span class="sxs-lookup"><span data-stu-id="959a4-124">passcode</span></span>|<span data-ttu-id="959a4-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="959a4-125">String</span></span>|<span data-ttu-id="959a4-126">Código de acceso recién generado para el dispositivo</span><span class="sxs-lookup"><span data-stu-id="959a4-126">Newly generated passcode for the device</span></span> |

## <a name="relationships"></a><span data-ttu-id="959a4-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="959a4-127">Relationships</span></span>
<span data-ttu-id="959a4-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="959a4-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="959a4-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="959a4-129">JSON Representation</span></span>
<span data-ttu-id="959a4-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="959a4-130">Here is a JSON representation of the resource.</span></span>
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



