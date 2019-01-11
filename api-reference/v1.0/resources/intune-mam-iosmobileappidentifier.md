---
title: Tipo de recurso iosMobileAppIdentifier
description: El identificador de una aplicación móvil de iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5dd2ee1531c2bfe2399949d2e08a209826079cb8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875841"
---
# <a name="iosmobileappidentifier-resource-type"></a><span data-ttu-id="72b13-103">Tipo de recurso iosMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="72b13-103">iosMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="72b13-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="72b13-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="72b13-105">El identificador de una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="72b13-105">The identifier for an iOS app.</span></span>

<span data-ttu-id="72b13-106">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="72b13-106">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="72b13-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72b13-107">Properties</span></span>
|<span data-ttu-id="72b13-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72b13-108">Property</span></span>|<span data-ttu-id="72b13-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="72b13-109">Type</span></span>|<span data-ttu-id="72b13-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="72b13-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72b13-111">bundleId</span><span class="sxs-lookup"><span data-stu-id="72b13-111">bundleId</span></span>|<span data-ttu-id="72b13-112">cadena</span><span class="sxs-lookup"><span data-stu-id="72b13-112">String</span></span>|<span data-ttu-id="72b13-113">El identificador de una aplicación, como se especifica en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="72b13-113">The identifier for an app, as specified in the app store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="72b13-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="72b13-114">Relationships</span></span>
<span data-ttu-id="72b13-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="72b13-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="72b13-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="72b13-116">JSON Representation</span></span>
<span data-ttu-id="72b13-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="72b13-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosMobileAppIdentifier"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMobileAppIdentifier",
  "bundleId": "String"
}
```



