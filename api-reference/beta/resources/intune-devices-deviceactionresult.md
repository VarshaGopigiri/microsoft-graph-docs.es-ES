---
title: Tipo de recurso deviceActionResult
description: Resultado de la acción de dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 22fd8e1bc338191bba54ba9f655f03899054ae86
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912305"
---
# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="c5740-103">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="c5740-103">deviceActionResult resource type</span></span>

> <span data-ttu-id="c5740-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5740-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5740-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5740-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c5740-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c5740-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c5740-107">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c5740-107">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="c5740-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5740-108">Properties</span></span>
|<span data-ttu-id="c5740-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5740-109">Property</span></span>|<span data-ttu-id="c5740-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5740-110">Type</span></span>|<span data-ttu-id="c5740-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5740-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c5740-112">actionName</span><span class="sxs-lookup"><span data-stu-id="c5740-112">actionName</span></span>|<span data-ttu-id="c5740-113">cadena</span><span class="sxs-lookup"><span data-stu-id="c5740-113">String</span></span>|<span data-ttu-id="c5740-114">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="c5740-114">Action name</span></span>|
|<span data-ttu-id="c5740-115">actionState</span><span class="sxs-lookup"><span data-stu-id="c5740-115">actionState</span></span>|[<span data-ttu-id="c5740-116">actionState</span><span class="sxs-lookup"><span data-stu-id="c5740-116">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="c5740-117">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="c5740-117">State of the action.</span></span> <span data-ttu-id="c5740-118">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="c5740-118">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="c5740-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="c5740-119">startDateTime</span></span>|<span data-ttu-id="c5740-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c5740-120">DateTimeOffset</span></span>|<span data-ttu-id="c5740-121">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="c5740-121">Time the action was initiated</span></span>|
|<span data-ttu-id="c5740-122">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="c5740-122">lastUpdatedDateTime</span></span>|<span data-ttu-id="c5740-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c5740-123">DateTimeOffset</span></span>|<span data-ttu-id="c5740-124">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="c5740-124">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="c5740-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c5740-125">Relationships</span></span>
<span data-ttu-id="c5740-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c5740-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c5740-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c5740-127">JSON Representation</span></span>
<span data-ttu-id="c5740-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c5740-128">Here is a JSON representation of the resource.</span></span>
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





