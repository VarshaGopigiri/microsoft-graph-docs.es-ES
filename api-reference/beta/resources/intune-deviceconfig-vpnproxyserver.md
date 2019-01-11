---
title: tipo de recurso vpnProxyServer
description: Servidor de Proxy VPN.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3b4842444bc248e51e1967fcbef4a863ed50498c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867679"
---
# <a name="vpnproxyserver-resource-type"></a><span data-ttu-id="1954e-103">tipo de recurso vpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="1954e-103">vpnProxyServer resource type</span></span>

> <span data-ttu-id="1954e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1954e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1954e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1954e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1954e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1954e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1954e-107">Servidor de Proxy VPN.</span><span class="sxs-lookup"><span data-stu-id="1954e-107">VPN Proxy Server.</span></span>
## <a name="properties"></a><span data-ttu-id="1954e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1954e-108">Properties</span></span>
|<span data-ttu-id="1954e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1954e-109">Property</span></span>|<span data-ttu-id="1954e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="1954e-110">Type</span></span>|<span data-ttu-id="1954e-111">Description</span><span class="sxs-lookup"><span data-stu-id="1954e-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1954e-112">automaticConfigurationScriptUrl</span><span class="sxs-lookup"><span data-stu-id="1954e-112">automaticConfigurationScriptUrl</span></span>|<span data-ttu-id="1954e-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="1954e-113">String</span></span>|<span data-ttu-id="1954e-114">Url de secuencia de comandos de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="1954e-114">Proxy's automatic configuration script url.</span></span>|
|<span data-ttu-id="1954e-115">address</span><span class="sxs-lookup"><span data-stu-id="1954e-115">address</span></span>|<span data-ttu-id="1954e-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="1954e-116">String</span></span>|<span data-ttu-id="1954e-117">Dirección.</span><span class="sxs-lookup"><span data-stu-id="1954e-117">Address.</span></span>|
|<span data-ttu-id="1954e-118">port</span><span class="sxs-lookup"><span data-stu-id="1954e-118">port</span></span>|<span data-ttu-id="1954e-119">Int32</span><span class="sxs-lookup"><span data-stu-id="1954e-119">Int32</span></span>|<span data-ttu-id="1954e-120">Puerto.</span><span class="sxs-lookup"><span data-stu-id="1954e-120">Port.</span></span> <span data-ttu-id="1954e-121">Valores válidos de 0 a 65535</span><span class="sxs-lookup"><span data-stu-id="1954e-121">Valid values 0 to 65535</span></span>|

## <a name="relationships"></a><span data-ttu-id="1954e-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1954e-122">Relationships</span></span>
<span data-ttu-id="1954e-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1954e-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1954e-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1954e-124">JSON Representation</span></span>
<span data-ttu-id="1954e-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1954e-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnProxyServer",
  "automaticConfigurationScriptUrl": "String",
  "address": "String",
  "port": 1024
}
```





