---
title: Tipo de recurso windowsInformationProtectionProxiedDomainCollection
description: Colección de dominios con proxy de Windows Information Protection
ms.openlocfilehash: b19709bff695d9184cda5adbffd9e0591e46db2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031905"
---
# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a><span data-ttu-id="585de-103">Tipo de recurso windowsInformationProtectionProxiedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="585de-103">windowsInformationProtectionProxiedDomainCollection resource type</span></span>

> <span data-ttu-id="585de-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="585de-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="585de-105">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="585de-105">Windows Information Protection Proxied Domain Collection</span></span>
## <a name="properties"></a><span data-ttu-id="585de-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="585de-106">Properties</span></span>
|<span data-ttu-id="585de-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="585de-107">Property</span></span>|<span data-ttu-id="585de-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="585de-108">Type</span></span>|<span data-ttu-id="585de-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="585de-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="585de-110">displayName</span><span class="sxs-lookup"><span data-stu-id="585de-110">displayName</span></span>|<span data-ttu-id="585de-111">cadena</span><span class="sxs-lookup"><span data-stu-id="585de-111">String</span></span>|<span data-ttu-id="585de-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="585de-112">Display name</span></span>|
|<span data-ttu-id="585de-113">proxiedDomains</span><span class="sxs-lookup"><span data-stu-id="585de-113">proxiedDomains</span></span>|<span data-ttu-id="585de-114">Colección [proxiedDomain](../resources/intune-mam-proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="585de-114">[proxiedDomain](../resources/intune-mam-proxieddomain.md) collection</span></span>|<span data-ttu-id="585de-115">Conjunto de dominios con proxy</span><span class="sxs-lookup"><span data-stu-id="585de-115">Collection of proxied domains</span></span>|

## <a name="relationships"></a><span data-ttu-id="585de-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="585de-116">Relationships</span></span>
<span data-ttu-id="585de-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="585de-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="585de-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="585de-118">JSON Representation</span></span>
<span data-ttu-id="585de-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="585de-119">Here is a JSON representation of the resource.</span></span>
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



