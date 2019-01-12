---
title: Tipo de recurso windowsInformationProtectionResourceCollection
description: Colección de recursos de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a913f90c2fed24a524e07b8dca1b629ebd9795f6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981220"
---
# <a name="windowsinformationprotectionresourcecollection-resource-type"></a><span data-ttu-id="f240d-103">Tipo de recurso windowsInformationProtectionResourceCollection</span><span class="sxs-lookup"><span data-stu-id="f240d-103">windowsInformationProtectionResourceCollection resource type</span></span>

> <span data-ttu-id="f240d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f240d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f240d-105">Colección de recursos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="f240d-105">Windows Information Protection Resource Collection</span></span>
## <a name="properties"></a><span data-ttu-id="f240d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f240d-106">Properties</span></span>
|<span data-ttu-id="f240d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f240d-107">Property</span></span>|<span data-ttu-id="f240d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f240d-108">Type</span></span>|<span data-ttu-id="f240d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f240d-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f240d-110">displayName</span><span class="sxs-lookup"><span data-stu-id="f240d-110">displayName</span></span>|<span data-ttu-id="f240d-111">cadena</span><span class="sxs-lookup"><span data-stu-id="f240d-111">String</span></span>|<span data-ttu-id="f240d-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="f240d-112">Display name</span></span>|
|<span data-ttu-id="f240d-113">resources</span><span class="sxs-lookup"><span data-stu-id="f240d-113">resources</span></span>|<span data-ttu-id="f240d-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="f240d-114">String collection</span></span>|<span data-ttu-id="f240d-115">Colección de recursos</span><span class="sxs-lookup"><span data-stu-id="f240d-115">Collection of resources</span></span>|

## <a name="relationships"></a><span data-ttu-id="f240d-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f240d-116">Relationships</span></span>
<span data-ttu-id="f240d-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f240d-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f240d-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f240d-118">JSON Representation</span></span>
<span data-ttu-id="f240d-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f240d-119">Here is a JSON representation of the resource.</span></span>
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



