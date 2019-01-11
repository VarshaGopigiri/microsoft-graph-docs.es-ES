---
title: tipo de recurso de keyValue
description: Definición de valor de clave.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: aae0fea85c5dd4f647a72c0fe66890bd8b82520b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885018"
---
# <a name="keyvalue-resource-type"></a><span data-ttu-id="c5ca6-103">tipo de recurso de keyValue</span><span class="sxs-lookup"><span data-stu-id="c5ca6-103">keyValue resource type</span></span>

> <span data-ttu-id="c5ca6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5ca6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5ca6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5ca6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c5ca6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c5ca6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c5ca6-107">Definición de valor de clave.</span><span class="sxs-lookup"><span data-stu-id="c5ca6-107">Key Value definition.</span></span>
## <a name="properties"></a><span data-ttu-id="c5ca6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5ca6-108">Properties</span></span>
|<span data-ttu-id="c5ca6-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5ca6-109">Property</span></span>|<span data-ttu-id="c5ca6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5ca6-110">Type</span></span>|<span data-ttu-id="c5ca6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5ca6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c5ca6-112">Key</span><span class="sxs-lookup"><span data-stu-id="c5ca6-112">key</span></span>|<span data-ttu-id="c5ca6-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="c5ca6-113">String</span></span>|<span data-ttu-id="c5ca6-114">Clave.</span><span class="sxs-lookup"><span data-stu-id="c5ca6-114">Key.</span></span>|
|<span data-ttu-id="c5ca6-115">valor</span><span class="sxs-lookup"><span data-stu-id="c5ca6-115">value</span></span>|<span data-ttu-id="c5ca6-116">cadena</span><span class="sxs-lookup"><span data-stu-id="c5ca6-116">String</span></span>|<span data-ttu-id="c5ca6-117">Valor.</span><span class="sxs-lookup"><span data-stu-id="c5ca6-117">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c5ca6-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c5ca6-118">Relationships</span></span>
<span data-ttu-id="c5ca6-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c5ca6-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c5ca6-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c5ca6-120">JSON Representation</span></span>
<span data-ttu-id="c5ca6-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c5ca6-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.keyValue"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.keyValue",
  "key": "String",
  "value": "String"
}
```





