---
title: Tipo de recurso androidMobileAppIdentifier
description: El identificador de una aplicación móvil de Android.
ms.openlocfilehash: 16f142c40083b9410f84e128951680ced269ea12
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031020"
---
# <a name="androidmobileappidentifier-resource-type"></a><span data-ttu-id="60746-103">Tipo de recurso androidMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="60746-103">androidMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="60746-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="60746-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="60746-105">El identificador de una aplicación móvil de Android.</span><span class="sxs-lookup"><span data-stu-id="60746-105">The identifier for an Android app.</span></span>

<span data-ttu-id="60746-106">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="60746-106">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="60746-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60746-107">Properties</span></span>
|<span data-ttu-id="60746-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60746-108">Property</span></span>|<span data-ttu-id="60746-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="60746-109">Type</span></span>|<span data-ttu-id="60746-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="60746-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="60746-111">packageId</span><span class="sxs-lookup"><span data-stu-id="60746-111">packageId</span></span>|<span data-ttu-id="60746-112">cadena</span><span class="sxs-lookup"><span data-stu-id="60746-112">String</span></span>|<span data-ttu-id="60746-113">El identificador de una aplicación, como se especifica en la Play Store.</span><span class="sxs-lookup"><span data-stu-id="60746-113">The identifier for an app, as specified in the play store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="60746-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="60746-114">Relationships</span></span>
<span data-ttu-id="60746-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="60746-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="60746-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60746-116">JSON Representation</span></span>
<span data-ttu-id="60746-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="60746-117">Here is a JSON representation of the resource.</span></span>
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



