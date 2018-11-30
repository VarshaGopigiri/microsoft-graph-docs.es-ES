---
title: Tipo de recurso iosDeviceType
description: Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.
ms.openlocfilehash: b14abbb6713daf9fad7b0d2fd6f7865d251b6147
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030603"
---
# <a name="iosdevicetype-resource-type"></a><span data-ttu-id="71cf8-103">Tipo de recurso iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="71cf8-103">iosDeviceType resource type</span></span>

> <span data-ttu-id="71cf8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71cf8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71cf8-105">Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="71cf8-105">Contains properties of the possible iOS device types the mobile app can run on.</span></span>
## <a name="properties"></a><span data-ttu-id="71cf8-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71cf8-106">Properties</span></span>
|<span data-ttu-id="71cf8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71cf8-107">Property</span></span>|<span data-ttu-id="71cf8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="71cf8-108">Type</span></span>|<span data-ttu-id="71cf8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="71cf8-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="71cf8-110">iPad</span><span class="sxs-lookup"><span data-stu-id="71cf8-110">iPad</span></span>|<span data-ttu-id="71cf8-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="71cf8-111">Boolean</span></span>|<span data-ttu-id="71cf8-112">Si la aplicación debe ejecutarse en iPad.</span><span class="sxs-lookup"><span data-stu-id="71cf8-112">Whether the app should run on iPads.</span></span>|
|<span data-ttu-id="71cf8-113">iPhoneAndIPod</span><span class="sxs-lookup"><span data-stu-id="71cf8-113">iPhoneAndIPod</span></span>|<span data-ttu-id="71cf8-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="71cf8-114">Boolean</span></span>|<span data-ttu-id="71cf8-115">Si la aplicación debe ejecutarse en iPhone y iPod.</span><span class="sxs-lookup"><span data-stu-id="71cf8-115">Whether the app should run on iPhones and iPods.</span></span>|

## <a name="relationships"></a><span data-ttu-id="71cf8-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="71cf8-116">Relationships</span></span>
<span data-ttu-id="71cf8-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="71cf8-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="71cf8-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="71cf8-118">JSON Representation</span></span>
<span data-ttu-id="71cf8-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="71cf8-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosDeviceType"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosDeviceType",
  "iPad": true,
  "iPhoneAndIPod": true
}
```



