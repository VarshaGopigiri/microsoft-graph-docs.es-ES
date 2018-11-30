---
title: Tipo de recurso iosMobileAppIdentifier
description: El identificador de una aplicación móvil de iOS.
ms.openlocfilehash: dbf37da4f225a42b1686896e3fa1fafa472b4a67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031850"
---
# <a name="iosmobileappidentifier-resource-type"></a><span data-ttu-id="e55d6-103">Tipo de recurso iosMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="e55d6-103">iosMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="e55d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e55d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e55d6-105">El identificador de una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="e55d6-105">The identifier for an iOS app.</span></span>

<span data-ttu-id="e55d6-106">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="e55d6-106">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e55d6-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e55d6-107">Properties</span></span>
|<span data-ttu-id="e55d6-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e55d6-108">Property</span></span>|<span data-ttu-id="e55d6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e55d6-109">Type</span></span>|<span data-ttu-id="e55d6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e55d6-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e55d6-111">bundleId</span><span class="sxs-lookup"><span data-stu-id="e55d6-111">bundleId</span></span>|<span data-ttu-id="e55d6-112">cadena</span><span class="sxs-lookup"><span data-stu-id="e55d6-112">String</span></span>|<span data-ttu-id="e55d6-113">El identificador de una aplicación, como se especifica en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e55d6-113">The identifier for an app, as specified in the app store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e55d6-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e55d6-114">Relationships</span></span>
<span data-ttu-id="e55d6-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e55d6-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e55d6-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e55d6-116">JSON Representation</span></span>
<span data-ttu-id="e55d6-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e55d6-117">Here is a JSON representation of the resource.</span></span>
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



