---
title: tipo de recurso vpnRoute
description: Definición de la ruta de VPN.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: eaa74a1cef7d2eee8148e240cd80ca72f94adcb4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860574"
---
# <a name="vpnroute-resource-type"></a><span data-ttu-id="eb0dc-103">tipo de recurso vpnRoute</span><span class="sxs-lookup"><span data-stu-id="eb0dc-103">vpnRoute resource type</span></span>

> <span data-ttu-id="eb0dc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb0dc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb0dc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb0dc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eb0dc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb0dc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb0dc-107">Definición de la ruta de VPN.</span><span class="sxs-lookup"><span data-stu-id="eb0dc-107">VPN Route definition.</span></span>
## <a name="properties"></a><span data-ttu-id="eb0dc-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb0dc-108">Properties</span></span>
|<span data-ttu-id="eb0dc-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb0dc-109">Property</span></span>|<span data-ttu-id="eb0dc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb0dc-110">Type</span></span>|<span data-ttu-id="eb0dc-111">Description</span><span class="sxs-lookup"><span data-stu-id="eb0dc-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eb0dc-112">destinationPrefix</span><span class="sxs-lookup"><span data-stu-id="eb0dc-112">destinationPrefix</span></span>|<span data-ttu-id="eb0dc-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb0dc-113">String</span></span>|<span data-ttu-id="eb0dc-114">Prefijo de destino (dirección IPv4 o v6).</span><span class="sxs-lookup"><span data-stu-id="eb0dc-114">Destination prefix (IPv4/v6 address).</span></span>|
|<span data-ttu-id="eb0dc-115">prefixSize</span><span class="sxs-lookup"><span data-stu-id="eb0dc-115">prefixSize</span></span>|<span data-ttu-id="eb0dc-116">Int32</span><span class="sxs-lookup"><span data-stu-id="eb0dc-116">Int32</span></span>|<span data-ttu-id="eb0dc-117">Tamaño del prefijo.</span><span class="sxs-lookup"><span data-stu-id="eb0dc-117">Prefix size.</span></span> <span data-ttu-id="eb0dc-118">(1-32).</span><span class="sxs-lookup"><span data-stu-id="eb0dc-118">(1-32).</span></span> <span data-ttu-id="eb0dc-119">Valores válidos de 1 a 32</span><span class="sxs-lookup"><span data-stu-id="eb0dc-119">Valid values 1 to 32</span></span>|

## <a name="relationships"></a><span data-ttu-id="eb0dc-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eb0dc-120">Relationships</span></span>
<span data-ttu-id="eb0dc-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="eb0dc-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="eb0dc-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eb0dc-122">JSON Representation</span></span>
<span data-ttu-id="eb0dc-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="eb0dc-123">Here is a JSON representation of the resource.</span></span>
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





