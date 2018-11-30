---
title: Tipo de recurso iosDeviceType
description: Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.
ms.openlocfilehash: 4d85d8801934e6f240bacd6fafe63c7bd1ee946f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087152"
---
# <a name="iosdevicetype-resource-type"></a><span data-ttu-id="7a67b-103">Tipo de recurso iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="7a67b-103">iosDeviceType resource type</span></span>

> <span data-ttu-id="7a67b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7a67b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7a67b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7a67b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7a67b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a67b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a67b-107">Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="7a67b-107">Contains properties of the possible iOS device types the mobile app can run on.</span></span>
## <a name="properties"></a><span data-ttu-id="7a67b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a67b-108">Properties</span></span>
|<span data-ttu-id="7a67b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a67b-109">Property</span></span>|<span data-ttu-id="7a67b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a67b-110">Type</span></span>|<span data-ttu-id="7a67b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a67b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a67b-112">iPad</span><span class="sxs-lookup"><span data-stu-id="7a67b-112">iPad</span></span>|<span data-ttu-id="7a67b-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="7a67b-113">Boolean</span></span>|<span data-ttu-id="7a67b-114">Si la aplicación debe ejecutarse en iPad.</span><span class="sxs-lookup"><span data-stu-id="7a67b-114">Whether the app should run on iPads.</span></span>|
|<span data-ttu-id="7a67b-115">iPhoneAndIPod</span><span class="sxs-lookup"><span data-stu-id="7a67b-115">iPhoneAndIPod</span></span>|<span data-ttu-id="7a67b-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="7a67b-116">Boolean</span></span>|<span data-ttu-id="7a67b-117">Si la aplicación debe ejecutarse en iPhone y iPod.</span><span class="sxs-lookup"><span data-stu-id="7a67b-117">Whether the app should run on iPhones and iPods.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7a67b-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7a67b-118">Relationships</span></span>
<span data-ttu-id="7a67b-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7a67b-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7a67b-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a67b-120">JSON Representation</span></span>
<span data-ttu-id="7a67b-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7a67b-121">Here is a JSON representation of the resource.</span></span>
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





