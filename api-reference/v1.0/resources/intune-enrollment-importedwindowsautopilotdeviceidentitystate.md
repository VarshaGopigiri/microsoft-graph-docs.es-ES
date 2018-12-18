---
title: Tipo de recurso importedWindowsAutopilotDeviceIdentityState resource type
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: ad1715098a50f61d83c529688b4a83f915741d1a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332777"
---
# <a name="importedwindowsautopilotdeviceidentitystate-resource-type"></a><span data-ttu-id="fc656-103">Tipo de recurso importedWindowsAutopilotDeviceIdentityState resource type</span><span class="sxs-lookup"><span data-stu-id="fc656-103">importedWindowsAutopilotDeviceIdentityState resource type</span></span>

> <span data-ttu-id="fc656-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fc656-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc656-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fc656-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="fc656-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc656-106">Properties</span></span>
|<span data-ttu-id="fc656-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc656-107">Property</span></span>|<span data-ttu-id="fc656-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc656-108">Type</span></span>|<span data-ttu-id="fc656-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc656-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fc656-110">deviceImportStatus</span><span class="sxs-lookup"><span data-stu-id="fc656-110">deviceImportStatus</span></span>|[<span data-ttu-id="fc656-111">importedWindowsAutopilotDeviceIdentityImportStatus</span><span class="sxs-lookup"><span data-stu-id="fc656-111">importedWindowsAutopilotDeviceIdentityImportStatus</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityimportstatus.md)|<span data-ttu-id="fc656-112">Estado del dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="fc656-112">Device status reported by Device Directory Service(DDS).</span></span> <span data-ttu-id="fc656-113">Los valores posibles son: `unknown`, `pending`, `partial`, `complete` y `error`.</span><span class="sxs-lookup"><span data-stu-id="fc656-113">Possible values are: `unknown`, `pending`, `partial`, `complete`, `error`.</span></span>|
|<span data-ttu-id="fc656-114">deviceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="fc656-114">deviceRegistrationId</span></span>|<span data-ttu-id="fc656-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="fc656-115">String</span></span>|<span data-ttu-id="fc656-116">Identificador del registro del dispositivo para el dispositivo agregado correctamente notificado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="fc656-116">Device Registration ID for successfully added device reported by Device Directory Service(DDS).</span></span>|
|<span data-ttu-id="fc656-117">deviceErrorCode</span><span class="sxs-lookup"><span data-stu-id="fc656-117">deviceErrorCode</span></span>|<span data-ttu-id="fc656-118">Int32</span><span class="sxs-lookup"><span data-stu-id="fc656-118">Int32</span></span>|<span data-ttu-id="fc656-119">Código de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="fc656-119">Device error code reported by Device Directory Service(DDS).</span></span>|
|<span data-ttu-id="fc656-120">deviceErrorName</span><span class="sxs-lookup"><span data-stu-id="fc656-120">deviceErrorName</span></span>|<span data-ttu-id="fc656-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="fc656-121">String</span></span>|<span data-ttu-id="fc656-122">Nombre de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="fc656-122">Device error name reported by Device Directory Service(DDS).</span></span>|

## <a name="relationships"></a><span data-ttu-id="fc656-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fc656-123">Relationships</span></span>
<span data-ttu-id="fc656-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fc656-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fc656-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fc656-125">JSON Representation</span></span>
<span data-ttu-id="fc656-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fc656-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
  "deviceImportStatus": "String",
  "deviceRegistrationId": "String",
  "deviceErrorCode": 1024,
  "deviceErrorName": "String"
}
```



