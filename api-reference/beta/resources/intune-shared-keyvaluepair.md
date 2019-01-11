---
title: Tipo de recurso keyValuePair
description: Par clave-valor para almacenar la configuración personalizada
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 056dbe1f8504a89e3551402de7aa7ff7bc0ce866
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858446"
---
# <a name="keyvaluepair-resource-type"></a><span data-ttu-id="022ea-103">Tipo de recurso keyValuePair</span><span class="sxs-lookup"><span data-stu-id="022ea-103">keyValuePair resource type</span></span>

> <span data-ttu-id="022ea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="022ea-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="022ea-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="022ea-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="022ea-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="022ea-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="022ea-107">Par clave-valor para almacenar la configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="022ea-107">Key value pair for storing custom settings</span></span>
## <a name="properties"></a><span data-ttu-id="022ea-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="022ea-108">Properties</span></span>
|<span data-ttu-id="022ea-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="022ea-109">Property</span></span>|<span data-ttu-id="022ea-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="022ea-110">Type</span></span>|<span data-ttu-id="022ea-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="022ea-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="022ea-112">name</span><span class="sxs-lookup"><span data-stu-id="022ea-112">name</span></span>|<span data-ttu-id="022ea-113">cadena</span><span class="sxs-lookup"><span data-stu-id="022ea-113">String</span></span>|<span data-ttu-id="022ea-114">Nombre de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="022ea-114">Name for this key-value pair</span></span>|
|<span data-ttu-id="022ea-115">valor</span><span class="sxs-lookup"><span data-stu-id="022ea-115">value</span></span>|<span data-ttu-id="022ea-116">cadena</span><span class="sxs-lookup"><span data-stu-id="022ea-116">String</span></span>|<span data-ttu-id="022ea-117">Valor de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="022ea-117">Value for this key-value pair</span></span>|

## <a name="relationships"></a><span data-ttu-id="022ea-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="022ea-118">Relationships</span></span>
<span data-ttu-id="022ea-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="022ea-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="022ea-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="022ea-120">JSON Representation</span></span>
<span data-ttu-id="022ea-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="022ea-121">Here is a JSON representation of the resource.</span></span>
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





