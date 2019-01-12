---
title: Tipo de recurso iPv4Range
description: Intervalo IPv4
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2c260796259ce6084add7eadb48192ea50c209c7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931933"
---
# <a name="ipv4range-resource-type"></a><span data-ttu-id="81a16-103">Tipo de recurso iPv4Range</span><span class="sxs-lookup"><span data-stu-id="81a16-103">iPv4Range resource type</span></span>

> <span data-ttu-id="81a16-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="81a16-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="81a16-105">Intervalo IPv4</span><span class="sxs-lookup"><span data-stu-id="81a16-105">IP V4 range</span></span>

<span data-ttu-id="81a16-106">Hereda de [ipRange](../resources/intune-mam-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="81a16-106">Inherits from [ipRange](../resources/intune-mam-iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="81a16-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81a16-107">Properties</span></span>
|<span data-ttu-id="81a16-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="81a16-108">Property</span></span>|<span data-ttu-id="81a16-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="81a16-109">Type</span></span>|<span data-ttu-id="81a16-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="81a16-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="81a16-111">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="81a16-111">lowerAddress</span></span>|<span data-ttu-id="81a16-112">cadena</span><span class="sxs-lookup"><span data-stu-id="81a16-112">String</span></span>|<span data-ttu-id="81a16-113">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="81a16-113">Lower IP Address</span></span>|
|<span data-ttu-id="81a16-114">upperAddress</span><span class="sxs-lookup"><span data-stu-id="81a16-114">upperAddress</span></span>|<span data-ttu-id="81a16-115">cadena</span><span class="sxs-lookup"><span data-stu-id="81a16-115">String</span></span>|<span data-ttu-id="81a16-116">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="81a16-116">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="81a16-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="81a16-117">Relationships</span></span>
<span data-ttu-id="81a16-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="81a16-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="81a16-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="81a16-119">JSON Representation</span></span>
<span data-ttu-id="81a16-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="81a16-120">Here is a JSON representation of the resource.</span></span>
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



