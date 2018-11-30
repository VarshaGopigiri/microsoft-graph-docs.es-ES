---
title: tipo de recurso vpnRoute
description: Definición de la ruta de VPN.
ms.openlocfilehash: 385ed5f369660805afa8cf935273b6689fc90173
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088448"
---
# <a name="vpnroute-resource-type"></a><span data-ttu-id="4fe8c-103">tipo de recurso vpnRoute</span><span class="sxs-lookup"><span data-stu-id="4fe8c-103">vpnRoute resource type</span></span>

> <span data-ttu-id="4fe8c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4fe8c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4fe8c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4fe8c-107">Definición de la ruta de VPN.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-107">VPN Route definition.</span></span>
## <a name="properties"></a><span data-ttu-id="4fe8c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4fe8c-108">Properties</span></span>
|<span data-ttu-id="4fe8c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4fe8c-109">Property</span></span>|<span data-ttu-id="4fe8c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fe8c-110">Type</span></span>|<span data-ttu-id="4fe8c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fe8c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4fe8c-112">destinationPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe8c-112">destinationPrefix</span></span>|<span data-ttu-id="4fe8c-113">String</span><span class="sxs-lookup"><span data-stu-id="4fe8c-113">String</span></span>|<span data-ttu-id="4fe8c-114">Prefijo de destino (dirección IPv4 o v6).</span><span class="sxs-lookup"><span data-stu-id="4fe8c-114">Destination prefix (IPv4/v6 address).</span></span>|
|<span data-ttu-id="4fe8c-115">prefixSize</span><span class="sxs-lookup"><span data-stu-id="4fe8c-115">prefixSize</span></span>|<span data-ttu-id="4fe8c-116">Int32</span><span class="sxs-lookup"><span data-stu-id="4fe8c-116">Int32</span></span>|<span data-ttu-id="4fe8c-117">Tamaño del prefijo.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-117">Prefix size.</span></span> <span data-ttu-id="4fe8c-118">(1-32).</span><span class="sxs-lookup"><span data-stu-id="4fe8c-118">(1-32).</span></span> <span data-ttu-id="4fe8c-119">Valores válidos de 1 a 32</span><span class="sxs-lookup"><span data-stu-id="4fe8c-119">Valid values 1 to 32</span></span>|

## <a name="relationships"></a><span data-ttu-id="4fe8c-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4fe8c-120">Relationships</span></span>
<span data-ttu-id="4fe8c-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4fe8c-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4fe8c-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4fe8c-122">JSON Representation</span></span>
<span data-ttu-id="4fe8c-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-123">Here is a JSON representation of the resource.</span></span>
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





