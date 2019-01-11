---
title: Tipo de recurso windowsInformationProtectionProxiedDomainCollection
description: Colección de dominios con proxy de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dfc07b47115e4e5ce4be959ac7867a2963021abf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822102"
---
# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a><span data-ttu-id="5858c-103">Tipo de recurso windowsInformationProtectionProxiedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="5858c-103">windowsInformationProtectionProxiedDomainCollection resource type</span></span>

> <span data-ttu-id="5858c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5858c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5858c-105">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="5858c-105">Windows Information Protection Proxied Domain Collection</span></span>
## <a name="properties"></a><span data-ttu-id="5858c-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5858c-106">Properties</span></span>
|<span data-ttu-id="5858c-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5858c-107">Property</span></span>|<span data-ttu-id="5858c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5858c-108">Type</span></span>|<span data-ttu-id="5858c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5858c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5858c-110">displayName</span><span class="sxs-lookup"><span data-stu-id="5858c-110">displayName</span></span>|<span data-ttu-id="5858c-111">cadena</span><span class="sxs-lookup"><span data-stu-id="5858c-111">String</span></span>|<span data-ttu-id="5858c-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="5858c-112">Display name</span></span>|
|<span data-ttu-id="5858c-113">proxiedDomains</span><span class="sxs-lookup"><span data-stu-id="5858c-113">proxiedDomains</span></span>|<span data-ttu-id="5858c-114">Colección [proxiedDomain](../resources/intune-mam-proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="5858c-114">[proxiedDomain](../resources/intune-mam-proxieddomain.md) collection</span></span>|<span data-ttu-id="5858c-115">Conjunto de dominios con proxy</span><span class="sxs-lookup"><span data-stu-id="5858c-115">Collection of proxied domains</span></span>|

## <a name="relationships"></a><span data-ttu-id="5858c-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5858c-116">Relationships</span></span>
<span data-ttu-id="5858c-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5858c-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5858c-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5858c-118">JSON Representation</span></span>
<span data-ttu-id="5858c-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5858c-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
  "displayName": "String",
  "proxiedDomains": [
    {
      "@odata.type": "microsoft.graph.proxiedDomain",
      "ipAddressOrFQDN": "String",
      "proxy": "String"
    }
  ]
}
```



