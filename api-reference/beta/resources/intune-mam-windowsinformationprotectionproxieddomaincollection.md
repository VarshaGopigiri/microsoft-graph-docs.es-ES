---
title: Tipo de recurso windowsInformationProtectionProxiedDomainCollection
description: Colección de dominios con proxy de Windows Information Protection
ms.openlocfilehash: 07539361d99211f2a787fe538745debf09fa4cf2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089101"
---
# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a><span data-ttu-id="11f9a-103">Tipo de recurso windowsInformationProtectionProxiedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="11f9a-103">windowsInformationProtectionProxiedDomainCollection resource type</span></span>

> <span data-ttu-id="11f9a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11f9a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11f9a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11f9a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="11f9a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11f9a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11f9a-107">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="11f9a-107">Windows Information Protection Proxied Domain Collection</span></span>
## <a name="properties"></a><span data-ttu-id="11f9a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11f9a-108">Properties</span></span>
|<span data-ttu-id="11f9a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11f9a-109">Property</span></span>|<span data-ttu-id="11f9a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="11f9a-110">Type</span></span>|<span data-ttu-id="11f9a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="11f9a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11f9a-112">displayName</span><span class="sxs-lookup"><span data-stu-id="11f9a-112">displayName</span></span>|<span data-ttu-id="11f9a-113">cadena</span><span class="sxs-lookup"><span data-stu-id="11f9a-113">String</span></span>|<span data-ttu-id="11f9a-114">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="11f9a-114">Display name</span></span>|
|<span data-ttu-id="11f9a-115">proxiedDomains</span><span class="sxs-lookup"><span data-stu-id="11f9a-115">proxiedDomains</span></span>|<span data-ttu-id="11f9a-116">Colección [proxiedDomain](../resources/intune-shared-proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="11f9a-116">[proxiedDomain](../resources/intune-shared-proxieddomain.md) collection</span></span>|<span data-ttu-id="11f9a-117">Conjunto de dominios con proxy</span><span class="sxs-lookup"><span data-stu-id="11f9a-117">Collection of proxied domains</span></span>|

## <a name="relationships"></a><span data-ttu-id="11f9a-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11f9a-118">Relationships</span></span>
<span data-ttu-id="11f9a-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11f9a-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="11f9a-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11f9a-120">JSON Representation</span></span>
<span data-ttu-id="11f9a-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11f9a-121">Here is a JSON representation of the resource.</span></span>
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





