---
title: Tipo de recurso deviceActionResult
description: Resultado de la acción de dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 051d5f381e27e4901f7e2fb9280cea3dc0bb71c4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806107"
---
# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="66302-103">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="66302-103">deviceActionResult resource type</span></span>

> <span data-ttu-id="66302-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66302-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66302-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66302-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="66302-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66302-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66302-107">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="66302-107">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="66302-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66302-108">Properties</span></span>
|<span data-ttu-id="66302-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66302-109">Property</span></span>|<span data-ttu-id="66302-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="66302-110">Type</span></span>|<span data-ttu-id="66302-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="66302-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66302-112">actionName</span><span class="sxs-lookup"><span data-stu-id="66302-112">actionName</span></span>|<span data-ttu-id="66302-113">cadena</span><span class="sxs-lookup"><span data-stu-id="66302-113">String</span></span>|<span data-ttu-id="66302-114">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="66302-114">Action name</span></span>|
|<span data-ttu-id="66302-115">actionState</span><span class="sxs-lookup"><span data-stu-id="66302-115">actionState</span></span>|[<span data-ttu-id="66302-116">actionState</span><span class="sxs-lookup"><span data-stu-id="66302-116">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="66302-117">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="66302-117">State of the action.</span></span> <span data-ttu-id="66302-118">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="66302-118">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="66302-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="66302-119">startDateTime</span></span>|<span data-ttu-id="66302-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66302-120">DateTimeOffset</span></span>|<span data-ttu-id="66302-121">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="66302-121">Time the action was initiated</span></span>|
|<span data-ttu-id="66302-122">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="66302-122">lastUpdatedDateTime</span></span>|<span data-ttu-id="66302-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66302-123">DateTimeOffset</span></span>|<span data-ttu-id="66302-124">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="66302-124">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="66302-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="66302-125">Relationships</span></span>
<span data-ttu-id="66302-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="66302-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="66302-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="66302-127">JSON Representation</span></span>
<span data-ttu-id="66302-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="66302-128">Here is a JSON representation of the resource.</span></span>
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





