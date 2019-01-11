---
title: Tipo de recurso deviceActionResult
description: Resultado de la acción de dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1b802d1b09fbe65e9e1e72e4c34a387462e12113
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861127"
---
# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="f219e-103">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="f219e-103">deviceActionResult resource type</span></span>

> <span data-ttu-id="f219e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f219e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f219e-105">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f219e-105">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="f219e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f219e-106">Properties</span></span>
|<span data-ttu-id="f219e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f219e-107">Property</span></span>|<span data-ttu-id="f219e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f219e-108">Type</span></span>|<span data-ttu-id="f219e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f219e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f219e-110">actionName</span><span class="sxs-lookup"><span data-stu-id="f219e-110">actionName</span></span>|<span data-ttu-id="f219e-111">cadena</span><span class="sxs-lookup"><span data-stu-id="f219e-111">String</span></span>|<span data-ttu-id="f219e-112">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="f219e-112">Action name</span></span>|
|<span data-ttu-id="f219e-113">actionState</span><span class="sxs-lookup"><span data-stu-id="f219e-113">actionState</span></span>|[<span data-ttu-id="f219e-114">actionState</span><span class="sxs-lookup"><span data-stu-id="f219e-114">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="f219e-115">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="f219e-115">State of the action.</span></span> <span data-ttu-id="f219e-116">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="f219e-116">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="f219e-117">startDateTime</span><span class="sxs-lookup"><span data-stu-id="f219e-117">startDateTime</span></span>|<span data-ttu-id="f219e-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f219e-118">DateTimeOffset</span></span>|<span data-ttu-id="f219e-119">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="f219e-119">Time the action was initiated</span></span>|
|<span data-ttu-id="f219e-120">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="f219e-120">lastUpdatedDateTime</span></span>|<span data-ttu-id="f219e-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f219e-121">DateTimeOffset</span></span>|<span data-ttu-id="f219e-122">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="f219e-122">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="f219e-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f219e-123">Relationships</span></span>
<span data-ttu-id="f219e-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f219e-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f219e-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f219e-125">JSON Representation</span></span>
<span data-ttu-id="f219e-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f219e-126">Here is a JSON representation of the resource.</span></span>
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



