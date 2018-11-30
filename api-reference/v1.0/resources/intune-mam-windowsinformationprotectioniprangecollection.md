---
title: Tipo de recurso windowsInformationProtectionIPRangeCollection
description: Colección de intervalos IP de Windows Information Protection
ms.openlocfilehash: 41558014ec3d48af06788e15fc40786fe7f9aea4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029686"
---
# <a name="windowsinformationprotectioniprangecollection-resource-type"></a><span data-ttu-id="6fff3-103">Tipo de recurso windowsInformationProtectionIPRangeCollection</span><span class="sxs-lookup"><span data-stu-id="6fff3-103">windowsInformationProtectionIPRangeCollection resource type</span></span>

> <span data-ttu-id="6fff3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6fff3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6fff3-105">Colección de intervalos IP de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="6fff3-105">Windows Information Protection IP Range Collection</span></span>
## <a name="properties"></a><span data-ttu-id="6fff3-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fff3-106">Properties</span></span>
|<span data-ttu-id="6fff3-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6fff3-107">Property</span></span>|<span data-ttu-id="6fff3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fff3-108">Type</span></span>|<span data-ttu-id="6fff3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fff3-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6fff3-110">displayName</span><span class="sxs-lookup"><span data-stu-id="6fff3-110">displayName</span></span>|<span data-ttu-id="6fff3-111">cadena</span><span class="sxs-lookup"><span data-stu-id="6fff3-111">String</span></span>|<span data-ttu-id="6fff3-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="6fff3-112">Display name</span></span>|
|<span data-ttu-id="6fff3-113">rangos</span><span class="sxs-lookup"><span data-stu-id="6fff3-113">ranges</span></span>|<span data-ttu-id="6fff3-114">Colección [ipRange](../resources/intune-mam-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="6fff3-114">[ipRange](../resources/intune-mam-iprange.md) collection</span></span>|<span data-ttu-id="6fff3-115">Conjunto de intervalos IP</span><span class="sxs-lookup"><span data-stu-id="6fff3-115">Collection of ip ranges</span></span>|

## <a name="relationships"></a><span data-ttu-id="6fff3-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6fff3-116">Relationships</span></span>
<span data-ttu-id="6fff3-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6fff3-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6fff3-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6fff3-118">JSON Representation</span></span>
<span data-ttu-id="6fff3-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6fff3-119">Here is a JSON representation of the resource.</span></span>
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



