---
title: Tipo de recurso androidMobileAppIdentifier
description: El identificador de una aplicación móvil de Android.
author: tfitzmac
ms.openlocfilehash: fa55d84c3f676d23caeba1e5fda33166b60aaada
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350830"
---
# <a name="androidmobileappidentifier-resource-type"></a><span data-ttu-id="149a3-103">Tipo de recurso androidMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="149a3-103">androidMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="149a3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="149a3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="149a3-105">El identificador de una aplicación móvil de Android.</span><span class="sxs-lookup"><span data-stu-id="149a3-105">The identifier for an Android app.</span></span>

<span data-ttu-id="149a3-106">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="149a3-106">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="149a3-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="149a3-107">Properties</span></span>
|<span data-ttu-id="149a3-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="149a3-108">Property</span></span>|<span data-ttu-id="149a3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="149a3-109">Type</span></span>|<span data-ttu-id="149a3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="149a3-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="149a3-111">packageId</span><span class="sxs-lookup"><span data-stu-id="149a3-111">packageId</span></span>|<span data-ttu-id="149a3-112">cadena</span><span class="sxs-lookup"><span data-stu-id="149a3-112">String</span></span>|<span data-ttu-id="149a3-113">El identificador de una aplicación, como se especifica en la Play Store.</span><span class="sxs-lookup"><span data-stu-id="149a3-113">The identifier for an app, as specified in the play store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="149a3-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="149a3-114">Relationships</span></span>
<span data-ttu-id="149a3-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="149a3-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="149a3-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="149a3-116">JSON Representation</span></span>
<span data-ttu-id="149a3-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="149a3-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidMobileAppIdentifier"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidMobileAppIdentifier",
  "packageId": "String"
}
```



