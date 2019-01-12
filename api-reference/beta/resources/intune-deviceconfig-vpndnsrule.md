---
title: tipo de recurso vpnDnsRule
description: Definición de la regla de DNS de VPN.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3c928542f749973ac3abea041c8ca60ee74ff8fe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964742"
---
# <a name="vpndnsrule-resource-type"></a><span data-ttu-id="c5ded-103">tipo de recurso vpnDnsRule</span><span class="sxs-lookup"><span data-stu-id="c5ded-103">vpnDnsRule resource type</span></span>

> <span data-ttu-id="c5ded-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5ded-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5ded-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5ded-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c5ded-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c5ded-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c5ded-107">Definición de la regla de DNS de VPN.</span><span class="sxs-lookup"><span data-stu-id="c5ded-107">VPN DNS Rule definition.</span></span>
## <a name="properties"></a><span data-ttu-id="c5ded-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5ded-108">Properties</span></span>
|<span data-ttu-id="c5ded-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5ded-109">Property</span></span>|<span data-ttu-id="c5ded-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5ded-110">Type</span></span>|<span data-ttu-id="c5ded-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5ded-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c5ded-112">name</span><span class="sxs-lookup"><span data-stu-id="c5ded-112">name</span></span>|<span data-ttu-id="c5ded-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="c5ded-113">String</span></span>|<span data-ttu-id="c5ded-114">Nombre.</span><span class="sxs-lookup"><span data-stu-id="c5ded-114">Name.</span></span>|
|<span data-ttu-id="c5ded-115">servidores</span><span class="sxs-lookup"><span data-stu-id="c5ded-115">servers</span></span>|<span data-ttu-id="c5ded-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="c5ded-116">String collection</span></span>|<span data-ttu-id="c5ded-117">Servidores.</span><span class="sxs-lookup"><span data-stu-id="c5ded-117">Servers.</span></span>|
|<span data-ttu-id="c5ded-118">proxyServerUri</span><span class="sxs-lookup"><span data-stu-id="c5ded-118">proxyServerUri</span></span>|<span data-ttu-id="c5ded-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="c5ded-119">String</span></span>|<span data-ttu-id="c5ded-120">Uri del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="c5ded-120">Proxy Server Uri.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c5ded-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c5ded-121">Relationships</span></span>
<span data-ttu-id="c5ded-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c5ded-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c5ded-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c5ded-123">JSON Representation</span></span>
<span data-ttu-id="c5ded-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c5ded-124">Here is a JSON representation of the resource.</span></span>
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





