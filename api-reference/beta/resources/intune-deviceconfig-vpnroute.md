---
title: tipo de recurso vpnRoute
description: Definición de la ruta de VPN.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 43924b76a76060ac6576657d172757a503204a82
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927593"
---
# <a name="vpnroute-resource-type"></a><span data-ttu-id="8749e-103">tipo de recurso vpnRoute</span><span class="sxs-lookup"><span data-stu-id="8749e-103">vpnRoute resource type</span></span>

> <span data-ttu-id="8749e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8749e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8749e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8749e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8749e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8749e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8749e-107">Definición de la ruta de VPN.</span><span class="sxs-lookup"><span data-stu-id="8749e-107">VPN Route definition.</span></span>
## <a name="properties"></a><span data-ttu-id="8749e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8749e-108">Properties</span></span>
|<span data-ttu-id="8749e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8749e-109">Property</span></span>|<span data-ttu-id="8749e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8749e-110">Type</span></span>|<span data-ttu-id="8749e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8749e-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8749e-112">destinationPrefix</span><span class="sxs-lookup"><span data-stu-id="8749e-112">destinationPrefix</span></span>|<span data-ttu-id="8749e-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="8749e-113">String</span></span>|<span data-ttu-id="8749e-114">Prefijo de destino (dirección IPv4 o v6).</span><span class="sxs-lookup"><span data-stu-id="8749e-114">Destination prefix (IPv4/v6 address).</span></span>|
|<span data-ttu-id="8749e-115">prefixSize</span><span class="sxs-lookup"><span data-stu-id="8749e-115">prefixSize</span></span>|<span data-ttu-id="8749e-116">Int32</span><span class="sxs-lookup"><span data-stu-id="8749e-116">Int32</span></span>|<span data-ttu-id="8749e-117">Tamaño del prefijo.</span><span class="sxs-lookup"><span data-stu-id="8749e-117">Prefix size.</span></span> <span data-ttu-id="8749e-118">(1-32).</span><span class="sxs-lookup"><span data-stu-id="8749e-118">(1-32).</span></span> <span data-ttu-id="8749e-119">Valores válidos de 1 a 32</span><span class="sxs-lookup"><span data-stu-id="8749e-119">Valid values 1 to 32</span></span>|

## <a name="relationships"></a><span data-ttu-id="8749e-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8749e-120">Relationships</span></span>
<span data-ttu-id="8749e-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8749e-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8749e-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8749e-122">JSON Representation</span></span>
<span data-ttu-id="8749e-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8749e-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnRoute"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnRoute",
  "destinationPrefix": "String",
  "prefixSize": 1024
}
```





