---
title: tipo de recurso windowsNetworkIsolationPolicy
description: Directiva de aislamiento de red de Windows
ms.openlocfilehash: 89c7db0453c76f6ec5016a4701bf357e27c579bc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086617"
---
# <a name="windowsnetworkisolationpolicy-resource-type"></a><span data-ttu-id="83abc-103">tipo de recurso windowsNetworkIsolationPolicy</span><span class="sxs-lookup"><span data-stu-id="83abc-103">windowsNetworkIsolationPolicy resource type</span></span>

> <span data-ttu-id="83abc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="83abc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="83abc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="83abc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="83abc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="83abc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="83abc-107">Directiva de aislamiento de red de Windows</span><span class="sxs-lookup"><span data-stu-id="83abc-107">Windows Network Isolation Policy</span></span>
## <a name="properties"></a><span data-ttu-id="83abc-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83abc-108">Properties</span></span>
|<span data-ttu-id="83abc-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="83abc-109">Property</span></span>|<span data-ttu-id="83abc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="83abc-110">Type</span></span>|<span data-ttu-id="83abc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="83abc-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="83abc-112">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="83abc-112">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="83abc-113">Colección String</span><span class="sxs-lookup"><span data-stu-id="83abc-113">String collection</span></span>|<span data-ttu-id="83abc-114">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="83abc-114">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="83abc-115">Datos de uno de estos dominios que se envía a un dispositivo que se consideran datos de la empresa y protegidas.</span><span class="sxs-lookup"><span data-stu-id="83abc-115">Data from one of these domains that is sent to a device will be considered enterprise data and protected.</span></span> <span data-ttu-id="83abc-116">Estas ubicaciones se considerarán un destino para los datos de la empresa para compartirse a seguros.</span><span class="sxs-lookup"><span data-stu-id="83abc-116">These locations will be considered a safe destination for enterprise data to be shared to.</span></span>|
|<span data-ttu-id="83abc-117">enterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="83abc-117">enterpriseCloudResources</span></span>|<span data-ttu-id="83abc-118">Colección [proxiedDomain](../resources/intune-shared-proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="83abc-118">[proxiedDomain](../resources/intune-shared-proxieddomain.md) collection</span></span>|<span data-ttu-id="83abc-119">Contiene una lista de dominios de recursos de empresa hospedadas en la nube que deben estar protegidos.</span><span class="sxs-lookup"><span data-stu-id="83abc-119">Contains a list of enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="83abc-120">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="83abc-120">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="83abc-121">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="83abc-121">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="83abc-122">Un servidor proxy utilizado para este propósito también debe configurarse con la directiva de EnterpriseInternalProxyServers.</span><span class="sxs-lookup"><span data-stu-id="83abc-122">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy.</span></span> <span data-ttu-id="83abc-123">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="83abc-123">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="83abc-124">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="83abc-124">enterpriseIPRanges</span></span>|<span data-ttu-id="83abc-125">Colección [ipRange](../resources/intune-shared-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="83abc-125">[ipRange](../resources/intune-shared-iprange.md) collection</span></span>|<span data-ttu-id="83abc-126">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="83abc-126">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="83abc-127">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="83abc-127">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="83abc-128">Estas ubicaciones se considerarán un destino para los datos de la empresa para compartirse a seguros.</span><span class="sxs-lookup"><span data-stu-id="83abc-128">These locations will be considered a safe destination for enterprise data to be shared to.</span></span> <span data-ttu-id="83abc-129">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="83abc-129">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="83abc-130">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="83abc-130">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="83abc-131">Colección String</span><span class="sxs-lookup"><span data-stu-id="83abc-131">String collection</span></span>|<span data-ttu-id="83abc-132">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="83abc-132">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="83abc-133">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="83abc-133">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="83abc-134">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="83abc-134">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="83abc-135">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="83abc-135">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="83abc-136">Los servidores proxy se aprovechan sólo en la configuración de la directiva EnterpriseCloudResources para forzar que el tráfico a los recursos de la nube coincidente a través de estos servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="83abc-136">The proxies are only leveraged in configuring the EnterpriseCloudResources policy to force traffic to the matched cloud resources through these proxies.</span></span>|
|<span data-ttu-id="83abc-137">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="83abc-137">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="83abc-138">Booleano</span><span class="sxs-lookup"><span data-stu-id="83abc-138">Boolean</span></span>|<span data-ttu-id="83abc-139">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="83abc-139">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="83abc-140">Valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="83abc-140">Default is false.</span></span>|
|<span data-ttu-id="83abc-141">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="83abc-141">enterpriseProxyServers</span></span>|<span data-ttu-id="83abc-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="83abc-142">String collection</span></span>|<span data-ttu-id="83abc-143">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="83abc-143">This is a list of proxy servers.</span></span> <span data-ttu-id="83abc-144">Cualquier servidor no en esta lista se considera que no sea de empresa.</span><span class="sxs-lookup"><span data-stu-id="83abc-144">Any server not on this list is considered non-enterprise.</span></span>|
|<span data-ttu-id="83abc-145">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="83abc-145">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="83abc-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="83abc-146">Boolean</span></span>|<span data-ttu-id="83abc-147">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="83abc-147">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="83abc-148">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="83abc-148">Default is false</span></span>|
|<span data-ttu-id="83abc-149">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="83abc-149">neutralDomainResources</span></span>|<span data-ttu-id="83abc-150">Colección String</span><span class="sxs-lookup"><span data-stu-id="83abc-150">String collection</span></span>|<span data-ttu-id="83abc-151">Lista de nombres de dominio que puede usar para el recurso de trabajo o personal.</span><span class="sxs-lookup"><span data-stu-id="83abc-151">List of domain names that can used for work or personal resource.</span></span>|

## <a name="relationships"></a><span data-ttu-id="83abc-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="83abc-152">Relationships</span></span>
<span data-ttu-id="83abc-153">Ninguna</span><span class="sxs-lookup"><span data-stu-id="83abc-153">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="83abc-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="83abc-154">JSON Representation</span></span>
<span data-ttu-id="83abc-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="83abc-155">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsNetworkIsolationPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsNetworkIsolationPolicy",
  "enterpriseNetworkDomainNames": [
    "String"
  ],
  "enterpriseCloudResources": [
    {
      "@odata.type": "microsoft.graph.proxiedDomain",
      "ipAddressOrFQDN": "String",
      "proxy": "String"
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.iPv6Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "enterpriseInternalProxyServers": [
    "String"
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    "String"
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    "String"
  ]
}
```




