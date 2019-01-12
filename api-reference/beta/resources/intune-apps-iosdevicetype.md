---
title: Tipo de recurso iosDeviceType
description: Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2fe1f686052468bbab5d7115541a631b77073d6e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977167"
---
# <a name="iosdevicetype-resource-type"></a><span data-ttu-id="4fc7a-103">Tipo de recurso iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="4fc7a-103">iosDeviceType resource type</span></span>

> <span data-ttu-id="4fc7a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4fc7a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4fc7a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4fc7a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4fc7a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4fc7a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4fc7a-107">Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="4fc7a-107">Contains properties of the possible iOS device types the mobile app can run on.</span></span>
## <a name="properties"></a><span data-ttu-id="4fc7a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4fc7a-108">Properties</span></span>
|<span data-ttu-id="4fc7a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4fc7a-109">Property</span></span>|<span data-ttu-id="4fc7a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fc7a-110">Type</span></span>|<span data-ttu-id="4fc7a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fc7a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4fc7a-112">iPad</span><span class="sxs-lookup"><span data-stu-id="4fc7a-112">iPad</span></span>|<span data-ttu-id="4fc7a-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="4fc7a-113">Boolean</span></span>|<span data-ttu-id="4fc7a-114">Si la aplicación debe ejecutarse en iPad.</span><span class="sxs-lookup"><span data-stu-id="4fc7a-114">Whether the app should run on iPads.</span></span>|
|<span data-ttu-id="4fc7a-115">iPhoneAndIPod</span><span class="sxs-lookup"><span data-stu-id="4fc7a-115">iPhoneAndIPod</span></span>|<span data-ttu-id="4fc7a-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="4fc7a-116">Boolean</span></span>|<span data-ttu-id="4fc7a-117">Si la aplicación debe ejecutarse en iPhone y iPod.</span><span class="sxs-lookup"><span data-stu-id="4fc7a-117">Whether the app should run on iPhones and iPods.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4fc7a-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4fc7a-118">Relationships</span></span>
<span data-ttu-id="4fc7a-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4fc7a-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4fc7a-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4fc7a-120">JSON Representation</span></span>
<span data-ttu-id="4fc7a-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4fc7a-121">Here is a JSON representation of the resource.</span></span>
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





