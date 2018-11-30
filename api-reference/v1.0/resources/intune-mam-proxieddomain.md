---
title: Tipo de recurso proxiedDomain
description: Dominio con proxy
ms.openlocfilehash: d73ed20341a7de025f6f2d39536a1e791b978f55
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031139"
---
# <a name="proxieddomain-resource-type"></a><span data-ttu-id="4a06f-103">Tipo de recurso proxiedDomain</span><span class="sxs-lookup"><span data-stu-id="4a06f-103">proxiedDomain resource type</span></span>

> <span data-ttu-id="4a06f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4a06f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4a06f-105">Dominio con proxy</span><span class="sxs-lookup"><span data-stu-id="4a06f-105">Proxied Domain</span></span>
## <a name="properties"></a><span data-ttu-id="4a06f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a06f-106">Properties</span></span>
|<span data-ttu-id="4a06f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a06f-107">Property</span></span>|<span data-ttu-id="4a06f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a06f-108">Type</span></span>|<span data-ttu-id="4a06f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a06f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a06f-110">ipAddressOrFQDN</span><span class="sxs-lookup"><span data-stu-id="4a06f-110">ipAddressOrFQDN</span></span>|<span data-ttu-id="4a06f-111">cadena</span><span class="sxs-lookup"><span data-stu-id="4a06f-111">String</span></span>|<span data-ttu-id="4a06f-112">La dirección IP o FQDN</span><span class="sxs-lookup"><span data-stu-id="4a06f-112">The IP address or FQDN</span></span>|
|<span data-ttu-id="4a06f-113">proxy</span><span class="sxs-lookup"><span data-stu-id="4a06f-113">proxy</span></span>|<span data-ttu-id="4a06f-114">cadena</span><span class="sxs-lookup"><span data-stu-id="4a06f-114">String</span></span>|<span data-ttu-id="4a06f-115">IP de proxy</span><span class="sxs-lookup"><span data-stu-id="4a06f-115">Proxy IP</span></span>|

## <a name="relationships"></a><span data-ttu-id="4a06f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4a06f-116">Relationships</span></span>
<span data-ttu-id="4a06f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4a06f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4a06f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a06f-118">JSON Representation</span></span>
<span data-ttu-id="4a06f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4a06f-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.proxiedDomain"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.proxiedDomain",
  "ipAddressOrFQDN": "String",
  "proxy": "String"
}
```



