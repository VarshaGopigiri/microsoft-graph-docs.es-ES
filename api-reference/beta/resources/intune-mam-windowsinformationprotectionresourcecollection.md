---
title: Tipo de recurso windowsInformationProtectionResourceCollection
description: Colección de recursos de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2a65704170c048f4aae66876f11ef8543c7b09e2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933011"
---
# <a name="windowsinformationprotectionresourcecollection-resource-type"></a><span data-ttu-id="315d6-103">Tipo de recurso windowsInformationProtectionResourceCollection</span><span class="sxs-lookup"><span data-stu-id="315d6-103">windowsInformationProtectionResourceCollection resource type</span></span>

> <span data-ttu-id="315d6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="315d6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="315d6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="315d6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="315d6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="315d6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="315d6-107">Colección de recursos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="315d6-107">Windows Information Protection Resource Collection</span></span>
## <a name="properties"></a><span data-ttu-id="315d6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="315d6-108">Properties</span></span>
|<span data-ttu-id="315d6-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="315d6-109">Property</span></span>|<span data-ttu-id="315d6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="315d6-110">Type</span></span>|<span data-ttu-id="315d6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="315d6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="315d6-112">displayName</span><span class="sxs-lookup"><span data-stu-id="315d6-112">displayName</span></span>|<span data-ttu-id="315d6-113">cadena</span><span class="sxs-lookup"><span data-stu-id="315d6-113">String</span></span>|<span data-ttu-id="315d6-114">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="315d6-114">Display name</span></span>|
|<span data-ttu-id="315d6-115">resources</span><span class="sxs-lookup"><span data-stu-id="315d6-115">resources</span></span>|<span data-ttu-id="315d6-116">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="315d6-116">String collection</span></span>|<span data-ttu-id="315d6-117">Colección de recursos</span><span class="sxs-lookup"><span data-stu-id="315d6-117">Collection of resources</span></span>|

## <a name="relationships"></a><span data-ttu-id="315d6-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="315d6-118">Relationships</span></span>
<span data-ttu-id="315d6-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="315d6-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="315d6-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="315d6-120">JSON Representation</span></span>
<span data-ttu-id="315d6-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="315d6-121">Here is a JSON representation of the resource.</span></span>
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





