---
title: tipo de recurso vpnOnDemandRule
description: Definición de la regla de petición de VPN.
ms.openlocfilehash: 366dd373d31b04d4f245c2394a7a6e476710cf84
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085205"
---
# <a name="vpnondemandrule-resource-type"></a><span data-ttu-id="292f7-103">tipo de recurso vpnOnDemandRule</span><span class="sxs-lookup"><span data-stu-id="292f7-103">vpnOnDemandRule resource type</span></span>

> <span data-ttu-id="292f7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="292f7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="292f7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="292f7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="292f7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="292f7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="292f7-107">Definición de la regla de petición de VPN.</span><span class="sxs-lookup"><span data-stu-id="292f7-107">VPN On-Demand Rule definition.</span></span>
## <a name="properties"></a><span data-ttu-id="292f7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="292f7-108">Properties</span></span>
|<span data-ttu-id="292f7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="292f7-109">Property</span></span>|<span data-ttu-id="292f7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="292f7-110">Type</span></span>|<span data-ttu-id="292f7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="292f7-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="292f7-112">SSID</span><span class="sxs-lookup"><span data-stu-id="292f7-112">ssids</span></span>|<span data-ttu-id="292f7-113">Colección String</span><span class="sxs-lookup"><span data-stu-id="292f7-113">String collection</span></span>|<span data-ttu-id="292f7-114">Servicio de red establece identificadores (SSID).</span><span class="sxs-lookup"><span data-stu-id="292f7-114">Network Service Set Identifiers (SSIDs).</span></span>|
|<span data-ttu-id="292f7-115">dnsSearchDomains</span><span class="sxs-lookup"><span data-stu-id="292f7-115">dnsSearchDomains</span></span>|<span data-ttu-id="292f7-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="292f7-116">String collection</span></span>|<span data-ttu-id="292f7-117">Dominios de búsqueda DNS.</span><span class="sxs-lookup"><span data-stu-id="292f7-117">DNS Search Domains.</span></span>|
|<span data-ttu-id="292f7-118">probeUrl</span><span class="sxs-lookup"><span data-stu-id="292f7-118">probeUrl</span></span>|<span data-ttu-id="292f7-119">String</span><span class="sxs-lookup"><span data-stu-id="292f7-119">String</span></span>|<span data-ttu-id="292f7-120">Una dirección URL de sondeo.</span><span class="sxs-lookup"><span data-stu-id="292f7-120">A URL to probe.</span></span> <span data-ttu-id="292f7-121">Si esta dirección URL es correctamente se capturaron (que devuelve un código de estado HTTP 200) sin el redireccionamiento, coincide esta regla.</span><span class="sxs-lookup"><span data-stu-id="292f7-121">If this URL is successfully fetched (returning a 200 HTTP status code) without redirection, this rule matches.</span></span>|
|<span data-ttu-id="292f7-122">action</span><span class="sxs-lookup"><span data-stu-id="292f7-122">action</span></span>|[<span data-ttu-id="292f7-123">vpnOnDemandRuleConnectionAction</span><span class="sxs-lookup"><span data-stu-id="292f7-123">vpnOnDemandRuleConnectionAction</span></span>](../resources/intune-deviceconfig-vpnondemandruleconnectionaction.md)|<span data-ttu-id="292f7-124">Acción.</span><span class="sxs-lookup"><span data-stu-id="292f7-124">Action.</span></span> <span data-ttu-id="292f7-125">Los valores posibles son: `connect`, `evaluateConnection`, `ignore` y `disconnect`.</span><span class="sxs-lookup"><span data-stu-id="292f7-125">Possible values are: `connect`, `evaluateConnection`, `ignore`, `disconnect`.</span></span>|
|<span data-ttu-id="292f7-126">domainAction</span><span class="sxs-lookup"><span data-stu-id="292f7-126">domainAction</span></span>|[<span data-ttu-id="292f7-127">vpnOnDemandRuleConnectionDomainAction</span><span class="sxs-lookup"><span data-stu-id="292f7-127">vpnOnDemandRuleConnectionDomainAction</span></span>](../resources/intune-deviceconfig-vpnondemandruleconnectiondomainaction.md)|<span data-ttu-id="292f7-128">Acción de dominio (sólo se aplica cuando la acción es evaluar la conexión).</span><span class="sxs-lookup"><span data-stu-id="292f7-128">Domain Action (Only applicable when Action is evaluate connection).</span></span> <span data-ttu-id="292f7-129">Los valores posibles son: `connectIfNeeded` y `neverConnect`.</span><span class="sxs-lookup"><span data-stu-id="292f7-129">Possible values are: `connectIfNeeded`, `neverConnect`.</span></span>|
|<span data-ttu-id="292f7-130">dominios</span><span class="sxs-lookup"><span data-stu-id="292f7-130">domains</span></span>|<span data-ttu-id="292f7-131">Colección String</span><span class="sxs-lookup"><span data-stu-id="292f7-131">String collection</span></span>|<span data-ttu-id="292f7-132">Dominios (solo se aplica cuando la acción es evaluar la conexión).</span><span class="sxs-lookup"><span data-stu-id="292f7-132">Domains (Only applicable when Action is evaluate connection).</span></span>|
|<span data-ttu-id="292f7-133">probeRequiredUrl</span><span class="sxs-lookup"><span data-stu-id="292f7-133">probeRequiredUrl</span></span>|<span data-ttu-id="292f7-134">String</span><span class="sxs-lookup"><span data-stu-id="292f7-134">String</span></span>|<span data-ttu-id="292f7-135">Sondeo obligatorio Url (solo se aplica cuando la acción es evaluar la conexión y DomainAction es conectar si es necesario).</span><span class="sxs-lookup"><span data-stu-id="292f7-135">Probe Required Url (Only applicable when Action is evaluate connection and DomainAction is connect if needed).</span></span>|

## <a name="relationships"></a><span data-ttu-id="292f7-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="292f7-136">Relationships</span></span>
<span data-ttu-id="292f7-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="292f7-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="292f7-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="292f7-138">JSON Representation</span></span>
<span data-ttu-id="292f7-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="292f7-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnOnDemandRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnOnDemandRule",
  "ssids": [
    "String"
  ],
  "dnsSearchDomains": [
    "String"
  ],
  "probeUrl": "String",
  "action": "String",
  "domainAction": "String",
  "domains": [
    "String"
  ],
  "probeRequiredUrl": "String"
}
```





