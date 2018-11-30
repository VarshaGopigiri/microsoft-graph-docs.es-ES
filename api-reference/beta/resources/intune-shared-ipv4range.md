---
title: Tipo de recurso iPv4Range
description: Intervalo IPv4
ms.openlocfilehash: 9147bb45380ec8d207bf8b4f332efe5a370f3c07
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084225"
---
# <a name="ipv4range-resource-type"></a><span data-ttu-id="27936-103">Tipo de recurso iPv4Range</span><span class="sxs-lookup"><span data-stu-id="27936-103">iPv4Range resource type</span></span>

> <span data-ttu-id="27936-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27936-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27936-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27936-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="27936-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="27936-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="27936-107">Intervalo IPv4</span><span class="sxs-lookup"><span data-stu-id="27936-107">IP V4 range</span></span>

<span data-ttu-id="27936-108">Hereda de [ipRange](../resources/intune-shared-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="27936-108">Inherits from [ipRange](../resources/intune-shared-iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="27936-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27936-109">Properties</span></span>
|<span data-ttu-id="27936-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27936-110">Property</span></span>|<span data-ttu-id="27936-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="27936-111">Type</span></span>|<span data-ttu-id="27936-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="27936-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="27936-113">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="27936-113">lowerAddress</span></span>|<span data-ttu-id="27936-114">cadena</span><span class="sxs-lookup"><span data-stu-id="27936-114">String</span></span>|<span data-ttu-id="27936-115">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="27936-115">Lower IP Address</span></span>|
|<span data-ttu-id="27936-116">upperAddress</span><span class="sxs-lookup"><span data-stu-id="27936-116">upperAddress</span></span>|<span data-ttu-id="27936-117">cadena</span><span class="sxs-lookup"><span data-stu-id="27936-117">String</span></span>|<span data-ttu-id="27936-118">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="27936-118">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="27936-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="27936-119">Relationships</span></span>
<span data-ttu-id="27936-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="27936-120">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="27936-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27936-121">JSON Representation</span></span>
<span data-ttu-id="27936-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="27936-122">Here is a JSON representation of the resource.</span></span>
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



