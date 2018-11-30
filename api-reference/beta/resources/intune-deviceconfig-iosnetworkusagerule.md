---
title: Tipo de recurso iosNetworkUsageRule
description: Las reglas de uso de red permiten a las empresas especificar cómo las aplicaciones administradas usan las redes, como las redes de datos de telefonía móvil.
ms.openlocfilehash: 93cfd1f5eefe6f32fd0b112b24e3cdfba6969434
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087317"
---
# <a name="iosnetworkusagerule-resource-type"></a><span data-ttu-id="32f44-103">Tipo de recurso iosNetworkUsageRule</span><span class="sxs-lookup"><span data-stu-id="32f44-103">iosNetworkUsageRule resource type</span></span>

> <span data-ttu-id="32f44-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="32f44-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="32f44-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="32f44-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="32f44-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32f44-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32f44-107">Las reglas de uso de red permiten a las empresas especificar cómo las aplicaciones administradas usan las redes, como las redes de datos de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="32f44-107">Network Usage Rules allow enterprises to specify how managed apps use networks, such as cellular data networks.</span></span>
## <a name="properties"></a><span data-ttu-id="32f44-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32f44-108">Properties</span></span>
|<span data-ttu-id="32f44-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32f44-109">Property</span></span>|<span data-ttu-id="32f44-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="32f44-110">Type</span></span>|<span data-ttu-id="32f44-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="32f44-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="32f44-112">managedApps</span><span class="sxs-lookup"><span data-stu-id="32f44-112">managedApps</span></span>|<span data-ttu-id="32f44-113">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="32f44-113">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="32f44-114">Información sobre las aplicaciones administradas a las que se va a aplicar esta regla.</span><span class="sxs-lookup"><span data-stu-id="32f44-114">Information about the managed apps that this rule is going to apply to.</span></span> <span data-ttu-id="32f44-115">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="32f44-115">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="32f44-116">cellularDataBlockWhenRoaming</span><span class="sxs-lookup"><span data-stu-id="32f44-116">cellularDataBlockWhenRoaming</span></span>|<span data-ttu-id="32f44-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="32f44-117">Boolean</span></span>|<span data-ttu-id="32f44-118">Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="32f44-118">If set to true, corresponding managed apps will not be allowed to use cellular data when roaming.</span></span>|
|<span data-ttu-id="32f44-119">cellularDataBlocked</span><span class="sxs-lookup"><span data-stu-id="32f44-119">cellularDataBlocked</span></span>|<span data-ttu-id="32f44-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="32f44-120">Boolean</span></span>|<span data-ttu-id="32f44-121">Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en ningún momento.</span><span class="sxs-lookup"><span data-stu-id="32f44-121">If set to true, corresponding managed apps will not be allowed to use cellular data at any time.</span></span>|

## <a name="relationships"></a><span data-ttu-id="32f44-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="32f44-122">Relationships</span></span>
<span data-ttu-id="32f44-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="32f44-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="32f44-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32f44-124">JSON Representation</span></span>
<span data-ttu-id="32f44-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="32f44-125">Here is a JSON representation of the resource.</span></span>
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





