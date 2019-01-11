---
title: Tipo de recurso windowsInformationProtectionResourceCollection
description: Colección de recursos de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0df0ebc3c67e7cf9bc18240f75d620442f80e0d6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844355"
---
# <a name="windowsinformationprotectionresourcecollection-resource-type"></a><span data-ttu-id="15949-103">Tipo de recurso windowsInformationProtectionResourceCollection</span><span class="sxs-lookup"><span data-stu-id="15949-103">windowsInformationProtectionResourceCollection resource type</span></span>

> <span data-ttu-id="15949-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="15949-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="15949-105">Colección de recursos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="15949-105">Windows Information Protection Resource Collection</span></span>
## <a name="properties"></a><span data-ttu-id="15949-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15949-106">Properties</span></span>
|<span data-ttu-id="15949-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15949-107">Property</span></span>|<span data-ttu-id="15949-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="15949-108">Type</span></span>|<span data-ttu-id="15949-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="15949-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="15949-110">displayName</span><span class="sxs-lookup"><span data-stu-id="15949-110">displayName</span></span>|<span data-ttu-id="15949-111">cadena</span><span class="sxs-lookup"><span data-stu-id="15949-111">String</span></span>|<span data-ttu-id="15949-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="15949-112">Display name</span></span>|
|<span data-ttu-id="15949-113">resources</span><span class="sxs-lookup"><span data-stu-id="15949-113">resources</span></span>|<span data-ttu-id="15949-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="15949-114">String collection</span></span>|<span data-ttu-id="15949-115">Colección de recursos</span><span class="sxs-lookup"><span data-stu-id="15949-115">Collection of resources</span></span>|

## <a name="relationships"></a><span data-ttu-id="15949-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="15949-116">Relationships</span></span>
<span data-ttu-id="15949-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="15949-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="15949-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="15949-118">JSON Representation</span></span>
<span data-ttu-id="15949-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="15949-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionResourceCollection",
  "displayName": "String",
  "resources": [
    "String"
  ]
}
```



