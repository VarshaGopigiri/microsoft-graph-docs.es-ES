---
title: Tipo de recurso edgeSearchEngine
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7a58cbed251773559beb2589893ab9759d4758fa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819911"
---
# <a name="edgesearchengine-resource-type"></a><span data-ttu-id="855a1-103">Tipo de recurso edgeSearchEngine</span><span class="sxs-lookup"><span data-stu-id="855a1-103">edgeSearchEngine resource type</span></span>

> <span data-ttu-id="855a1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="855a1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="855a1-105">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="855a1-105">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="855a1-106">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="855a1-106">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="855a1-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="855a1-107">Properties</span></span>
|<span data-ttu-id="855a1-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="855a1-108">Property</span></span>|<span data-ttu-id="855a1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="855a1-109">Type</span></span>|<span data-ttu-id="855a1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="855a1-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="855a1-111">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="855a1-111">edgeSearchEngineType</span></span>|[<span data-ttu-id="855a1-112">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="855a1-112">edgeSearchEngineType</span></span>](../resources/intune-deviceconfig-edgesearchenginetype.md)|<span data-ttu-id="855a1-113">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="855a1-113">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="855a1-114">Los valores posibles son: `default` y `bing`.</span><span class="sxs-lookup"><span data-stu-id="855a1-114">Possible values are: `default`, `bing`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="855a1-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="855a1-115">Relationships</span></span>
<span data-ttu-id="855a1-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="855a1-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="855a1-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="855a1-117">JSON Representation</span></span>
<span data-ttu-id="855a1-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="855a1-118">Here is a JSON representation of the resource.</span></span>
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



