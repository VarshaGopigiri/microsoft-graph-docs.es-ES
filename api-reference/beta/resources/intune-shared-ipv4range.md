---
title: Tipo de recurso iPv4Range
description: Intervalo IPv4
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 57bcaabfc5155e6b6733de2dc228dd240515281b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980184"
---
# <a name="ipv4range-resource-type"></a><span data-ttu-id="1834d-103">Tipo de recurso iPv4Range</span><span class="sxs-lookup"><span data-stu-id="1834d-103">iPv4Range resource type</span></span>

> <span data-ttu-id="1834d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1834d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1834d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1834d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1834d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1834d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1834d-107">Intervalo IPv4</span><span class="sxs-lookup"><span data-stu-id="1834d-107">IP V4 range</span></span>

<span data-ttu-id="1834d-108">Hereda de [ipRange](../resources/intune-shared-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="1834d-108">Inherits from [ipRange](../resources/intune-shared-iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="1834d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1834d-109">Properties</span></span>
|<span data-ttu-id="1834d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1834d-110">Property</span></span>|<span data-ttu-id="1834d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1834d-111">Type</span></span>|<span data-ttu-id="1834d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1834d-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1834d-113">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="1834d-113">lowerAddress</span></span>|<span data-ttu-id="1834d-114">cadena</span><span class="sxs-lookup"><span data-stu-id="1834d-114">String</span></span>|<span data-ttu-id="1834d-115">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="1834d-115">Lower IP Address</span></span>|
|<span data-ttu-id="1834d-116">upperAddress</span><span class="sxs-lookup"><span data-stu-id="1834d-116">upperAddress</span></span>|<span data-ttu-id="1834d-117">cadena</span><span class="sxs-lookup"><span data-stu-id="1834d-117">String</span></span>|<span data-ttu-id="1834d-118">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="1834d-118">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="1834d-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1834d-119">Relationships</span></span>
<span data-ttu-id="1834d-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1834d-120">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="1834d-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1834d-121">JSON Representation</span></span>
<span data-ttu-id="1834d-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1834d-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



