---
title: tipo de recurso iosWebContentFilterAutoFilter
description: Representa un tipo de configuración de filtro de contenido Web, que habilita la característica de filtro automático de iOS y permite para control de acceso de dirección URL adicional de iOS. Cuando se construye sin valores de propiedad, el dispositivo iOS habilitará el filtro automático independientemente.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 03e3c4f51e673be1e2bada89e06a26048fe4e385
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916784"
---
# <a name="ioswebcontentfilterautofilter-resource-type"></a><span data-ttu-id="7da9a-104">tipo de recurso iosWebContentFilterAutoFilter</span><span class="sxs-lookup"><span data-stu-id="7da9a-104">iosWebContentFilterAutoFilter resource type</span></span>

> <span data-ttu-id="7da9a-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7da9a-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7da9a-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7da9a-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7da9a-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7da9a-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7da9a-108">Representa un tipo de configuración de filtro de contenido Web, que habilita la característica de filtro automático de iOS y permite para control de acceso de dirección URL adicional de iOS.</span><span class="sxs-lookup"><span data-stu-id="7da9a-108">Represents an iOS Web Content Filter setting type, which enables iOS automatic filter feature and allows for additional URL access control.</span></span> <span data-ttu-id="7da9a-109">Cuando se construye sin valores de propiedad, el dispositivo iOS habilitará el filtro automático independientemente.</span><span class="sxs-lookup"><span data-stu-id="7da9a-109">When constructed with no property values, the iOS device will enable the automatic filter regardless.</span></span>

<span data-ttu-id="7da9a-110">Hereda de [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)</span><span class="sxs-lookup"><span data-stu-id="7da9a-110">Inherits from [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="7da9a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7da9a-111">Properties</span></span>
|<span data-ttu-id="7da9a-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7da9a-112">Property</span></span>|<span data-ttu-id="7da9a-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="7da9a-113">Type</span></span>|<span data-ttu-id="7da9a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7da9a-114">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7da9a-115">allowedUrls</span><span class="sxs-lookup"><span data-stu-id="7da9a-115">allowedUrls</span></span>|<span data-ttu-id="7da9a-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="7da9a-116">String collection</span></span>|<span data-ttu-id="7da9a-117">Direcciones URL adicionales permitidas para el acceso</span><span class="sxs-lookup"><span data-stu-id="7da9a-117">Additional URLs allowed for access</span></span>|
|<span data-ttu-id="7da9a-118">blockedUrls</span><span class="sxs-lookup"><span data-stu-id="7da9a-118">blockedUrls</span></span>|<span data-ttu-id="7da9a-119">Colección String</span><span class="sxs-lookup"><span data-stu-id="7da9a-119">String collection</span></span>|<span data-ttu-id="7da9a-120">Bloqueada el acceso de las direcciones URL adicionales</span><span class="sxs-lookup"><span data-stu-id="7da9a-120">Additional URLs blocked for access</span></span>|

## <a name="relationships"></a><span data-ttu-id="7da9a-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7da9a-121">Relationships</span></span>
<span data-ttu-id="7da9a-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7da9a-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7da9a-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7da9a-123">JSON Representation</span></span>
<span data-ttu-id="7da9a-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7da9a-124">Here is a JSON representation of the resource.</span></span>
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





