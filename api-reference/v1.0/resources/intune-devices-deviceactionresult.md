---
title: Tipo de recurso deviceActionResult
description: Resultado de la acción de dispositivo
author: tfitzmac
ms.openlocfilehash: 48429e059616d9af0e3cbdac8544e68354b94fb5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320548"
---
# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="8d3e3-103">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="8d3e3-103">deviceActionResult resource type</span></span>

> <span data-ttu-id="8d3e3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d3e3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d3e3-105">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8d3e3-105">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="8d3e3-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d3e3-106">Properties</span></span>
|<span data-ttu-id="8d3e3-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d3e3-107">Property</span></span>|<span data-ttu-id="8d3e3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d3e3-108">Type</span></span>|<span data-ttu-id="8d3e3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d3e3-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d3e3-110">actionName</span><span class="sxs-lookup"><span data-stu-id="8d3e3-110">actionName</span></span>|<span data-ttu-id="8d3e3-111">cadena</span><span class="sxs-lookup"><span data-stu-id="8d3e3-111">String</span></span>|<span data-ttu-id="8d3e3-112">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="8d3e3-112">Action name</span></span>|
|<span data-ttu-id="8d3e3-113">actionState</span><span class="sxs-lookup"><span data-stu-id="8d3e3-113">actionState</span></span>|[<span data-ttu-id="8d3e3-114">actionState</span><span class="sxs-lookup"><span data-stu-id="8d3e3-114">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="8d3e3-115">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="8d3e3-115">State of the action.</span></span> <span data-ttu-id="8d3e3-116">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="8d3e3-116">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="8d3e3-117">startDateTime</span><span class="sxs-lookup"><span data-stu-id="8d3e3-117">startDateTime</span></span>|<span data-ttu-id="8d3e3-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d3e3-118">DateTimeOffset</span></span>|<span data-ttu-id="8d3e3-119">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="8d3e3-119">Time the action was initiated</span></span>|
|<span data-ttu-id="8d3e3-120">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="8d3e3-120">lastUpdatedDateTime</span></span>|<span data-ttu-id="8d3e3-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d3e3-121">DateTimeOffset</span></span>|<span data-ttu-id="8d3e3-122">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="8d3e3-122">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d3e3-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d3e3-123">Relationships</span></span>
<span data-ttu-id="8d3e3-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d3e3-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d3e3-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d3e3-125">JSON Representation</span></span>
<span data-ttu-id="8d3e3-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d3e3-126">Here is a JSON representation of the resource.</span></span>
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



