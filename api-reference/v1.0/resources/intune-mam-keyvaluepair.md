---
title: Tipo de recurso keyValuePair
description: Par clave-valor para almacenar la configuración personalizada
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: db3e24c1c14cb208be66b7a2b0364ad12b162956
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926445"
---
# <a name="keyvaluepair-resource-type"></a><span data-ttu-id="e7a77-103">Tipo de recurso keyValuePair</span><span class="sxs-lookup"><span data-stu-id="e7a77-103">keyValuePair resource type</span></span>

> <span data-ttu-id="e7a77-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7a77-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7a77-105">Par clave-valor para almacenar la configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="e7a77-105">Key value pair for storing custom settings</span></span>
## <a name="properties"></a><span data-ttu-id="e7a77-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7a77-106">Properties</span></span>
|<span data-ttu-id="e7a77-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7a77-107">Property</span></span>|<span data-ttu-id="e7a77-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7a77-108">Type</span></span>|<span data-ttu-id="e7a77-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7a77-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7a77-110">name</span><span class="sxs-lookup"><span data-stu-id="e7a77-110">name</span></span>|<span data-ttu-id="e7a77-111">cadena</span><span class="sxs-lookup"><span data-stu-id="e7a77-111">String</span></span>|<span data-ttu-id="e7a77-112">Nombre de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="e7a77-112">Name for this key-value pair</span></span>|
|<span data-ttu-id="e7a77-113">valor</span><span class="sxs-lookup"><span data-stu-id="e7a77-113">value</span></span>|<span data-ttu-id="e7a77-114">cadena</span><span class="sxs-lookup"><span data-stu-id="e7a77-114">String</span></span>|<span data-ttu-id="e7a77-115">Valor de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="e7a77-115">Value for this key-value pair</span></span>|

## <a name="relationships"></a><span data-ttu-id="e7a77-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7a77-116">Relationships</span></span>
<span data-ttu-id="e7a77-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e7a77-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e7a77-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7a77-118">JSON Representation</span></span>
<span data-ttu-id="e7a77-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7a77-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.keyValuePair"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.keyValuePair",
  "name": "String",
  "value": "String"
}
```



