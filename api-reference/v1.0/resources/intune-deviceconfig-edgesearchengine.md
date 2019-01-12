---
title: Tipo de recurso edgeSearchEngine
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 87a072ca6fb325f599c51a219bfa0e9d2ad0ac0d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935622"
---
# <a name="edgesearchengine-resource-type"></a><span data-ttu-id="ed067-103">Tipo de recurso edgeSearchEngine</span><span class="sxs-lookup"><span data-stu-id="ed067-103">edgeSearchEngine resource type</span></span>

> <span data-ttu-id="ed067-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed067-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed067-105">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="ed067-105">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="ed067-106">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="ed067-106">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ed067-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed067-107">Properties</span></span>
|<span data-ttu-id="ed067-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed067-108">Property</span></span>|<span data-ttu-id="ed067-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed067-109">Type</span></span>|<span data-ttu-id="ed067-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed067-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed067-111">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="ed067-111">edgeSearchEngineType</span></span>|[<span data-ttu-id="ed067-112">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="ed067-112">edgeSearchEngineType</span></span>](../resources/intune-deviceconfig-edgesearchenginetype.md)|<span data-ttu-id="ed067-113">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="ed067-113">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="ed067-114">Los valores posibles son: `default` y `bing`.</span><span class="sxs-lookup"><span data-stu-id="ed067-114">Possible values are: `default`, `bing`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ed067-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ed067-115">Relationships</span></span>
<span data-ttu-id="ed067-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ed067-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ed067-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ed067-117">JSON Representation</span></span>
<span data-ttu-id="ed067-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ed067-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.edgeSearchEngine"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngine",
  "edgeSearchEngineType": "String"
}
```



