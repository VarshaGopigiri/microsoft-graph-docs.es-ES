---
title: tipo de recurso windows10VpnProxyServer
description: Servidor de Proxy VPN.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a4b34d105900478a1bcbc811e782e1ceaf94f251
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912277"
---
# <a name="windows10vpnproxyserver-resource-type"></a><span data-ttu-id="44903-103">tipo de recurso windows10VpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="44903-103">windows10VpnProxyServer resource type</span></span>

> <span data-ttu-id="44903-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="44903-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="44903-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="44903-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="44903-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="44903-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="44903-107">Servidor de Proxy VPN.</span><span class="sxs-lookup"><span data-stu-id="44903-107">VPN Proxy Server.</span></span>

<span data-ttu-id="44903-108">Hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="44903-108">Inherits from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>

## <a name="properties"></a><span data-ttu-id="44903-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44903-109">Properties</span></span>
|<span data-ttu-id="44903-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="44903-110">Property</span></span>|<span data-ttu-id="44903-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="44903-111">Type</span></span>|<span data-ttu-id="44903-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="44903-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="44903-113">automaticConfigurationScriptUrl</span><span class="sxs-lookup"><span data-stu-id="44903-113">automaticConfigurationScriptUrl</span></span>|<span data-ttu-id="44903-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="44903-114">String</span></span>|<span data-ttu-id="44903-115">Url de secuencia de comandos de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="44903-115">Proxy's automatic configuration script url.</span></span> <span data-ttu-id="44903-116">Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="44903-116">Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="44903-117">address</span><span class="sxs-lookup"><span data-stu-id="44903-117">address</span></span>|<span data-ttu-id="44903-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="44903-118">String</span></span>|<span data-ttu-id="44903-119">Dirección.</span><span class="sxs-lookup"><span data-stu-id="44903-119">Address.</span></span> <span data-ttu-id="44903-120">Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="44903-120">Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="44903-121">port</span><span class="sxs-lookup"><span data-stu-id="44903-121">port</span></span>|<span data-ttu-id="44903-122">Int32</span><span class="sxs-lookup"><span data-stu-id="44903-122">Int32</span></span>|<span data-ttu-id="44903-123">Puerto.</span><span class="sxs-lookup"><span data-stu-id="44903-123">Port.</span></span> <span data-ttu-id="44903-124">Válido valores heredada de 0 a 65535 de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span><span class="sxs-lookup"><span data-stu-id="44903-124">Valid values 0 to 65535 Inherited from [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)</span></span>|
|<span data-ttu-id="44903-125">bypassProxyServerForLocalAddress</span><span class="sxs-lookup"><span data-stu-id="44903-125">bypassProxyServerForLocalAddress</span></span>|<span data-ttu-id="44903-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="44903-126">Boolean</span></span>|<span data-ttu-id="44903-127">No usar servidor proxy para direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="44903-127">Bypass proxy server for local address.</span></span>|

## <a name="relationships"></a><span data-ttu-id="44903-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="44903-128">Relationships</span></span>
<span data-ttu-id="44903-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="44903-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="44903-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="44903-130">JSON Representation</span></span>
<span data-ttu-id="44903-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="44903-131">Here is a JSON representation of the resource.</span></span>
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





