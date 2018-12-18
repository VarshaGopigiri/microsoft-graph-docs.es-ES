---
title: Tipo de recurso edgeSearchEngine
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.
author: tfitzmac
ms.openlocfilehash: 0c49780ddd7d2174116f7a0821fa98681d3e5d2a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339735"
---
# <a name="edgesearchengine-resource-type"></a><span data-ttu-id="e7a42-103">Tipo de recurso edgeSearchEngine</span><span class="sxs-lookup"><span data-stu-id="e7a42-103">edgeSearchEngine resource type</span></span>

> <span data-ttu-id="e7a42-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7a42-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7a42-105">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="e7a42-105">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="e7a42-106">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="e7a42-106">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e7a42-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7a42-107">Properties</span></span>
|<span data-ttu-id="e7a42-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7a42-108">Property</span></span>|<span data-ttu-id="e7a42-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7a42-109">Type</span></span>|<span data-ttu-id="e7a42-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7a42-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7a42-111">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="e7a42-111">edgeSearchEngineType</span></span>|[<span data-ttu-id="e7a42-112">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="e7a42-112">edgeSearchEngineType</span></span>](../resources/intune-deviceconfig-edgesearchenginetype.md)|<span data-ttu-id="e7a42-113">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="e7a42-113">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="e7a42-114">Los valores posibles son: `default` y `bing`.</span><span class="sxs-lookup"><span data-stu-id="e7a42-114">Possible values are: `default`, `bing`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e7a42-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7a42-115">Relationships</span></span>
<span data-ttu-id="e7a42-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e7a42-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e7a42-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7a42-117">JSON Representation</span></span>
<span data-ttu-id="e7a42-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7a42-118">Here is a JSON representation of the resource.</span></span>
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



