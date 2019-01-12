---
title: tipo de recurso windowsKioskSingleUWPApp
description: La clase que se usa para identificar la información de aplicación UWP para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c59af9f5828a56d6d55e0f2bc0dc486e45321e8b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959096"
---
# <a name="windowskiosksingleuwpapp-resource-type"></a><span data-ttu-id="fb752-103">tipo de recurso windowsKioskSingleUWPApp</span><span class="sxs-lookup"><span data-stu-id="fb752-103">windowsKioskSingleUWPApp resource type</span></span>

> <span data-ttu-id="fb752-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb752-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb752-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb752-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fb752-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb752-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb752-107">La clase que se usa para identificar la información de aplicación UWP para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="fb752-107">The class used to identify the UWP app info for the kiosk configuration</span></span>

<span data-ttu-id="fb752-108">Hereda de [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fb752-108">Inherits from [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span></span>

## <a name="properties"></a><span data-ttu-id="fb752-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb752-109">Properties</span></span>
|<span data-ttu-id="fb752-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb752-110">Property</span></span>|<span data-ttu-id="fb752-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb752-111">Type</span></span>|<span data-ttu-id="fb752-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb752-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb752-113">uwpApp</span><span class="sxs-lookup"><span data-stu-id="fb752-113">uwpApp</span></span>|[<span data-ttu-id="fb752-114">windowsKioskUWPApp</span><span class="sxs-lookup"><span data-stu-id="fb752-114">windowsKioskUWPApp</span></span>](../resources/intune-deviceconfig-windowskioskuwpapp.md)|<span data-ttu-id="fb752-115">Esta es la única aplicación de usuario modelo de identificador (AUMID) que estará disponible para iniciar el uso en el modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="fb752-115">This is the only Application User Model ID (AUMID) that will be available to launch use while in Kiosk Mode</span></span>|

## <a name="relationships"></a><span data-ttu-id="fb752-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fb752-116">Relationships</span></span>
<span data-ttu-id="fb752-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fb752-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fb752-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb752-118">JSON Representation</span></span>
<span data-ttu-id="fb752-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fb752-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskSingleUWPApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskSingleUWPApp",
  "uwpApp": {
    "@odata.type": "microsoft.graph.windowsKioskUWPApp",
    "startLayoutTileSize": "String",
    "name": "String",
    "appUserModelId": "String",
    "appId": "String",
    "containedAppId": "String"
  }
}
```





