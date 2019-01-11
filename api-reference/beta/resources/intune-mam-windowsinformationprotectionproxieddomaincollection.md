---
title: Tipo de recurso windowsInformationProtectionProxiedDomainCollection
description: Colección de dominios con proxy de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: df71cd36a84a0b0782b645cf56df708d1f30e365
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855128"
---
# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a><span data-ttu-id="f116f-103">Tipo de recurso windowsInformationProtectionProxiedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="f116f-103">windowsInformationProtectionProxiedDomainCollection resource type</span></span>

> <span data-ttu-id="f116f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f116f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f116f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f116f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f116f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f116f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f116f-107">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="f116f-107">Windows Information Protection Proxied Domain Collection</span></span>
## <a name="properties"></a><span data-ttu-id="f116f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f116f-108">Properties</span></span>
|<span data-ttu-id="f116f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f116f-109">Property</span></span>|<span data-ttu-id="f116f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f116f-110">Type</span></span>|<span data-ttu-id="f116f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f116f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f116f-112">displayName</span><span class="sxs-lookup"><span data-stu-id="f116f-112">displayName</span></span>|<span data-ttu-id="f116f-113">cadena</span><span class="sxs-lookup"><span data-stu-id="f116f-113">String</span></span>|<span data-ttu-id="f116f-114">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="f116f-114">Display name</span></span>|
|<span data-ttu-id="f116f-115">proxiedDomains</span><span class="sxs-lookup"><span data-stu-id="f116f-115">proxiedDomains</span></span>|<span data-ttu-id="f116f-116">Colección [proxiedDomain](../resources/intune-shared-proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="f116f-116">[proxiedDomain](../resources/intune-shared-proxieddomain.md) collection</span></span>|<span data-ttu-id="f116f-117">Conjunto de dominios con proxy</span><span class="sxs-lookup"><span data-stu-id="f116f-117">Collection of proxied domains</span></span>|

## <a name="relationships"></a><span data-ttu-id="f116f-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f116f-118">Relationships</span></span>
<span data-ttu-id="f116f-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f116f-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f116f-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f116f-120">JSON Representation</span></span>
<span data-ttu-id="f116f-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f116f-121">Here is a JSON representation of the resource.</span></span>
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





