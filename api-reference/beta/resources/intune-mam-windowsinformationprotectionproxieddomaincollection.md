---
title: Tipo de recurso windowsInformationProtectionProxiedDomainCollection
description: Colección de dominios con proxy de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a2f4b1e29afd113c2e06b611fabd525f9f5a6ba1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916905"
---
# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a><span data-ttu-id="e7dc7-103">Tipo de recurso windowsInformationProtectionProxiedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="e7dc7-103">windowsInformationProtectionProxiedDomainCollection resource type</span></span>

> <span data-ttu-id="e7dc7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7dc7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7dc7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7dc7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e7dc7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7dc7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7dc7-107">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="e7dc7-107">Windows Information Protection Proxied Domain Collection</span></span>
## <a name="properties"></a><span data-ttu-id="e7dc7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7dc7-108">Properties</span></span>
|<span data-ttu-id="e7dc7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7dc7-109">Property</span></span>|<span data-ttu-id="e7dc7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7dc7-110">Type</span></span>|<span data-ttu-id="e7dc7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7dc7-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7dc7-112">displayName</span><span class="sxs-lookup"><span data-stu-id="e7dc7-112">displayName</span></span>|<span data-ttu-id="e7dc7-113">cadena</span><span class="sxs-lookup"><span data-stu-id="e7dc7-113">String</span></span>|<span data-ttu-id="e7dc7-114">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="e7dc7-114">Display name</span></span>|
|<span data-ttu-id="e7dc7-115">proxiedDomains</span><span class="sxs-lookup"><span data-stu-id="e7dc7-115">proxiedDomains</span></span>|<span data-ttu-id="e7dc7-116">Colección [proxiedDomain](../resources/intune-shared-proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="e7dc7-116">[proxiedDomain](../resources/intune-shared-proxieddomain.md) collection</span></span>|<span data-ttu-id="e7dc7-117">Conjunto de dominios con proxy</span><span class="sxs-lookup"><span data-stu-id="e7dc7-117">Collection of proxied domains</span></span>|

## <a name="relationships"></a><span data-ttu-id="e7dc7-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7dc7-118">Relationships</span></span>
<span data-ttu-id="e7dc7-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e7dc7-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e7dc7-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7dc7-120">JSON Representation</span></span>
<span data-ttu-id="e7dc7-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7dc7-121">Here is a JSON representation of the resource.</span></span>
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





