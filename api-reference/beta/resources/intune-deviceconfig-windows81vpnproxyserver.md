---
title: tipo de recurso windows81VpnProxyServer
description: Servidor de Proxy VPN.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d276ee7ac84bfe86c197025c05bf1a119b85e06c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917968"
---
# <a name="windows81vpnproxyserver-resource-type"></a><span data-ttu-id="c3a85-103">tipo de recurso windows81VpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="c3a85-103">windows81VpnProxyServer resource type</span></span>

> <span data-ttu-id="c3a85-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c3a85-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c3a85-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c3a85-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c3a85-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c3a85-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c3a85-107">Servidor de Proxy VPN.</span><span class="sxs-lookup"><span data-stu-id="c3a85-107">VPN Proxy Server.</span></span>

<span data-ttu-id="c3a85-108">Hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="c3a85-108">Inherits from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c3a85-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c3a85-109">Properties</span></span>
|<span data-ttu-id="c3a85-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c3a85-110">Property</span></span>|<span data-ttu-id="c3a85-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3a85-111">Type</span></span>|<span data-ttu-id="c3a85-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3a85-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c3a85-113">automaticConfigurationScriptUrl</span><span class="sxs-lookup"><span data-stu-id="c3a85-113">automaticConfigurationScriptUrl</span></span>|<span data-ttu-id="c3a85-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="c3a85-114">String</span></span>|<span data-ttu-id="c3a85-115">Url de secuencia de comandos de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="c3a85-115">Proxy's automatic configuration script url.</span></span> <span data-ttu-id="c3a85-116">Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="c3a85-116">Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="c3a85-117">address</span><span class="sxs-lookup"><span data-stu-id="c3a85-117">address</span></span>|<span data-ttu-id="c3a85-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="c3a85-118">String</span></span>|<span data-ttu-id="c3a85-119">Dirección.</span><span class="sxs-lookup"><span data-stu-id="c3a85-119">Address.</span></span> <span data-ttu-id="c3a85-120">Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="c3a85-120">Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="c3a85-121">port</span><span class="sxs-lookup"><span data-stu-id="c3a85-121">port</span></span>|<span data-ttu-id="c3a85-122">Int32</span><span class="sxs-lookup"><span data-stu-id="c3a85-122">Int32</span></span>|<span data-ttu-id="c3a85-123">Puerto.</span><span class="sxs-lookup"><span data-stu-id="c3a85-123">Port.</span></span> <span data-ttu-id="c3a85-124">Válido valores heredada de 0 a 65535 de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="c3a85-124">Valid values 0 to 65535 Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="c3a85-125">automaticallyDetectProxySettings</span><span class="sxs-lookup"><span data-stu-id="c3a85-125">automaticallyDetectProxySettings</span></span>|<span data-ttu-id="c3a85-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="c3a85-126">Boolean</span></span>|<span data-ttu-id="c3a85-127">Detectar automáticamente la configuración de proxy.</span><span class="sxs-lookup"><span data-stu-id="c3a85-127">Automatically detect proxy settings.</span></span>|
|<span data-ttu-id="c3a85-128">bypassProxyServerForLocalAddress</span><span class="sxs-lookup"><span data-stu-id="c3a85-128">bypassProxyServerForLocalAddress</span></span>|<span data-ttu-id="c3a85-129">Booleano</span><span class="sxs-lookup"><span data-stu-id="c3a85-129">Boolean</span></span>|<span data-ttu-id="c3a85-130">No usar servidor proxy para direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="c3a85-130">Bypass proxy server for local address.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c3a85-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c3a85-131">Relationships</span></span>
<span data-ttu-id="c3a85-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c3a85-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c3a85-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c3a85-133">JSON Representation</span></span>
<span data-ttu-id="c3a85-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c3a85-134">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows81VpnProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows81VpnProxyServer",
  "automaticConfigurationScriptUrl": "String",
  "address": "String",
  "port": 1024,
  "automaticallyDetectProxySettings": true,
  "bypassProxyServerForLocalAddress": true
}
```





