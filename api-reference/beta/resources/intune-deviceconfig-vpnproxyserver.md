---
title: tipo de recurso vpnProxyServer
description: Servidor de Proxy VPN.
ms.openlocfilehash: 31e711475bf0f797eead80ca3fe2f3c9af8ba27f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084506"
---
# <a name="vpnproxyserver-resource-type"></a><span data-ttu-id="8af89-103">tipo de recurso vpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="8af89-103">vpnProxyServer resource type</span></span>

> <span data-ttu-id="8af89-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8af89-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8af89-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8af89-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8af89-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8af89-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8af89-107">Servidor de Proxy VPN.</span><span class="sxs-lookup"><span data-stu-id="8af89-107">VPN Proxy Server.</span></span>
## <a name="properties"></a><span data-ttu-id="8af89-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8af89-108">Properties</span></span>
|<span data-ttu-id="8af89-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8af89-109">Property</span></span>|<span data-ttu-id="8af89-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8af89-110">Type</span></span>|<span data-ttu-id="8af89-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8af89-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8af89-112">automaticConfigurationScriptUrl</span><span class="sxs-lookup"><span data-stu-id="8af89-112">automaticConfigurationScriptUrl</span></span>|<span data-ttu-id="8af89-113">String</span><span class="sxs-lookup"><span data-stu-id="8af89-113">String</span></span>|<span data-ttu-id="8af89-114">Url de secuencia de comandos de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="8af89-114">Proxy's automatic configuration script url.</span></span>|
|<span data-ttu-id="8af89-115">address</span><span class="sxs-lookup"><span data-stu-id="8af89-115">address</span></span>|<span data-ttu-id="8af89-116">String</span><span class="sxs-lookup"><span data-stu-id="8af89-116">String</span></span>|<span data-ttu-id="8af89-117">Dirección.</span><span class="sxs-lookup"><span data-stu-id="8af89-117">Address.</span></span>|
|<span data-ttu-id="8af89-118">port</span><span class="sxs-lookup"><span data-stu-id="8af89-118">port</span></span>|<span data-ttu-id="8af89-119">Int32</span><span class="sxs-lookup"><span data-stu-id="8af89-119">Int32</span></span>|<span data-ttu-id="8af89-120">Puerto.</span><span class="sxs-lookup"><span data-stu-id="8af89-120">Port.</span></span> <span data-ttu-id="8af89-121">Valores válidos de 0 a 65535</span><span class="sxs-lookup"><span data-stu-id="8af89-121">Valid values 0 to 65535</span></span>|

## <a name="relationships"></a><span data-ttu-id="8af89-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8af89-122">Relationships</span></span>
<span data-ttu-id="8af89-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8af89-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8af89-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8af89-124">JSON Representation</span></span>
<span data-ttu-id="8af89-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8af89-125">Here is a JSON representation of the resource.</span></span>
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





