---
title: tipo de recurso iosWebContentFilterAutoFilter
description: Representa un tipo de configuración de filtro de contenido Web, que habilita la característica de filtro automático de iOS y permite para control de acceso de dirección URL adicional de iOS. Cuando se construye sin valores de propiedad, el dispositivo iOS habilitará el filtro automático independientemente.
localization_priority: Normal
ms.openlocfilehash: 02576565ecf764d33312477531d6a76c61911cb6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868134"
---
# <a name="ioswebcontentfilterautofilter-resource-type"></a><span data-ttu-id="c5a93-104">tipo de recurso iosWebContentFilterAutoFilter</span><span class="sxs-lookup"><span data-stu-id="c5a93-104">iosWebContentFilterAutoFilter resource type</span></span>

> <span data-ttu-id="c5a93-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5a93-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5a93-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5a93-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c5a93-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c5a93-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c5a93-108">Representa un tipo de configuración de filtro de contenido Web, que habilita la característica de filtro automático de iOS y permite para control de acceso de dirección URL adicional de iOS.</span><span class="sxs-lookup"><span data-stu-id="c5a93-108">Represents an iOS Web Content Filter setting type, which enables iOS automatic filter feature and allows for additional URL access control.</span></span> <span data-ttu-id="c5a93-109">Cuando se construye sin valores de propiedad, el dispositivo iOS habilitará el filtro automático independientemente.</span><span class="sxs-lookup"><span data-stu-id="c5a93-109">When constructed with no property values, the iOS device will enable the automatic filter regardless.</span></span>

<span data-ttu-id="c5a93-110">Hereda de [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)</span><span class="sxs-lookup"><span data-stu-id="c5a93-110">Inherits from [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c5a93-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5a93-111">Properties</span></span>
|<span data-ttu-id="c5a93-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5a93-112">Property</span></span>|<span data-ttu-id="c5a93-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5a93-113">Type</span></span>|<span data-ttu-id="c5a93-114">Description</span><span class="sxs-lookup"><span data-stu-id="c5a93-114">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c5a93-115">allowedUrls</span><span class="sxs-lookup"><span data-stu-id="c5a93-115">allowedUrls</span></span>|<span data-ttu-id="c5a93-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="c5a93-116">String collection</span></span>|<span data-ttu-id="c5a93-117">Direcciones URL adicionales permitidas para el acceso</span><span class="sxs-lookup"><span data-stu-id="c5a93-117">Additional URLs allowed for access</span></span>|
|<span data-ttu-id="c5a93-118">blockedUrls</span><span class="sxs-lookup"><span data-stu-id="c5a93-118">blockedUrls</span></span>|<span data-ttu-id="c5a93-119">Colección String</span><span class="sxs-lookup"><span data-stu-id="c5a93-119">String collection</span></span>|<span data-ttu-id="c5a93-120">Bloqueada el acceso de las direcciones URL adicionales</span><span class="sxs-lookup"><span data-stu-id="c5a93-120">Additional URLs blocked for access</span></span>|

## <a name="relationships"></a><span data-ttu-id="c5a93-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c5a93-121">Relationships</span></span>
<span data-ttu-id="c5a93-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c5a93-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c5a93-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c5a93-123">JSON Representation</span></span>
<span data-ttu-id="c5a93-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c5a93-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosWebContentFilterAutoFilter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosWebContentFilterAutoFilter",
  "allowedUrls": [
    "String"
  ],
  "blockedUrls": [
    "String"
  ]
}
```





