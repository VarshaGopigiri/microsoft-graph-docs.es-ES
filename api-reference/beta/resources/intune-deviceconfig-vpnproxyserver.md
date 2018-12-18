---
title: tipo de recurso vpnProxyServer
description: Servidor de Proxy VPN.
author: tfitzmac
ms.openlocfilehash: f622d476e041fd89a639c14113e273a16aca992f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333477"
---
# <a name="vpnproxyserver-resource-type"></a><span data-ttu-id="cd603-103">tipo de recurso vpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="cd603-103">vpnProxyServer resource type</span></span>

> <span data-ttu-id="cd603-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd603-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd603-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd603-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cd603-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cd603-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cd603-107">Servidor de Proxy VPN.</span><span class="sxs-lookup"><span data-stu-id="cd603-107">VPN Proxy Server.</span></span>
## <a name="properties"></a><span data-ttu-id="cd603-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd603-108">Properties</span></span>
|<span data-ttu-id="cd603-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd603-109">Property</span></span>|<span data-ttu-id="cd603-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd603-110">Type</span></span>|<span data-ttu-id="cd603-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd603-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cd603-112">automaticConfigurationScriptUrl</span><span class="sxs-lookup"><span data-stu-id="cd603-112">automaticConfigurationScriptUrl</span></span>|<span data-ttu-id="cd603-113">String</span><span class="sxs-lookup"><span data-stu-id="cd603-113">String</span></span>|<span data-ttu-id="cd603-114">Url de secuencia de comandos de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="cd603-114">Proxy's automatic configuration script url.</span></span>|
|<span data-ttu-id="cd603-115">address</span><span class="sxs-lookup"><span data-stu-id="cd603-115">address</span></span>|<span data-ttu-id="cd603-116">String</span><span class="sxs-lookup"><span data-stu-id="cd603-116">String</span></span>|<span data-ttu-id="cd603-117">Dirección.</span><span class="sxs-lookup"><span data-stu-id="cd603-117">Address.</span></span>|
|<span data-ttu-id="cd603-118">port</span><span class="sxs-lookup"><span data-stu-id="cd603-118">port</span></span>|<span data-ttu-id="cd603-119">Int32</span><span class="sxs-lookup"><span data-stu-id="cd603-119">Int32</span></span>|<span data-ttu-id="cd603-120">Puerto.</span><span class="sxs-lookup"><span data-stu-id="cd603-120">Port.</span></span> <span data-ttu-id="cd603-121">Valores válidos de 0 a 65535</span><span class="sxs-lookup"><span data-stu-id="cd603-121">Valid values 0 to 65535</span></span>|

## <a name="relationships"></a><span data-ttu-id="cd603-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cd603-122">Relationships</span></span>
<span data-ttu-id="cd603-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cd603-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cd603-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd603-124">JSON Representation</span></span>
<span data-ttu-id="cd603-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cd603-125">Here is a JSON representation of the resource.</span></span>
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





