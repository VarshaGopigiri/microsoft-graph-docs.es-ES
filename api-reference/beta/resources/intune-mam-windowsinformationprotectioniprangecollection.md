---
title: Tipo de recurso windowsInformationProtectionIPRangeCollection
description: Colección de intervalos IP de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9981b585818bb6db712b0088b2fde275179917ef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911829"
---
# <a name="windowsinformationprotectioniprangecollection-resource-type"></a><span data-ttu-id="0e194-103">Tipo de recurso windowsInformationProtectionIPRangeCollection</span><span class="sxs-lookup"><span data-stu-id="0e194-103">windowsInformationProtectionIPRangeCollection resource type</span></span>

> <span data-ttu-id="0e194-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0e194-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0e194-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0e194-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0e194-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e194-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e194-107">Colección de intervalos IP de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="0e194-107">Windows Information Protection IP Range Collection</span></span>
## <a name="properties"></a><span data-ttu-id="0e194-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e194-108">Properties</span></span>
|<span data-ttu-id="0e194-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e194-109">Property</span></span>|<span data-ttu-id="0e194-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e194-110">Type</span></span>|<span data-ttu-id="0e194-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e194-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e194-112">displayName</span><span class="sxs-lookup"><span data-stu-id="0e194-112">displayName</span></span>|<span data-ttu-id="0e194-113">cadena</span><span class="sxs-lookup"><span data-stu-id="0e194-113">String</span></span>|<span data-ttu-id="0e194-114">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="0e194-114">Display name</span></span>|
|<span data-ttu-id="0e194-115">rangos</span><span class="sxs-lookup"><span data-stu-id="0e194-115">ranges</span></span>|<span data-ttu-id="0e194-116">Colección [ipRange](../resources/intune-shared-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="0e194-116">[ipRange](../resources/intune-shared-iprange.md) collection</span></span>|<span data-ttu-id="0e194-117">Conjunto de intervalos IP</span><span class="sxs-lookup"><span data-stu-id="0e194-117">Collection of ip ranges</span></span>|

## <a name="relationships"></a><span data-ttu-id="0e194-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0e194-118">Relationships</span></span>
<span data-ttu-id="0e194-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0e194-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0e194-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0e194-120">JSON Representation</span></span>
<span data-ttu-id="0e194-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0e194-121">Here is a JSON representation of the resource.</span></span>
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
      "@odata.type": "microsoft.graph.iPv6Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ]
}
```





