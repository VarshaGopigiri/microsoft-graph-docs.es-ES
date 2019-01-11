---
title: Tipo de recurso iosDeviceType
description: Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ffa46d1e8fb693822051250fb4a722815b1dcb73
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866783"
---
# <a name="iosdevicetype-resource-type"></a><span data-ttu-id="ab122-103">Tipo de recurso iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="ab122-103">iosDeviceType resource type</span></span>

> <span data-ttu-id="ab122-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab122-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab122-105">Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="ab122-105">Contains properties of the possible iOS device types the mobile app can run on.</span></span>
## <a name="properties"></a><span data-ttu-id="ab122-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab122-106">Properties</span></span>
|<span data-ttu-id="ab122-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab122-107">Property</span></span>|<span data-ttu-id="ab122-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab122-108">Type</span></span>|<span data-ttu-id="ab122-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab122-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab122-110">iPad</span><span class="sxs-lookup"><span data-stu-id="ab122-110">iPad</span></span>|<span data-ttu-id="ab122-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab122-111">Boolean</span></span>|<span data-ttu-id="ab122-112">Si la aplicación debe ejecutarse en iPad.</span><span class="sxs-lookup"><span data-stu-id="ab122-112">Whether the app should run on iPads.</span></span>|
|<span data-ttu-id="ab122-113">iPhoneAndIPod</span><span class="sxs-lookup"><span data-stu-id="ab122-113">iPhoneAndIPod</span></span>|<span data-ttu-id="ab122-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab122-114">Boolean</span></span>|<span data-ttu-id="ab122-115">Si la aplicación debe ejecutarse en iPhone y iPod.</span><span class="sxs-lookup"><span data-stu-id="ab122-115">Whether the app should run on iPhones and iPods.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ab122-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ab122-116">Relationships</span></span>
<span data-ttu-id="ab122-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ab122-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ab122-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab122-118">JSON Representation</span></span>
<span data-ttu-id="ab122-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ab122-119">Here is a JSON representation of the resource.</span></span>
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



