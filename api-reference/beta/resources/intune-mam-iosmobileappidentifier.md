---
title: Tipo de recurso iosMobileAppIdentifier
description: El identificador de una aplicación móvil de iOS.
ms.openlocfilehash: d95a9820c06d4d8e4122c3555e6e225c3d747761
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085250"
---
# <a name="iosmobileappidentifier-resource-type"></a><span data-ttu-id="ff10b-103">Tipo de recurso iosMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="ff10b-103">iosMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="ff10b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff10b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff10b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff10b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ff10b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ff10b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ff10b-107">El identificador de una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="ff10b-107">The identifier for an iOS app.</span></span>

<span data-ttu-id="ff10b-108">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="ff10b-108">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ff10b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff10b-109">Properties</span></span>
|<span data-ttu-id="ff10b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff10b-110">Property</span></span>|<span data-ttu-id="ff10b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff10b-111">Type</span></span>|<span data-ttu-id="ff10b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff10b-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ff10b-113">bundleId</span><span class="sxs-lookup"><span data-stu-id="ff10b-113">bundleId</span></span>|<span data-ttu-id="ff10b-114">cadena</span><span class="sxs-lookup"><span data-stu-id="ff10b-114">String</span></span>|<span data-ttu-id="ff10b-115">El identificador de una aplicación, como se especifica en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ff10b-115">The identifier for an app, as specified in the app store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ff10b-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ff10b-116">Relationships</span></span>
<span data-ttu-id="ff10b-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ff10b-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ff10b-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff10b-118">JSON Representation</span></span>
<span data-ttu-id="ff10b-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ff10b-119">Here is a JSON representation of the resource.</span></span>
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





