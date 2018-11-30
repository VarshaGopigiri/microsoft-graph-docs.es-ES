---
title: tipo de recurso de keyValue
description: Definición de valor de clave.
ms.openlocfilehash: 7279b48243139b9234b737ceb7d7fb1ad7232451
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085575"
---
# <a name="keyvalue-resource-type"></a><span data-ttu-id="eed6d-103">tipo de recurso de keyValue</span><span class="sxs-lookup"><span data-stu-id="eed6d-103">keyValue resource type</span></span>

> <span data-ttu-id="eed6d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eed6d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eed6d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eed6d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eed6d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eed6d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eed6d-107">Definición de valor de clave.</span><span class="sxs-lookup"><span data-stu-id="eed6d-107">Key Value definition.</span></span>
## <a name="properties"></a><span data-ttu-id="eed6d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eed6d-108">Properties</span></span>
|<span data-ttu-id="eed6d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eed6d-109">Property</span></span>|<span data-ttu-id="eed6d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="eed6d-110">Type</span></span>|<span data-ttu-id="eed6d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="eed6d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eed6d-112">Key</span><span class="sxs-lookup"><span data-stu-id="eed6d-112">key</span></span>|<span data-ttu-id="eed6d-113">String</span><span class="sxs-lookup"><span data-stu-id="eed6d-113">String</span></span>|<span data-ttu-id="eed6d-114">Clave.</span><span class="sxs-lookup"><span data-stu-id="eed6d-114">Key.</span></span>|
|<span data-ttu-id="eed6d-115">valor</span><span class="sxs-lookup"><span data-stu-id="eed6d-115">value</span></span>|<span data-ttu-id="eed6d-116">cadena</span><span class="sxs-lookup"><span data-stu-id="eed6d-116">String</span></span>|<span data-ttu-id="eed6d-117">Valor.</span><span class="sxs-lookup"><span data-stu-id="eed6d-117">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="eed6d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eed6d-118">Relationships</span></span>
<span data-ttu-id="eed6d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="eed6d-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="eed6d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eed6d-120">JSON Representation</span></span>
<span data-ttu-id="eed6d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="eed6d-121">Here is a JSON representation of the resource.</span></span>
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





