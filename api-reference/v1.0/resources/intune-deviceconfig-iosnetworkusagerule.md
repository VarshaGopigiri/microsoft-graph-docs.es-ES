---
title: Tipo de recurso iosNetworkUsageRule
description: Las reglas de uso de red permiten a las empresas especificar cómo las aplicaciones administradas usan las redes, como las redes de datos de telefonía móvil.
ms.openlocfilehash: 211cbc52f596bbe62647a14c84bd5fd5178fdfc6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032354"
---
# <a name="iosnetworkusagerule-resource-type"></a><span data-ttu-id="e9a75-103">Tipo de recurso iosNetworkUsageRule</span><span class="sxs-lookup"><span data-stu-id="e9a75-103">iosNetworkUsageRule resource type</span></span>

> <span data-ttu-id="e9a75-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9a75-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9a75-105">Las reglas de uso de red permiten a las empresas especificar cómo las aplicaciones administradas usan las redes, como las redes de datos de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="e9a75-105">Network Usage Rules allow enterprises to specify how managed apps use networks, such as cellular data networks.</span></span>
## <a name="properties"></a><span data-ttu-id="e9a75-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9a75-106">Properties</span></span>
|<span data-ttu-id="e9a75-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9a75-107">Property</span></span>|<span data-ttu-id="e9a75-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9a75-108">Type</span></span>|<span data-ttu-id="e9a75-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9a75-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e9a75-110">managedApps</span><span class="sxs-lookup"><span data-stu-id="e9a75-110">managedApps</span></span>|<span data-ttu-id="e9a75-111">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="e9a75-111">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="e9a75-112">Información sobre las aplicaciones administradas a las que se va a aplicar esta regla.</span><span class="sxs-lookup"><span data-stu-id="e9a75-112">Information about the managed apps that this rule is going to apply to.</span></span> <span data-ttu-id="e9a75-113">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="e9a75-113">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="e9a75-114">cellularDataBlockWhenRoaming</span><span class="sxs-lookup"><span data-stu-id="e9a75-114">cellularDataBlockWhenRoaming</span></span>|<span data-ttu-id="e9a75-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9a75-115">Boolean</span></span>|<span data-ttu-id="e9a75-116">Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="e9a75-116">If set to true, corresponding managed apps will not be allowed to use cellular data when roaming.</span></span>|
|<span data-ttu-id="e9a75-117">cellularDataBlocked</span><span class="sxs-lookup"><span data-stu-id="e9a75-117">cellularDataBlocked</span></span>|<span data-ttu-id="e9a75-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9a75-118">Boolean</span></span>|<span data-ttu-id="e9a75-119">Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en ningún momento.</span><span class="sxs-lookup"><span data-stu-id="e9a75-119">If set to true, corresponding managed apps will not be allowed to use cellular data at any time.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e9a75-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e9a75-120">Relationships</span></span>
<span data-ttu-id="e9a75-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e9a75-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e9a75-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e9a75-122">JSON Representation</span></span>
<span data-ttu-id="e9a75-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e9a75-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNetworkUsageRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNetworkUsageRule",
  "managedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "cellularDataBlockWhenRoaming": true,
  "cellularDataBlocked": true
}
```



