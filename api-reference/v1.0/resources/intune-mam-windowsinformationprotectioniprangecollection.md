---
title: Tipo de recurso windowsInformationProtectionIPRangeCollection
description: Colección de intervalos IP de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e9d23f8a6d771b116b35058c249866c70c7460d8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952660"
---
# <a name="windowsinformationprotectioniprangecollection-resource-type"></a><span data-ttu-id="4a21e-103">Tipo de recurso windowsInformationProtectionIPRangeCollection</span><span class="sxs-lookup"><span data-stu-id="4a21e-103">windowsInformationProtectionIPRangeCollection resource type</span></span>

> <span data-ttu-id="4a21e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4a21e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4a21e-105">Colección de intervalos IP de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="4a21e-105">Windows Information Protection IP Range Collection</span></span>
## <a name="properties"></a><span data-ttu-id="4a21e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a21e-106">Properties</span></span>
|<span data-ttu-id="4a21e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a21e-107">Property</span></span>|<span data-ttu-id="4a21e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a21e-108">Type</span></span>|<span data-ttu-id="4a21e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a21e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a21e-110">displayName</span><span class="sxs-lookup"><span data-stu-id="4a21e-110">displayName</span></span>|<span data-ttu-id="4a21e-111">cadena</span><span class="sxs-lookup"><span data-stu-id="4a21e-111">String</span></span>|<span data-ttu-id="4a21e-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="4a21e-112">Display name</span></span>|
|<span data-ttu-id="4a21e-113">rangos</span><span class="sxs-lookup"><span data-stu-id="4a21e-113">ranges</span></span>|<span data-ttu-id="4a21e-114">Colección [ipRange](../resources/intune-mam-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="4a21e-114">[ipRange](../resources/intune-mam-iprange.md) collection</span></span>|<span data-ttu-id="4a21e-115">Conjunto de intervalos IP</span><span class="sxs-lookup"><span data-stu-id="4a21e-115">Collection of ip ranges</span></span>|

## <a name="relationships"></a><span data-ttu-id="4a21e-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4a21e-116">Relationships</span></span>
<span data-ttu-id="4a21e-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4a21e-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4a21e-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a21e-118">JSON Representation</span></span>
<span data-ttu-id="4a21e-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4a21e-119">Here is a JSON representation of the resource.</span></span>
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



