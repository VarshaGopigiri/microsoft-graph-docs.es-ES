---
title: Tipo de recurso keyValuePair
description: Par clave-valor para almacenar la configuración personalizada
author: tfitzmac
ms.openlocfilehash: f6438d97376d46f66e02026acc87c948ab2a91bb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329319"
---
# <a name="keyvaluepair-resource-type"></a><span data-ttu-id="0c12f-103">Tipo de recurso keyValuePair</span><span class="sxs-lookup"><span data-stu-id="0c12f-103">keyValuePair resource type</span></span>

> <span data-ttu-id="0c12f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0c12f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0c12f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0c12f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0c12f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0c12f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0c12f-107">Par clave-valor para almacenar la configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="0c12f-107">Key value pair for storing custom settings</span></span>
## <a name="properties"></a><span data-ttu-id="0c12f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c12f-108">Properties</span></span>
|<span data-ttu-id="0c12f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c12f-109">Property</span></span>|<span data-ttu-id="0c12f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c12f-110">Type</span></span>|<span data-ttu-id="0c12f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c12f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0c12f-112">name</span><span class="sxs-lookup"><span data-stu-id="0c12f-112">name</span></span>|<span data-ttu-id="0c12f-113">cadena</span><span class="sxs-lookup"><span data-stu-id="0c12f-113">String</span></span>|<span data-ttu-id="0c12f-114">Nombre de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="0c12f-114">Name for this key-value pair</span></span>|
|<span data-ttu-id="0c12f-115">valor</span><span class="sxs-lookup"><span data-stu-id="0c12f-115">value</span></span>|<span data-ttu-id="0c12f-116">cadena</span><span class="sxs-lookup"><span data-stu-id="0c12f-116">String</span></span>|<span data-ttu-id="0c12f-117">Valor de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="0c12f-117">Value for this key-value pair</span></span>|

## <a name="relationships"></a><span data-ttu-id="0c12f-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0c12f-118">Relationships</span></span>
<span data-ttu-id="0c12f-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0c12f-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0c12f-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0c12f-120">JSON Representation</span></span>
<span data-ttu-id="0c12f-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0c12f-121">Here is a JSON representation of the resource.</span></span>
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





