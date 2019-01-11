---
title: Tipo de recurso importedWindowsAutopilotDeviceIdentityState resource type
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8017ac803ffa07a2e122553dee3268b0193157f0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869576"
---
# <a name="importedwindowsautopilotdeviceidentitystate-resource-type"></a><span data-ttu-id="27d50-103">Tipo de recurso importedWindowsAutopilotDeviceIdentityState resource type</span><span class="sxs-lookup"><span data-stu-id="27d50-103">importedWindowsAutopilotDeviceIdentityState resource type</span></span>

> <span data-ttu-id="27d50-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27d50-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27d50-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27d50-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="27d50-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="27d50-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="27d50-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="27d50-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="27d50-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27d50-108">Properties</span></span>
|<span data-ttu-id="27d50-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27d50-109">Property</span></span>|<span data-ttu-id="27d50-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="27d50-110">Type</span></span>|<span data-ttu-id="27d50-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="27d50-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="27d50-112">deviceImportStatus</span><span class="sxs-lookup"><span data-stu-id="27d50-112">deviceImportStatus</span></span>|[<span data-ttu-id="27d50-113">importedWindowsAutopilotDeviceIdentityImportStatus</span><span class="sxs-lookup"><span data-stu-id="27d50-113">importedWindowsAutopilotDeviceIdentityImportStatus</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityimportstatus.md)|<span data-ttu-id="27d50-114">Estado del dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="27d50-114">Device status reported by Device Directory Service(DDS).</span></span> <span data-ttu-id="27d50-115">Los valores posibles son: `unknown`, `pending`, `partial`, `complete` y `error`.</span><span class="sxs-lookup"><span data-stu-id="27d50-115">Possible values are: `unknown`, `pending`, `partial`, `complete`, `error`.</span></span>|
|<span data-ttu-id="27d50-116">deviceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="27d50-116">deviceRegistrationId</span></span>|<span data-ttu-id="27d50-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="27d50-117">String</span></span>|<span data-ttu-id="27d50-118">Identificador del registro del dispositivo para el dispositivo agregado correctamente notificado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="27d50-118">Device Registration ID for successfully added device reported by Device Directory Service(DDS).</span></span>|
|<span data-ttu-id="27d50-119">deviceErrorCode</span><span class="sxs-lookup"><span data-stu-id="27d50-119">deviceErrorCode</span></span>|<span data-ttu-id="27d50-120">Int32</span><span class="sxs-lookup"><span data-stu-id="27d50-120">Int32</span></span>|<span data-ttu-id="27d50-121">Código de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="27d50-121">Device error code reported by Device Directory Service(DDS).</span></span>|
|<span data-ttu-id="27d50-122">deviceErrorName</span><span class="sxs-lookup"><span data-stu-id="27d50-122">deviceErrorName</span></span>|<span data-ttu-id="27d50-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="27d50-123">String</span></span>|<span data-ttu-id="27d50-124">Nombre de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="27d50-124">Device error name reported by Device Directory Service(DDS).</span></span>|

## <a name="relationships"></a><span data-ttu-id="27d50-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="27d50-125">Relationships</span></span>
<span data-ttu-id="27d50-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="27d50-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="27d50-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27d50-127">JSON Representation</span></span>
<span data-ttu-id="27d50-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="27d50-128">Here is a JSON representation of the resource.</span></span>
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





