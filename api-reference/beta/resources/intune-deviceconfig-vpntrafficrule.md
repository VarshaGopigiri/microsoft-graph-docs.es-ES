---
title: tipo de recurso vpnTrafficRule
description: Definición de la regla de tráfico de VPN.
ms.openlocfilehash: 564528cf0c0ae39785a2cc43dc800d8dbdf7d285
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084974"
---
# <a name="vpntrafficrule-resource-type"></a><span data-ttu-id="8e8dd-103">tipo de recurso vpnTrafficRule</span><span class="sxs-lookup"><span data-stu-id="8e8dd-103">vpnTrafficRule resource type</span></span>

> <span data-ttu-id="8e8dd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8e8dd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8e8dd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8e8dd-107">Definición de la regla de tráfico de VPN.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-107">VPN Traffic Rule definition.</span></span>
## <a name="properties"></a><span data-ttu-id="8e8dd-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e8dd-108">Properties</span></span>
|<span data-ttu-id="8e8dd-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8e8dd-109">Property</span></span>|<span data-ttu-id="8e8dd-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e8dd-110">Type</span></span>|<span data-ttu-id="8e8dd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e8dd-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8e8dd-112">name</span><span class="sxs-lookup"><span data-stu-id="8e8dd-112">name</span></span>|<span data-ttu-id="8e8dd-113">String</span><span class="sxs-lookup"><span data-stu-id="8e8dd-113">String</span></span>|<span data-ttu-id="8e8dd-114">Nombre.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-114">Name.</span></span>|
|<span data-ttu-id="8e8dd-115">protocolos</span><span class="sxs-lookup"><span data-stu-id="8e8dd-115">protocols</span></span>|<span data-ttu-id="8e8dd-116">Int32</span><span class="sxs-lookup"><span data-stu-id="8e8dd-116">Int32</span></span>|<span data-ttu-id="8e8dd-117">Protocolos (0-255).</span><span class="sxs-lookup"><span data-stu-id="8e8dd-117">Protocols (0-255).</span></span> <span data-ttu-id="8e8dd-118">Valores válidos de 0 a 255</span><span class="sxs-lookup"><span data-stu-id="8e8dd-118">Valid values 0 to 255</span></span>|
|<span data-ttu-id="8e8dd-119">localPortRanges</span><span class="sxs-lookup"><span data-stu-id="8e8dd-119">localPortRanges</span></span>|<span data-ttu-id="8e8dd-120">colección de [numberRange](../resources/intune-deviceconfig-numberrange.md)</span><span class="sxs-lookup"><span data-stu-id="8e8dd-120">[numberRange](../resources/intune-deviceconfig-numberrange.md) collection</span></span>|<span data-ttu-id="8e8dd-121">Intervalo de puertos locales se puede establecer sólo al protocolo es TCP o UDP (6 o 17).</span><span class="sxs-lookup"><span data-stu-id="8e8dd-121">Local port range can be set only when protocol is either TCP or UDP (6 or 17).</span></span> <span data-ttu-id="8e8dd-122">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-122">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8e8dd-123">remotePortRanges</span><span class="sxs-lookup"><span data-stu-id="8e8dd-123">remotePortRanges</span></span>|<span data-ttu-id="8e8dd-124">colección de [numberRange](../resources/intune-deviceconfig-numberrange.md)</span><span class="sxs-lookup"><span data-stu-id="8e8dd-124">[numberRange](../resources/intune-deviceconfig-numberrange.md) collection</span></span>|<span data-ttu-id="8e8dd-125">Intervalo de puertos remotos se puede establecer sólo al protocolo es TCP o UDP (6 o 17).</span><span class="sxs-lookup"><span data-stu-id="8e8dd-125">Remote port range can be set only when protocol is either TCP or UDP (6 or 17).</span></span> <span data-ttu-id="8e8dd-126">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-126">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8e8dd-127">localAddressRanges</span><span class="sxs-lookup"><span data-stu-id="8e8dd-127">localAddressRanges</span></span>|<span data-ttu-id="8e8dd-128">colección de [iPv4Range](../resources/intune-shared-ipv4range.md)</span><span class="sxs-lookup"><span data-stu-id="8e8dd-128">[iPv4Range](../resources/intune-shared-ipv4range.md) collection</span></span>|<span data-ttu-id="8e8dd-129">Intervalo de direcciones local.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-129">Local address range.</span></span> <span data-ttu-id="8e8dd-130">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-130">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8e8dd-131">remoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="8e8dd-131">remoteAddressRanges</span></span>|<span data-ttu-id="8e8dd-132">colección de [iPv4Range](../resources/intune-shared-ipv4range.md)</span><span class="sxs-lookup"><span data-stu-id="8e8dd-132">[iPv4Range](../resources/intune-shared-ipv4range.md) collection</span></span>|<span data-ttu-id="8e8dd-133">Intervalo de direcciones remoto.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-133">Remote address range.</span></span> <span data-ttu-id="8e8dd-134">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-134">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8e8dd-135">appId</span><span class="sxs-lookup"><span data-stu-id="8e8dd-135">appId</span></span>|<span data-ttu-id="8e8dd-136">cadena</span><span class="sxs-lookup"><span data-stu-id="8e8dd-136">String</span></span>|<span data-ttu-id="8e8dd-137">Identificador de la aplicación, si se desencadena esta regla de tráfico por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-137">App identifier, if this traffic rule is triggered by an app.</span></span>|
|<span data-ttu-id="8e8dd-138">tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="8e8dd-138">appType</span></span>|[<span data-ttu-id="8e8dd-139">vpnTrafficRuleAppType</span><span class="sxs-lookup"><span data-stu-id="8e8dd-139">vpnTrafficRuleAppType</span></span>](../resources/intune-deviceconfig-vpntrafficruleapptype.md)|<span data-ttu-id="8e8dd-140">Tipo de aplicación, si se desencadena esta regla de tráfico por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-140">App type, if this traffic rule is triggered by an app.</span></span> <span data-ttu-id="8e8dd-141">Los valores posibles son: `none`, `desktop` y `universal`.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-141">Possible values are: `none`, `desktop`, `universal`.</span></span>|
|<span data-ttu-id="8e8dd-142">routingPolicyType</span><span class="sxs-lookup"><span data-stu-id="8e8dd-142">routingPolicyType</span></span>|[<span data-ttu-id="8e8dd-143">vpnTrafficRuleRoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="8e8dd-143">vpnTrafficRuleRoutingPolicyType</span></span>](../resources/intune-deviceconfig-vpntrafficruleroutingpolicytype.md)|<span data-ttu-id="8e8dd-144">Cuando aplicación desencadena, indica si se debe habilitar el túnel dividido a lo largo de esta ruta.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-144">When app triggered, indicates whether to enable split tunneling along this route.</span></span> <span data-ttu-id="8e8dd-145">Los valores posibles son: `none`, `splitTunnel` y `forceTunnel`.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-145">Possible values are: `none`, `splitTunnel`, `forceTunnel`.</span></span>|
|<span data-ttu-id="8e8dd-146">notificaciones</span><span class="sxs-lookup"><span data-stu-id="8e8dd-146">claims</span></span>|<span data-ttu-id="8e8dd-147">String</span><span class="sxs-lookup"><span data-stu-id="8e8dd-147">String</span></span>|<span data-ttu-id="8e8dd-148">Notificaciones asociados con esta regla de tráfico.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-148">Claims associated with this traffic rule.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8e8dd-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8e8dd-149">Relationships</span></span>
<span data-ttu-id="8e8dd-150">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8e8dd-150">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8e8dd-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8e8dd-151">JSON Representation</span></span>
<span data-ttu-id="8e8dd-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8e8dd-152">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnTrafficRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnTrafficRule",
  "name": "String",
  "protocols": 1024,
  "localPortRanges": [
    {
      "@odata.type": "microsoft.graph.numberRange",
      "lowerNumber": 1024,
      "upperNumber": 1024
    }
  ],
  "remotePortRanges": [
    {
      "@odata.type": "microsoft.graph.numberRange",
      "lowerNumber": 1024,
      "upperNumber": 1024
    }
  ],
  "localAddressRanges": [
    {
      "@odata.type": "microsoft.graph.iPv4Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "remoteAddressRanges": [
    {
      "@odata.type": "microsoft.graph.iPv4Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "appId": "String",
  "appType": "String",
  "routingPolicyType": "String",
  "claims": "String"
}
```





