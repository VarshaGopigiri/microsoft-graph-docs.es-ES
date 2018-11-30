---
title: tipo de recurso deviceManagementScriptRunSummary
description: Contiene las propiedades para el resumen de la ejecución de una secuencia de comandos de administración de dispositivos.
ms.openlocfilehash: 9269ae5f3f6fc889cb02ad90e2897c9a3e979241
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088947"
---
# <a name="devicemanagementscriptrunsummary-resource-type"></a><span data-ttu-id="dbfc7-103">tipo de recurso deviceManagementScriptRunSummary</span><span class="sxs-lookup"><span data-stu-id="dbfc7-103">deviceManagementScriptRunSummary resource type</span></span>

> <span data-ttu-id="dbfc7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dbfc7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dbfc7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dbfc7-107">Contiene las propiedades para el resumen de la ejecución de una secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-107">Contains properties for the run summary of a device management script.</span></span>
## <a name="methods"></a><span data-ttu-id="dbfc7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbfc7-108">Methods</span></span>
|<span data-ttu-id="dbfc7-109">Método</span><span class="sxs-lookup"><span data-stu-id="dbfc7-109">Method</span></span>|<span data-ttu-id="dbfc7-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbfc7-110">Return Type</span></span>|<span data-ttu-id="dbfc7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbfc7-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="dbfc7-112">Obtener deviceManagementScriptRunSummary</span><span class="sxs-lookup"><span data-stu-id="dbfc7-112">Get deviceManagementScriptRunSummary</span></span>](../api/intune-devices-devicemanagementscriptrunsummary-get.md)|[<span data-ttu-id="dbfc7-113">deviceManagementScriptRunSummary</span><span class="sxs-lookup"><span data-stu-id="dbfc7-113">deviceManagementScriptRunSummary</span></span>](../resources/intune-devices-devicemanagementscriptrunsummary.md)|<span data-ttu-id="dbfc7-114">Leer las propiedades y las relaciones del objeto [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="dbfc7-114">Read properties and relationships of the [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) object.</span></span>|
|[<span data-ttu-id="dbfc7-115">Actualizar deviceManagementScriptRunSummary</span><span class="sxs-lookup"><span data-stu-id="dbfc7-115">Update deviceManagementScriptRunSummary</span></span>](../api/intune-devices-devicemanagementscriptrunsummary-update.md)|[<span data-ttu-id="dbfc7-116">deviceManagementScriptRunSummary</span><span class="sxs-lookup"><span data-stu-id="dbfc7-116">deviceManagementScriptRunSummary</span></span>](../resources/intune-devices-devicemanagementscriptrunsummary.md)|<span data-ttu-id="dbfc7-117">Actualizar las propiedades de un objeto [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="dbfc7-117">Update the properties of a [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="dbfc7-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbfc7-118">Properties</span></span>
|<span data-ttu-id="dbfc7-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbfc7-119">Property</span></span>|<span data-ttu-id="dbfc7-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbfc7-120">Type</span></span>|<span data-ttu-id="dbfc7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbfc7-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dbfc7-122">id</span><span class="sxs-lookup"><span data-stu-id="dbfc7-122">id</span></span>|<span data-ttu-id="dbfc7-123">String</span><span class="sxs-lookup"><span data-stu-id="dbfc7-123">String</span></span>|<span data-ttu-id="dbfc7-124">Clave de la secuencia de comandos de administración de dispositivo ejecute entidad resumen.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-124">Key of the device management script run summary entity.</span></span>|
|<span data-ttu-id="dbfc7-125">successDeviceCount</span><span class="sxs-lookup"><span data-stu-id="dbfc7-125">successDeviceCount</span></span>|<span data-ttu-id="dbfc7-126">Int32</span><span class="sxs-lookup"><span data-stu-id="dbfc7-126">Int32</span></span>|<span data-ttu-id="dbfc7-127">Recuento de éxito de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-127">Success device count.</span></span>|
|<span data-ttu-id="dbfc7-128">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="dbfc7-128">errorDeviceCount</span></span>|<span data-ttu-id="dbfc7-129">Int32</span><span class="sxs-lookup"><span data-stu-id="dbfc7-129">Int32</span></span>|<span data-ttu-id="dbfc7-130">Recuento de error de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-130">Error device count.</span></span>|
|<span data-ttu-id="dbfc7-131">successUserCount</span><span class="sxs-lookup"><span data-stu-id="dbfc7-131">successUserCount</span></span>|<span data-ttu-id="dbfc7-132">Int32</span><span class="sxs-lookup"><span data-stu-id="dbfc7-132">Int32</span></span>|<span data-ttu-id="dbfc7-133">Recuento de usuario correcto.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-133">Success user count.</span></span>|
|<span data-ttu-id="dbfc7-134">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="dbfc7-134">errorUserCount</span></span>|<span data-ttu-id="dbfc7-135">Int32</span><span class="sxs-lookup"><span data-stu-id="dbfc7-135">Int32</span></span>|<span data-ttu-id="dbfc7-136">Recuento de usuario de error.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-136">Error user count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="dbfc7-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dbfc7-137">Relationships</span></span>
<span data-ttu-id="dbfc7-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="dbfc7-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="dbfc7-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dbfc7-139">JSON Representation</span></span>
<span data-ttu-id="dbfc7-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dbfc7-140">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptRunSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptRunSummary",
  "id": "String (identifier)",
  "successDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "successUserCount": 1024,
  "errorUserCount": 1024
}
```





