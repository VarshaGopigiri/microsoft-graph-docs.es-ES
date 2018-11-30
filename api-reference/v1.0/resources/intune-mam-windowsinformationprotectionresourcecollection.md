---
title: Tipo de recurso windowsInformationProtectionResourceCollection
description: Colección de recursos de Windows Information Protection
ms.openlocfilehash: fd350f85acb962267f92352e6298dc50c44949ed
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030262"
---
# <a name="windowsinformationprotectionresourcecollection-resource-type"></a><span data-ttu-id="7686f-103">Tipo de recurso windowsInformationProtectionResourceCollection</span><span class="sxs-lookup"><span data-stu-id="7686f-103">windowsInformationProtectionResourceCollection resource type</span></span>

> <span data-ttu-id="7686f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7686f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7686f-105">Colección de recursos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="7686f-105">Windows Information Protection Resource Collection</span></span>
## <a name="properties"></a><span data-ttu-id="7686f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7686f-106">Properties</span></span>
|<span data-ttu-id="7686f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7686f-107">Property</span></span>|<span data-ttu-id="7686f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7686f-108">Type</span></span>|<span data-ttu-id="7686f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7686f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7686f-110">displayName</span><span class="sxs-lookup"><span data-stu-id="7686f-110">displayName</span></span>|<span data-ttu-id="7686f-111">cadena</span><span class="sxs-lookup"><span data-stu-id="7686f-111">String</span></span>|<span data-ttu-id="7686f-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="7686f-112">Display name</span></span>|
|<span data-ttu-id="7686f-113">resources</span><span class="sxs-lookup"><span data-stu-id="7686f-113">resources</span></span>|<span data-ttu-id="7686f-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="7686f-114">String collection</span></span>|<span data-ttu-id="7686f-115">Colección de recursos</span><span class="sxs-lookup"><span data-stu-id="7686f-115">Collection of resources</span></span>|

## <a name="relationships"></a><span data-ttu-id="7686f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7686f-116">Relationships</span></span>
<span data-ttu-id="7686f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7686f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7686f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7686f-118">JSON Representation</span></span>
<span data-ttu-id="7686f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7686f-119">Here is a JSON representation of the resource.</span></span>
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



