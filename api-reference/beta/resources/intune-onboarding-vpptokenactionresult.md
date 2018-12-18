---
title: tipo de recurso vppTokenActionResult
description: El estado de la acción realizada con un token de programa de compra de volumen de Apple.
author: tfitzmac
ms.openlocfilehash: 0b8b074e879321d0aed361373c49e6ed1fd16e62
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341681"
---
# <a name="vpptokenactionresult-resource-type"></a><span data-ttu-id="2a9e3-103">tipo de recurso vppTokenActionResult</span><span class="sxs-lookup"><span data-stu-id="2a9e3-103">vppTokenActionResult resource type</span></span>

> <span data-ttu-id="2a9e3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a9e3-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a9e3-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a9e3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2a9e3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a9e3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a9e3-107">El estado de la acción realizada con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="2a9e3-107">The status of the action performed with an Apple Volume Purchase Program token.</span></span>
## <a name="properties"></a><span data-ttu-id="2a9e3-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a9e3-108">Properties</span></span>
|<span data-ttu-id="2a9e3-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2a9e3-109">Property</span></span>|<span data-ttu-id="2a9e3-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a9e3-110">Type</span></span>|<span data-ttu-id="2a9e3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a9e3-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a9e3-112">actionName</span><span class="sxs-lookup"><span data-stu-id="2a9e3-112">actionName</span></span>|<span data-ttu-id="2a9e3-113">cadena</span><span class="sxs-lookup"><span data-stu-id="2a9e3-113">String</span></span>|<span data-ttu-id="2a9e3-114">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="2a9e3-114">Action name</span></span>|
|<span data-ttu-id="2a9e3-115">actionState</span><span class="sxs-lookup"><span data-stu-id="2a9e3-115">actionState</span></span>|[<span data-ttu-id="2a9e3-116">actionState</span><span class="sxs-lookup"><span data-stu-id="2a9e3-116">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="2a9e3-117">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="2a9e3-117">State of the action.</span></span> <span data-ttu-id="2a9e3-118">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="2a9e3-118">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="2a9e3-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="2a9e3-119">startDateTime</span></span>|<span data-ttu-id="2a9e3-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2a9e3-120">DateTimeOffset</span></span>|<span data-ttu-id="2a9e3-121">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="2a9e3-121">Time the action was initiated</span></span>|
|<span data-ttu-id="2a9e3-122">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="2a9e3-122">lastUpdatedDateTime</span></span>|<span data-ttu-id="2a9e3-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2a9e3-123">DateTimeOffset</span></span>|<span data-ttu-id="2a9e3-124">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="2a9e3-124">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="2a9e3-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2a9e3-125">Relationships</span></span>
<span data-ttu-id="2a9e3-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2a9e3-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2a9e3-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2a9e3-127">JSON Representation</span></span>
<span data-ttu-id="2a9e3-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2a9e3-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppTokenActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppTokenActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```





