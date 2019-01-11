---
title: Tipo de recurso androidMobileAppIdentifier
description: El identificador de una aplicación móvil de Android.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 9cc203cc9268849e8b7b46d994c166378252df59
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871746"
---
# <a name="androidmobileappidentifier-resource-type"></a><span data-ttu-id="0e2a4-103">Tipo de recurso androidMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="0e2a4-103">androidMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="0e2a4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e2a4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e2a4-105">El identificador de una aplicación móvil de Android.</span><span class="sxs-lookup"><span data-stu-id="0e2a4-105">The identifier for an Android app.</span></span>

<span data-ttu-id="0e2a4-106">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="0e2a4-106">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="0e2a4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e2a4-107">Properties</span></span>
|<span data-ttu-id="0e2a4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e2a4-108">Property</span></span>|<span data-ttu-id="0e2a4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e2a4-109">Type</span></span>|<span data-ttu-id="0e2a4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e2a4-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e2a4-111">packageId</span><span class="sxs-lookup"><span data-stu-id="0e2a4-111">packageId</span></span>|<span data-ttu-id="0e2a4-112">cadena</span><span class="sxs-lookup"><span data-stu-id="0e2a4-112">String</span></span>|<span data-ttu-id="0e2a4-113">El identificador de una aplicación, como se especifica en la Play Store.</span><span class="sxs-lookup"><span data-stu-id="0e2a4-113">The identifier for an app, as specified in the play store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0e2a4-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0e2a4-114">Relationships</span></span>
<span data-ttu-id="0e2a4-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0e2a4-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0e2a4-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0e2a4-116">JSON Representation</span></span>
<span data-ttu-id="0e2a4-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0e2a4-117">Here is a JSON representation of the resource.</span></span>
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



