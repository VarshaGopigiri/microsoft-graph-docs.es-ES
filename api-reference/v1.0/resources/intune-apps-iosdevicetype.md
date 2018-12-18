---
title: Tipo de recurso iosDeviceType
description: Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.
author: tfitzmac
ms.openlocfilehash: 3111bc4b5fc78f6ed60b4a241b48e443923f7159
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313604"
---
# <a name="iosdevicetype-resource-type"></a><span data-ttu-id="00525-103">Tipo de recurso iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="00525-103">iosDeviceType resource type</span></span>

> <span data-ttu-id="00525-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="00525-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="00525-105">Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="00525-105">Contains properties of the possible iOS device types the mobile app can run on.</span></span>
## <a name="properties"></a><span data-ttu-id="00525-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00525-106">Properties</span></span>
|<span data-ttu-id="00525-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00525-107">Property</span></span>|<span data-ttu-id="00525-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="00525-108">Type</span></span>|<span data-ttu-id="00525-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="00525-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="00525-110">iPad</span><span class="sxs-lookup"><span data-stu-id="00525-110">iPad</span></span>|<span data-ttu-id="00525-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="00525-111">Boolean</span></span>|<span data-ttu-id="00525-112">Si la aplicación debe ejecutarse en iPad.</span><span class="sxs-lookup"><span data-stu-id="00525-112">Whether the app should run on iPads.</span></span>|
|<span data-ttu-id="00525-113">iPhoneAndIPod</span><span class="sxs-lookup"><span data-stu-id="00525-113">iPhoneAndIPod</span></span>|<span data-ttu-id="00525-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="00525-114">Boolean</span></span>|<span data-ttu-id="00525-115">Si la aplicación debe ejecutarse en iPhone y iPod.</span><span class="sxs-lookup"><span data-stu-id="00525-115">Whether the app should run on iPhones and iPods.</span></span>|

## <a name="relationships"></a><span data-ttu-id="00525-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="00525-116">Relationships</span></span>
<span data-ttu-id="00525-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="00525-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="00525-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="00525-118">JSON Representation</span></span>
<span data-ttu-id="00525-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="00525-119">Here is a JSON representation of the resource.</span></span>
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



