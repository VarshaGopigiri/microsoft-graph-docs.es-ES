---
title: Tipo de recurso proxiedDomain
description: Dominio con proxy
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dc90ebd57752fedcaf7acf069da6e653da04978e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968550"
---
# <a name="proxieddomain-resource-type"></a><span data-ttu-id="d33d8-103">Tipo de recurso proxiedDomain</span><span class="sxs-lookup"><span data-stu-id="d33d8-103">proxiedDomain resource type</span></span>

> <span data-ttu-id="d33d8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d33d8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d33d8-105">Dominio con proxy</span><span class="sxs-lookup"><span data-stu-id="d33d8-105">Proxied Domain</span></span>
## <a name="properties"></a><span data-ttu-id="d33d8-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d33d8-106">Properties</span></span>
|<span data-ttu-id="d33d8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d33d8-107">Property</span></span>|<span data-ttu-id="d33d8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d33d8-108">Type</span></span>|<span data-ttu-id="d33d8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d33d8-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d33d8-110">ipAddressOrFQDN</span><span class="sxs-lookup"><span data-stu-id="d33d8-110">ipAddressOrFQDN</span></span>|<span data-ttu-id="d33d8-111">cadena</span><span class="sxs-lookup"><span data-stu-id="d33d8-111">String</span></span>|<span data-ttu-id="d33d8-112">La dirección IP o FQDN</span><span class="sxs-lookup"><span data-stu-id="d33d8-112">The IP address or FQDN</span></span>|
|<span data-ttu-id="d33d8-113">proxy</span><span class="sxs-lookup"><span data-stu-id="d33d8-113">proxy</span></span>|<span data-ttu-id="d33d8-114">cadena</span><span class="sxs-lookup"><span data-stu-id="d33d8-114">String</span></span>|<span data-ttu-id="d33d8-115">IP de proxy</span><span class="sxs-lookup"><span data-stu-id="d33d8-115">Proxy IP</span></span>|

## <a name="relationships"></a><span data-ttu-id="d33d8-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d33d8-116">Relationships</span></span>
<span data-ttu-id="d33d8-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d33d8-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d33d8-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d33d8-118">JSON Representation</span></span>
<span data-ttu-id="d33d8-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d33d8-119">Here is a JSON representation of the resource.</span></span>
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



