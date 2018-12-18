---
title: Tipo de recurso windowsInformationProtectionProxiedDomainCollection
description: Colección de dominios con proxy de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: c95c54c5bbfcc1b5202a0c56a6e3932b35ffac88
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309474"
---
# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a><span data-ttu-id="7a1c2-103">Tipo de recurso windowsInformationProtectionProxiedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="7a1c2-103">windowsInformationProtectionProxiedDomainCollection resource type</span></span>

> <span data-ttu-id="7a1c2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a1c2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a1c2-105">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="7a1c2-105">Windows Information Protection Proxied Domain Collection</span></span>
## <a name="properties"></a><span data-ttu-id="7a1c2-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a1c2-106">Properties</span></span>
|<span data-ttu-id="7a1c2-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a1c2-107">Property</span></span>|<span data-ttu-id="7a1c2-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a1c2-108">Type</span></span>|<span data-ttu-id="7a1c2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a1c2-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a1c2-110">displayName</span><span class="sxs-lookup"><span data-stu-id="7a1c2-110">displayName</span></span>|<span data-ttu-id="7a1c2-111">cadena</span><span class="sxs-lookup"><span data-stu-id="7a1c2-111">String</span></span>|<span data-ttu-id="7a1c2-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="7a1c2-112">Display name</span></span>|
|<span data-ttu-id="7a1c2-113">proxiedDomains</span><span class="sxs-lookup"><span data-stu-id="7a1c2-113">proxiedDomains</span></span>|<span data-ttu-id="7a1c2-114">Colección [proxiedDomain](../resources/intune-mam-proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="7a1c2-114">[proxiedDomain](../resources/intune-mam-proxieddomain.md) collection</span></span>|<span data-ttu-id="7a1c2-115">Conjunto de dominios con proxy</span><span class="sxs-lookup"><span data-stu-id="7a1c2-115">Collection of proxied domains</span></span>|

## <a name="relationships"></a><span data-ttu-id="7a1c2-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7a1c2-116">Relationships</span></span>
<span data-ttu-id="7a1c2-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7a1c2-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7a1c2-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a1c2-118">JSON Representation</span></span>
<span data-ttu-id="7a1c2-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7a1c2-119">Here is a JSON representation of the resource.</span></span>
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



