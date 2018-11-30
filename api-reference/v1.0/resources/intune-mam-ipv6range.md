---
title: Tipo de recurso iPv6Range
description: Intervalo IPv6
ms.openlocfilehash: c2f17529b589fc2d7837f6a8f539ff64d5d82dd9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032617"
---
# <a name="ipv6range-resource-type"></a><span data-ttu-id="65872-103">Tipo de recurso iPv6Range</span><span class="sxs-lookup"><span data-stu-id="65872-103">iPv6Range resource type</span></span>

> <span data-ttu-id="65872-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="65872-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="65872-105">Intervalo IPv6</span><span class="sxs-lookup"><span data-stu-id="65872-105">IP V6 range</span></span>

<span data-ttu-id="65872-106">Hereda de [ipRange](../resources/intune-mam-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="65872-106">Inherits from [ipRange](../resources/intune-mam-iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="65872-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65872-107">Properties</span></span>
|<span data-ttu-id="65872-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65872-108">Property</span></span>|<span data-ttu-id="65872-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="65872-109">Type</span></span>|<span data-ttu-id="65872-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="65872-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="65872-111">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="65872-111">lowerAddress</span></span>|<span data-ttu-id="65872-112">cadena</span><span class="sxs-lookup"><span data-stu-id="65872-112">String</span></span>|<span data-ttu-id="65872-113">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="65872-113">Lower IP Address</span></span>|
|<span data-ttu-id="65872-114">upperAddress</span><span class="sxs-lookup"><span data-stu-id="65872-114">upperAddress</span></span>|<span data-ttu-id="65872-115">cadena</span><span class="sxs-lookup"><span data-stu-id="65872-115">String</span></span>|<span data-ttu-id="65872-116">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="65872-116">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="65872-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="65872-117">Relationships</span></span>
<span data-ttu-id="65872-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="65872-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="65872-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="65872-119">JSON Representation</span></span>
<span data-ttu-id="65872-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="65872-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iPv6Range"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iPv6Range",
  "lowerAddress": "String",
  "upperAddress": "String"
}
```



