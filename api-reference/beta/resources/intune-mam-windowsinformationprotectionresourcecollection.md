---
title: Tipo de recurso windowsInformationProtectionResourceCollection
description: Colección de recursos de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: 96b3b36f40d1eeb88731f6f44ebec812a18fe713
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306891"
---
# <a name="windowsinformationprotectionresourcecollection-resource-type"></a><span data-ttu-id="f3716-103">Tipo de recurso windowsInformationProtectionResourceCollection</span><span class="sxs-lookup"><span data-stu-id="f3716-103">windowsInformationProtectionResourceCollection resource type</span></span>

> <span data-ttu-id="f3716-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3716-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3716-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3716-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f3716-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f3716-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f3716-107">Colección de recursos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="f3716-107">Windows Information Protection Resource Collection</span></span>
## <a name="properties"></a><span data-ttu-id="f3716-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3716-108">Properties</span></span>
|<span data-ttu-id="f3716-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3716-109">Property</span></span>|<span data-ttu-id="f3716-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3716-110">Type</span></span>|<span data-ttu-id="f3716-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3716-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f3716-112">displayName</span><span class="sxs-lookup"><span data-stu-id="f3716-112">displayName</span></span>|<span data-ttu-id="f3716-113">cadena</span><span class="sxs-lookup"><span data-stu-id="f3716-113">String</span></span>|<span data-ttu-id="f3716-114">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="f3716-114">Display name</span></span>|
|<span data-ttu-id="f3716-115">resources</span><span class="sxs-lookup"><span data-stu-id="f3716-115">resources</span></span>|<span data-ttu-id="f3716-116">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="f3716-116">String collection</span></span>|<span data-ttu-id="f3716-117">Colección de recursos</span><span class="sxs-lookup"><span data-stu-id="f3716-117">Collection of resources</span></span>|

## <a name="relationships"></a><span data-ttu-id="f3716-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f3716-118">Relationships</span></span>
<span data-ttu-id="f3716-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f3716-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f3716-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f3716-120">JSON Representation</span></span>
<span data-ttu-id="f3716-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f3716-121">Here is a JSON representation of the resource.</span></span>
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





