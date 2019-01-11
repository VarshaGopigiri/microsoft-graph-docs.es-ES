---
title: Tipo de recurso edgeSearchEngine
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 08434805545de7814765f62e73898db7455b79ee
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889267"
---
# <a name="edgesearchengine-resource-type"></a><span data-ttu-id="10bce-103">Tipo de recurso edgeSearchEngine</span><span class="sxs-lookup"><span data-stu-id="10bce-103">edgeSearchEngine resource type</span></span>

> <span data-ttu-id="10bce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="10bce-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="10bce-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="10bce-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="10bce-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="10bce-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="10bce-107">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="10bce-107">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="10bce-108">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="10bce-108">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="10bce-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10bce-109">Properties</span></span>
|<span data-ttu-id="10bce-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10bce-110">Property</span></span>|<span data-ttu-id="10bce-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="10bce-111">Type</span></span>|<span data-ttu-id="10bce-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="10bce-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="10bce-113">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="10bce-113">edgeSearchEngineType</span></span>|[<span data-ttu-id="10bce-114">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="10bce-114">edgeSearchEngineType</span></span>](../resources/intune-deviceconfig-edgesearchenginetype.md)|<span data-ttu-id="10bce-115">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="10bce-115">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="10bce-116">Los valores posibles son: `default` y `bing`.</span><span class="sxs-lookup"><span data-stu-id="10bce-116">Possible values are: `default`, `bing`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="10bce-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="10bce-117">Relationships</span></span>
<span data-ttu-id="10bce-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="10bce-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="10bce-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="10bce-119">JSON Representation</span></span>
<span data-ttu-id="10bce-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="10bce-120">Here is a JSON representation of the resource.</span></span>
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





