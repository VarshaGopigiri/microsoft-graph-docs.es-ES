---
title: tipo de recurso windowsManagementAppHealthSummary
description: Contiene las propiedades para el resumen de estado de la aplicación de administración de Windows.
ms.openlocfilehash: dddcb40a0a66446ab6e87a2e684c1dbf0df547fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086780"
---
# <a name="windowsmanagementapphealthsummary-resource-type"></a><span data-ttu-id="35cb9-103">tipo de recurso windowsManagementAppHealthSummary</span><span class="sxs-lookup"><span data-stu-id="35cb9-103">windowsManagementAppHealthSummary resource type</span></span>

> <span data-ttu-id="35cb9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35cb9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35cb9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35cb9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="35cb9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35cb9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35cb9-107">Contiene las propiedades para el resumen de estado de la aplicación de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="35cb9-107">Contains properties for the health summary of the Windows management app.</span></span>
## <a name="methods"></a><span data-ttu-id="35cb9-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="35cb9-108">Methods</span></span>
|<span data-ttu-id="35cb9-109">Método</span><span class="sxs-lookup"><span data-stu-id="35cb9-109">Method</span></span>|<span data-ttu-id="35cb9-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35cb9-110">Return Type</span></span>|<span data-ttu-id="35cb9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="35cb9-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="35cb9-112">Obtener windowsManagementAppHealthSummary</span><span class="sxs-lookup"><span data-stu-id="35cb9-112">Get windowsManagementAppHealthSummary</span></span>](../api/intune-devices-windowsmanagementapphealthsummary-get.md)|[<span data-ttu-id="35cb9-113">windowsManagementAppHealthSummary</span><span class="sxs-lookup"><span data-stu-id="35cb9-113">windowsManagementAppHealthSummary</span></span>](../resources/intune-devices-windowsmanagementapphealthsummary.md)|<span data-ttu-id="35cb9-114">Leer las propiedades y las relaciones del objeto [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="35cb9-114">Read properties and relationships of the [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) object.</span></span>|
|[<span data-ttu-id="35cb9-115">Actualizar windowsManagementAppHealthSummary</span><span class="sxs-lookup"><span data-stu-id="35cb9-115">Update windowsManagementAppHealthSummary</span></span>](../api/intune-devices-windowsmanagementapphealthsummary-update.md)|[<span data-ttu-id="35cb9-116">windowsManagementAppHealthSummary</span><span class="sxs-lookup"><span data-stu-id="35cb9-116">windowsManagementAppHealthSummary</span></span>](../resources/intune-devices-windowsmanagementapphealthsummary.md)|<span data-ttu-id="35cb9-117">Actualizar las propiedades de un objeto [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="35cb9-117">Update the properties of a [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="35cb9-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35cb9-118">Properties</span></span>
|<span data-ttu-id="35cb9-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="35cb9-119">Property</span></span>|<span data-ttu-id="35cb9-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="35cb9-120">Type</span></span>|<span data-ttu-id="35cb9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="35cb9-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="35cb9-122">id</span><span class="sxs-lookup"><span data-stu-id="35cb9-122">id</span></span>|<span data-ttu-id="35cb9-123">String</span><span class="sxs-lookup"><span data-stu-id="35cb9-123">String</span></span>|<span data-ttu-id="35cb9-124">Clave de la entidad resumen del estado de aplicación de Windows management.</span><span class="sxs-lookup"><span data-stu-id="35cb9-124">Key of the Windows management app health summary entity.</span></span>|
|<span data-ttu-id="35cb9-125">healthyDeviceCount</span><span class="sxs-lookup"><span data-stu-id="35cb9-125">healthyDeviceCount</span></span>|<span data-ttu-id="35cb9-126">Int32</span><span class="sxs-lookup"><span data-stu-id="35cb9-126">Int32</span></span>|<span data-ttu-id="35cb9-127">Recuento de dispositivo correcto.</span><span class="sxs-lookup"><span data-stu-id="35cb9-127">Healthy device count.</span></span>|
|<span data-ttu-id="35cb9-128">unhealthyDeviceCount</span><span class="sxs-lookup"><span data-stu-id="35cb9-128">unhealthyDeviceCount</span></span>|<span data-ttu-id="35cb9-129">Int32</span><span class="sxs-lookup"><span data-stu-id="35cb9-129">Int32</span></span>|<span data-ttu-id="35cb9-130">Recuento de dispositivo mal estado.</span><span class="sxs-lookup"><span data-stu-id="35cb9-130">Unhealthy device count.</span></span>|
|<span data-ttu-id="35cb9-131">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="35cb9-131">unknownDeviceCount</span></span>|<span data-ttu-id="35cb9-132">Int32</span><span class="sxs-lookup"><span data-stu-id="35cb9-132">Int32</span></span>|<span data-ttu-id="35cb9-133">Recuento de dispositivo desconocido.</span><span class="sxs-lookup"><span data-stu-id="35cb9-133">Unknown device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="35cb9-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="35cb9-134">Relationships</span></span>
<span data-ttu-id="35cb9-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="35cb9-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="35cb9-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="35cb9-136">JSON Representation</span></span>
<span data-ttu-id="35cb9-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="35cb9-137">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsManagementAppHealthSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsManagementAppHealthSummary",
  "id": "String (identifier)",
  "healthyDeviceCount": 1024,
  "unhealthyDeviceCount": 1024,
  "unknownDeviceCount": 1024
}
```




