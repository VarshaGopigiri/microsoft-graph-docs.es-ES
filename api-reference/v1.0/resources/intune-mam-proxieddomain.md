---
title: Tipo de recurso proxiedDomain
description: Dominio con proxy
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: eff345414531b0ddda1600bb567aacd4a5436602
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871116"
---
# <a name="proxieddomain-resource-type"></a><span data-ttu-id="84d63-103">Tipo de recurso proxiedDomain</span><span class="sxs-lookup"><span data-stu-id="84d63-103">proxiedDomain resource type</span></span>

> <span data-ttu-id="84d63-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84d63-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84d63-105">Dominio con proxy</span><span class="sxs-lookup"><span data-stu-id="84d63-105">Proxied Domain</span></span>
## <a name="properties"></a><span data-ttu-id="84d63-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84d63-106">Properties</span></span>
|<span data-ttu-id="84d63-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84d63-107">Property</span></span>|<span data-ttu-id="84d63-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="84d63-108">Type</span></span>|<span data-ttu-id="84d63-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="84d63-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84d63-110">ipAddressOrFQDN</span><span class="sxs-lookup"><span data-stu-id="84d63-110">ipAddressOrFQDN</span></span>|<span data-ttu-id="84d63-111">cadena</span><span class="sxs-lookup"><span data-stu-id="84d63-111">String</span></span>|<span data-ttu-id="84d63-112">La dirección IP o FQDN</span><span class="sxs-lookup"><span data-stu-id="84d63-112">The IP address or FQDN</span></span>|
|<span data-ttu-id="84d63-113">proxy</span><span class="sxs-lookup"><span data-stu-id="84d63-113">proxy</span></span>|<span data-ttu-id="84d63-114">cadena</span><span class="sxs-lookup"><span data-stu-id="84d63-114">String</span></span>|<span data-ttu-id="84d63-115">IP de proxy</span><span class="sxs-lookup"><span data-stu-id="84d63-115">Proxy IP</span></span>|

## <a name="relationships"></a><span data-ttu-id="84d63-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="84d63-116">Relationships</span></span>
<span data-ttu-id="84d63-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="84d63-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="84d63-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="84d63-118">JSON Representation</span></span>
<span data-ttu-id="84d63-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="84d63-119">Here is a JSON representation of the resource.</span></span>
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



