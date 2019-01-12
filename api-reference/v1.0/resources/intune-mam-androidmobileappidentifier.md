---
title: Tipo de recurso androidMobileAppIdentifier
description: El identificador de una aplicación móvil de Android.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6a940acc726467634df3a64dc686824350abf98f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915070"
---
# <a name="androidmobileappidentifier-resource-type"></a><span data-ttu-id="789ed-103">Tipo de recurso androidMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="789ed-103">androidMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="789ed-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="789ed-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="789ed-105">El identificador de una aplicación móvil de Android.</span><span class="sxs-lookup"><span data-stu-id="789ed-105">The identifier for an Android app.</span></span>

<span data-ttu-id="789ed-106">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="789ed-106">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="789ed-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="789ed-107">Properties</span></span>
|<span data-ttu-id="789ed-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="789ed-108">Property</span></span>|<span data-ttu-id="789ed-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="789ed-109">Type</span></span>|<span data-ttu-id="789ed-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="789ed-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="789ed-111">packageId</span><span class="sxs-lookup"><span data-stu-id="789ed-111">packageId</span></span>|<span data-ttu-id="789ed-112">cadena</span><span class="sxs-lookup"><span data-stu-id="789ed-112">String</span></span>|<span data-ttu-id="789ed-113">El identificador de una aplicación, como se especifica en la Play Store.</span><span class="sxs-lookup"><span data-stu-id="789ed-113">The identifier for an app, as specified in the play store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="789ed-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="789ed-114">Relationships</span></span>
<span data-ttu-id="789ed-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="789ed-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="789ed-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="789ed-116">JSON Representation</span></span>
<span data-ttu-id="789ed-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="789ed-117">Here is a JSON representation of the resource.</span></span>
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



