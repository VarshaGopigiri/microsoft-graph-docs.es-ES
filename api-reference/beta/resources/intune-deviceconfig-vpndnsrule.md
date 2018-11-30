---
title: tipo de recurso vpnDnsRule
description: Definición de la regla de DNS de VPN.
ms.openlocfilehash: dcb6a0d3a0cd709e8a88835c553f9f29cb094e57
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084910"
---
# <a name="vpndnsrule-resource-type"></a><span data-ttu-id="82c12-103">tipo de recurso vpnDnsRule</span><span class="sxs-lookup"><span data-stu-id="82c12-103">vpnDnsRule resource type</span></span>

> <span data-ttu-id="82c12-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="82c12-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="82c12-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="82c12-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="82c12-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="82c12-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82c12-107">Definición de la regla de DNS de VPN.</span><span class="sxs-lookup"><span data-stu-id="82c12-107">VPN DNS Rule definition.</span></span>
## <a name="properties"></a><span data-ttu-id="82c12-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82c12-108">Properties</span></span>
|<span data-ttu-id="82c12-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82c12-109">Property</span></span>|<span data-ttu-id="82c12-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="82c12-110">Type</span></span>|<span data-ttu-id="82c12-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="82c12-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82c12-112">name</span><span class="sxs-lookup"><span data-stu-id="82c12-112">name</span></span>|<span data-ttu-id="82c12-113">String</span><span class="sxs-lookup"><span data-stu-id="82c12-113">String</span></span>|<span data-ttu-id="82c12-114">Nombre.</span><span class="sxs-lookup"><span data-stu-id="82c12-114">Name.</span></span>|
|<span data-ttu-id="82c12-115">servidores</span><span class="sxs-lookup"><span data-stu-id="82c12-115">servers</span></span>|<span data-ttu-id="82c12-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="82c12-116">String collection</span></span>|<span data-ttu-id="82c12-117">Servidores.</span><span class="sxs-lookup"><span data-stu-id="82c12-117">Servers.</span></span>|
|<span data-ttu-id="82c12-118">proxyServerUri</span><span class="sxs-lookup"><span data-stu-id="82c12-118">proxyServerUri</span></span>|<span data-ttu-id="82c12-119">String</span><span class="sxs-lookup"><span data-stu-id="82c12-119">String</span></span>|<span data-ttu-id="82c12-120">Uri del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="82c12-120">Proxy Server Uri.</span></span>|

## <a name="relationships"></a><span data-ttu-id="82c12-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="82c12-121">Relationships</span></span>
<span data-ttu-id="82c12-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="82c12-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="82c12-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="82c12-123">JSON Representation</span></span>
<span data-ttu-id="82c12-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="82c12-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnDnsRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnDnsRule",
  "name": "String",
  "servers": [
    "String"
  ],
  "proxyServerUri": "String"
}
```





