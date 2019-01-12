---
title: Tipo de recurso deviceActionResult
description: Resultado de la acción de dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: be8519adc44f7bb63379b0bfa821a067f3eee947
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985892"
---
# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="8cdcd-103">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="8cdcd-103">deviceActionResult resource type</span></span>

> <span data-ttu-id="8cdcd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8cdcd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8cdcd-105">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8cdcd-105">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="8cdcd-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8cdcd-106">Properties</span></span>
|<span data-ttu-id="8cdcd-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8cdcd-107">Property</span></span>|<span data-ttu-id="8cdcd-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8cdcd-108">Type</span></span>|<span data-ttu-id="8cdcd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cdcd-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8cdcd-110">actionName</span><span class="sxs-lookup"><span data-stu-id="8cdcd-110">actionName</span></span>|<span data-ttu-id="8cdcd-111">cadena</span><span class="sxs-lookup"><span data-stu-id="8cdcd-111">String</span></span>|<span data-ttu-id="8cdcd-112">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="8cdcd-112">Action name</span></span>|
|<span data-ttu-id="8cdcd-113">actionState</span><span class="sxs-lookup"><span data-stu-id="8cdcd-113">actionState</span></span>|[<span data-ttu-id="8cdcd-114">actionState</span><span class="sxs-lookup"><span data-stu-id="8cdcd-114">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="8cdcd-115">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="8cdcd-115">State of the action.</span></span> <span data-ttu-id="8cdcd-116">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="8cdcd-116">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="8cdcd-117">startDateTime</span><span class="sxs-lookup"><span data-stu-id="8cdcd-117">startDateTime</span></span>|<span data-ttu-id="8cdcd-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8cdcd-118">DateTimeOffset</span></span>|<span data-ttu-id="8cdcd-119">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="8cdcd-119">Time the action was initiated</span></span>|
|<span data-ttu-id="8cdcd-120">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="8cdcd-120">lastUpdatedDateTime</span></span>|<span data-ttu-id="8cdcd-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8cdcd-121">DateTimeOffset</span></span>|<span data-ttu-id="8cdcd-122">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="8cdcd-122">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="8cdcd-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8cdcd-123">Relationships</span></span>
<span data-ttu-id="8cdcd-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8cdcd-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8cdcd-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8cdcd-125">JSON Representation</span></span>
<span data-ttu-id="8cdcd-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8cdcd-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```



