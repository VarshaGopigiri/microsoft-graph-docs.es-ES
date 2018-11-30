---
title: Tipo de recurso iPv6Range
description: Intervalo IPv6
ms.openlocfilehash: ac2834ea68e1ce4aa7e28f7b421ff4e3d031f8fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090880"
---
# <a name="ipv6range-resource-type"></a><span data-ttu-id="75603-103">Tipo de recurso iPv6Range</span><span class="sxs-lookup"><span data-stu-id="75603-103">iPv6Range resource type</span></span>

> <span data-ttu-id="75603-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75603-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75603-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75603-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="75603-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75603-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75603-107">Intervalo IPv6</span><span class="sxs-lookup"><span data-stu-id="75603-107">IP V6 range</span></span>

<span data-ttu-id="75603-108">Hereda de [ipRange](../resources/intune-shared-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="75603-108">Inherits from [ipRange](../resources/intune-shared-iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="75603-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75603-109">Properties</span></span>
|<span data-ttu-id="75603-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75603-110">Property</span></span>|<span data-ttu-id="75603-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="75603-111">Type</span></span>|<span data-ttu-id="75603-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="75603-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75603-113">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="75603-113">lowerAddress</span></span>|<span data-ttu-id="75603-114">cadena</span><span class="sxs-lookup"><span data-stu-id="75603-114">String</span></span>|<span data-ttu-id="75603-115">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="75603-115">Lower IP Address</span></span>|
|<span data-ttu-id="75603-116">upperAddress</span><span class="sxs-lookup"><span data-stu-id="75603-116">upperAddress</span></span>|<span data-ttu-id="75603-117">cadena</span><span class="sxs-lookup"><span data-stu-id="75603-117">String</span></span>|<span data-ttu-id="75603-118">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="75603-118">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="75603-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="75603-119">Relationships</span></span>
<span data-ttu-id="75603-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="75603-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="75603-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75603-121">JSON Representation</span></span>
<span data-ttu-id="75603-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75603-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



