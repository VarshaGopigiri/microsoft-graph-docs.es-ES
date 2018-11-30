---
title: tipo de recurso windows10VpnProxyServer
description: Servidor de Proxy VPN.
ms.openlocfilehash: cae448924087cba4b039eab92c83c8bffc94f9fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086334"
---
# <a name="windows10vpnproxyserver-resource-type"></a><span data-ttu-id="e4289-103">tipo de recurso windows10VpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="e4289-103">windows10VpnProxyServer resource type</span></span>

> <span data-ttu-id="e4289-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4289-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e4289-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e4289-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e4289-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e4289-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e4289-107">Servidor de Proxy VPN.</span><span class="sxs-lookup"><span data-stu-id="e4289-107">VPN Proxy Server.</span></span>

<span data-ttu-id="e4289-108">Hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="e4289-108">Inherits from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e4289-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4289-109">Properties</span></span>
|<span data-ttu-id="e4289-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e4289-110">Property</span></span>|<span data-ttu-id="e4289-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4289-111">Type</span></span>|<span data-ttu-id="e4289-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4289-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e4289-113">automaticConfigurationScriptUrl</span><span class="sxs-lookup"><span data-stu-id="e4289-113">automaticConfigurationScriptUrl</span></span>|<span data-ttu-id="e4289-114">String</span><span class="sxs-lookup"><span data-stu-id="e4289-114">String</span></span>|<span data-ttu-id="e4289-115">Url de secuencia de comandos de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="e4289-115">Proxy's automatic configuration script url.</span></span> <span data-ttu-id="e4289-116">Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="e4289-116">Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="e4289-117">address</span><span class="sxs-lookup"><span data-stu-id="e4289-117">address</span></span>|<span data-ttu-id="e4289-118">String</span><span class="sxs-lookup"><span data-stu-id="e4289-118">String</span></span>|<span data-ttu-id="e4289-119">Dirección.</span><span class="sxs-lookup"><span data-stu-id="e4289-119">Address.</span></span> <span data-ttu-id="e4289-120">Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="e4289-120">Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="e4289-121">port</span><span class="sxs-lookup"><span data-stu-id="e4289-121">port</span></span>|<span data-ttu-id="e4289-122">Int32</span><span class="sxs-lookup"><span data-stu-id="e4289-122">Int32</span></span>|<span data-ttu-id="e4289-123">Puerto.</span><span class="sxs-lookup"><span data-stu-id="e4289-123">Port.</span></span> <span data-ttu-id="e4289-124">Válido valores heredada de 0 a 65535 de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="e4289-124">Valid values 0 to 65535 Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="e4289-125">bypassProxyServerForLocalAddress</span><span class="sxs-lookup"><span data-stu-id="e4289-125">bypassProxyServerForLocalAddress</span></span>|<span data-ttu-id="e4289-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="e4289-126">Boolean</span></span>|<span data-ttu-id="e4289-127">No usar servidor proxy para direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="e4289-127">Bypass proxy server for local address.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e4289-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e4289-128">Relationships</span></span>
<span data-ttu-id="e4289-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e4289-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e4289-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e4289-130">JSON Representation</span></span>
<span data-ttu-id="e4289-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e4289-131">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10VpnProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10VpnProxyServer",
  "automaticConfigurationScriptUrl": "String",
  "address": "String",
  "port": 1024,
  "bypassProxyServerForLocalAddress": true
}
```





