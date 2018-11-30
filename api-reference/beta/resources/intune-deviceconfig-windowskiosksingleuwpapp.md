---
title: tipo de recurso windowsKioskSingleUWPApp
description: La clase que se usa para identificar la información de aplicación UWP para la configuración de quiosco
ms.openlocfilehash: 009d53d1439894b59a89a1f269df34c4dbb09ce1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088111"
---
# <a name="windowskiosksingleuwpapp-resource-type"></a><span data-ttu-id="2286f-103">tipo de recurso windowsKioskSingleUWPApp</span><span class="sxs-lookup"><span data-stu-id="2286f-103">windowsKioskSingleUWPApp resource type</span></span>

> <span data-ttu-id="2286f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2286f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2286f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2286f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2286f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2286f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2286f-107">La clase que se usa para identificar la información de aplicación UWP para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="2286f-107">The class used to identify the UWP app info for the kiosk configuration</span></span>

<span data-ttu-id="2286f-108">Hereda de [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2286f-108">Inherits from [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span></span>

## <a name="properties"></a><span data-ttu-id="2286f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2286f-109">Properties</span></span>
|<span data-ttu-id="2286f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2286f-110">Property</span></span>|<span data-ttu-id="2286f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2286f-111">Type</span></span>|<span data-ttu-id="2286f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2286f-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2286f-113">uwpApp</span><span class="sxs-lookup"><span data-stu-id="2286f-113">uwpApp</span></span>|[<span data-ttu-id="2286f-114">windowsKioskUWPApp</span><span class="sxs-lookup"><span data-stu-id="2286f-114">windowsKioskUWPApp</span></span>](../resources/intune-deviceconfig-windowskioskuwpapp.md)|<span data-ttu-id="2286f-115">Esta es la única aplicación de usuario modelo de identificador (AUMID) que estará disponible para iniciar el uso en el modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="2286f-115">This is the only Application User Model ID (AUMID) that will be available to launch use while in Kiosk Mode</span></span>|

## <a name="relationships"></a><span data-ttu-id="2286f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2286f-116">Relationships</span></span>
<span data-ttu-id="2286f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2286f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2286f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2286f-118">JSON Representation</span></span>
<span data-ttu-id="2286f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2286f-119">Here is a JSON representation of the resource.</span></span>
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





