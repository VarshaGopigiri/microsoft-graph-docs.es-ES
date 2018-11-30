---
title: Tipo de recurso iPv4Range
description: Intervalo IPv4
ms.openlocfilehash: 8b59101e1fcdb5ab88d9c24a0359f8abb1687818
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031432"
---
# <a name="ipv4range-resource-type"></a><span data-ttu-id="45755-103">Tipo de recurso iPv4Range</span><span class="sxs-lookup"><span data-stu-id="45755-103">iPv4Range resource type</span></span>

> <span data-ttu-id="45755-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="45755-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="45755-105">Intervalo IPv4</span><span class="sxs-lookup"><span data-stu-id="45755-105">IP V4 range</span></span>

<span data-ttu-id="45755-106">Hereda de [ipRange](../resources/intune-mam-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="45755-106">Inherits from [ipRange](../resources/intune-mam-iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="45755-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45755-107">Properties</span></span>
|<span data-ttu-id="45755-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="45755-108">Property</span></span>|<span data-ttu-id="45755-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="45755-109">Type</span></span>|<span data-ttu-id="45755-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="45755-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="45755-111">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="45755-111">lowerAddress</span></span>|<span data-ttu-id="45755-112">cadena</span><span class="sxs-lookup"><span data-stu-id="45755-112">String</span></span>|<span data-ttu-id="45755-113">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="45755-113">Lower IP Address</span></span>|
|<span data-ttu-id="45755-114">upperAddress</span><span class="sxs-lookup"><span data-stu-id="45755-114">upperAddress</span></span>|<span data-ttu-id="45755-115">cadena</span><span class="sxs-lookup"><span data-stu-id="45755-115">String</span></span>|<span data-ttu-id="45755-116">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="45755-116">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="45755-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="45755-117">Relationships</span></span>
<span data-ttu-id="45755-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="45755-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="45755-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="45755-119">JSON Representation</span></span>
<span data-ttu-id="45755-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="45755-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iPv4Range"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iPv4Range",
  "lowerAddress": "String",
  "upperAddress": "String"
}
```



