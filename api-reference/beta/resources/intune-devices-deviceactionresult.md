---
title: Tipo de recurso deviceActionResult
description: Resultado de la acción de dispositivo
ms.openlocfilehash: ac37cdff8ec323dfb8a2019b383d506c1b7e1076
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084409"
---
# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="811d1-103">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="811d1-103">deviceActionResult resource type</span></span>

> <span data-ttu-id="811d1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="811d1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="811d1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="811d1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="811d1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="811d1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="811d1-107">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="811d1-107">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="811d1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="811d1-108">Properties</span></span>
|<span data-ttu-id="811d1-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="811d1-109">Property</span></span>|<span data-ttu-id="811d1-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="811d1-110">Type</span></span>|<span data-ttu-id="811d1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="811d1-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="811d1-112">actionName</span><span class="sxs-lookup"><span data-stu-id="811d1-112">actionName</span></span>|<span data-ttu-id="811d1-113">cadena</span><span class="sxs-lookup"><span data-stu-id="811d1-113">String</span></span>|<span data-ttu-id="811d1-114">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="811d1-114">Action name</span></span>|
|<span data-ttu-id="811d1-115">actionState</span><span class="sxs-lookup"><span data-stu-id="811d1-115">actionState</span></span>|[<span data-ttu-id="811d1-116">actionState</span><span class="sxs-lookup"><span data-stu-id="811d1-116">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="811d1-117">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="811d1-117">State of the action.</span></span> <span data-ttu-id="811d1-118">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="811d1-118">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="811d1-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="811d1-119">startDateTime</span></span>|<span data-ttu-id="811d1-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="811d1-120">DateTimeOffset</span></span>|<span data-ttu-id="811d1-121">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="811d1-121">Time the action was initiated</span></span>|
|<span data-ttu-id="811d1-122">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="811d1-122">lastUpdatedDateTime</span></span>|<span data-ttu-id="811d1-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="811d1-123">DateTimeOffset</span></span>|<span data-ttu-id="811d1-124">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="811d1-124">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="811d1-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="811d1-125">Relationships</span></span>
<span data-ttu-id="811d1-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="811d1-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="811d1-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="811d1-127">JSON Representation</span></span>
<span data-ttu-id="811d1-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="811d1-128">Here is a JSON representation of the resource.</span></span>
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





