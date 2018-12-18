---
title: Tipo de recurso windowsInformationProtectionIPRangeCollection
description: Colección de intervalos IP de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: 12030ab0b71448c644e4e664f9095dea3e48a26c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319757"
---
# <a name="windowsinformationprotectioniprangecollection-resource-type"></a><span data-ttu-id="5f000-103">Tipo de recurso windowsInformationProtectionIPRangeCollection</span><span class="sxs-lookup"><span data-stu-id="5f000-103">windowsInformationProtectionIPRangeCollection resource type</span></span>

> <span data-ttu-id="5f000-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5f000-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f000-105">Colección de intervalos IP de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="5f000-105">Windows Information Protection IP Range Collection</span></span>
## <a name="properties"></a><span data-ttu-id="5f000-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f000-106">Properties</span></span>
|<span data-ttu-id="5f000-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f000-107">Property</span></span>|<span data-ttu-id="5f000-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f000-108">Type</span></span>|<span data-ttu-id="5f000-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f000-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f000-110">displayName</span><span class="sxs-lookup"><span data-stu-id="5f000-110">displayName</span></span>|<span data-ttu-id="5f000-111">cadena</span><span class="sxs-lookup"><span data-stu-id="5f000-111">String</span></span>|<span data-ttu-id="5f000-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="5f000-112">Display name</span></span>|
|<span data-ttu-id="5f000-113">rangos</span><span class="sxs-lookup"><span data-stu-id="5f000-113">ranges</span></span>|<span data-ttu-id="5f000-114">Colección [ipRange](../resources/intune-mam-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="5f000-114">[ipRange](../resources/intune-mam-iprange.md) collection</span></span>|<span data-ttu-id="5f000-115">Conjunto de intervalos IP</span><span class="sxs-lookup"><span data-stu-id="5f000-115">Collection of ip ranges</span></span>|

## <a name="relationships"></a><span data-ttu-id="5f000-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5f000-116">Relationships</span></span>
<span data-ttu-id="5f000-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5f000-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5f000-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5f000-118">JSON Representation</span></span>
<span data-ttu-id="5f000-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5f000-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionIPRangeCollection",
  "displayName": "String",
  "ranges": [
    {
      "@odata.type": "microsoft.graph.ipRange",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ]
}
```



