---
title: Tipo de recurso iosMobileAppIdentifier
description: El identificador de una aplicación móvil de iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5e9305963654356c56bff31f6ffb9f97129f4980
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922791"
---
# <a name="iosmobileappidentifier-resource-type"></a><span data-ttu-id="e573c-103">Tipo de recurso iosMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="e573c-103">iosMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="e573c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e573c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e573c-105">El identificador de una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="e573c-105">The identifier for an iOS app.</span></span>

<span data-ttu-id="e573c-106">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="e573c-106">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e573c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e573c-107">Properties</span></span>
|<span data-ttu-id="e573c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e573c-108">Property</span></span>|<span data-ttu-id="e573c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e573c-109">Type</span></span>|<span data-ttu-id="e573c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e573c-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e573c-111">bundleId</span><span class="sxs-lookup"><span data-stu-id="e573c-111">bundleId</span></span>|<span data-ttu-id="e573c-112">cadena</span><span class="sxs-lookup"><span data-stu-id="e573c-112">String</span></span>|<span data-ttu-id="e573c-113">El identificador de una aplicación, como se especifica en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e573c-113">The identifier for an app, as specified in the app store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e573c-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e573c-114">Relationships</span></span>
<span data-ttu-id="e573c-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e573c-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e573c-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e573c-116">JSON Representation</span></span>
<span data-ttu-id="e573c-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e573c-117">Here is a JSON representation of the resource.</span></span>
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



