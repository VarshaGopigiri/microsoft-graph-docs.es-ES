---
title: tipo de recurso windowsKioskDesktopApp
description: La clase base para un tipo de aplicaciones
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 53eb615dcd1ba2b88c6cdd4bb5a1b76b83b67eaf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830978"
---
# <a name="windowskioskdesktopapp-resource-type"></a><span data-ttu-id="3ed17-103">tipo de recurso windowsKioskDesktopApp</span><span class="sxs-lookup"><span data-stu-id="3ed17-103">windowsKioskDesktopApp resource type</span></span>

> <span data-ttu-id="3ed17-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3ed17-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3ed17-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3ed17-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3ed17-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3ed17-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3ed17-107">La clase base para un tipo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="3ed17-107">The base class for a type of apps</span></span>

<span data-ttu-id="3ed17-108">Hereda de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="3ed17-108">Inherits from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="3ed17-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ed17-109">Properties</span></span>
|<span data-ttu-id="3ed17-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3ed17-110">Property</span></span>|<span data-ttu-id="3ed17-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ed17-111">Type</span></span>|<span data-ttu-id="3ed17-112">Description</span><span class="sxs-lookup"><span data-stu-id="3ed17-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3ed17-113">startLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="3ed17-113">startLayoutTileSize</span></span>|[<span data-ttu-id="3ed17-114">windowsAppStartLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="3ed17-114">windowsAppStartLayoutTileSize</span></span>](../resources/intune-deviceconfig-windowsappstartlayouttilesize.md)|<span data-ttu-id="3ed17-115">El tamaño del mosaico de aplicación para el diseño de inicio Inherited desde [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md).</span><span class="sxs-lookup"><span data-stu-id="3ed17-115">The app tile size for the start layout Inherited from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md).</span></span> <span data-ttu-id="3ed17-116">Los valores posibles son: `hidden`, `small`, `medium`, `wide` y `large`.</span><span class="sxs-lookup"><span data-stu-id="3ed17-116">Possible values are: `hidden`, `small`, `medium`, `wide`, `large`.</span></span>|
|<span data-ttu-id="3ed17-117">name</span><span class="sxs-lookup"><span data-stu-id="3ed17-117">name</span></span>|<span data-ttu-id="3ed17-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="3ed17-118">String</span></span>|<span data-ttu-id="3ed17-119">Representa el nombre descriptivo de una aplicación heredada de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="3ed17-119">Represents the friendly name of an app Inherited from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span></span>|
|<span data-ttu-id="3ed17-120">ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="3ed17-120">path</span></span>|<span data-ttu-id="3ed17-121">String</span><span class="sxs-lookup"><span data-stu-id="3ed17-121">String</span></span>|<span data-ttu-id="3ed17-122">Definir la ruta de acceso de una aplicación de escritorio</span><span class="sxs-lookup"><span data-stu-id="3ed17-122">Define the path of a desktop app</span></span>|
|<span data-ttu-id="3ed17-123">desktopApplicationId</span><span class="sxs-lookup"><span data-stu-id="3ed17-123">desktopApplicationId</span></span>|<span data-ttu-id="3ed17-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="3ed17-124">String</span></span>|<span data-ttu-id="3ed17-125">Definir la DesktopApplicationID de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3ed17-125">Define the DesktopApplicationID of the app</span></span>|
|<span data-ttu-id="3ed17-126">desktopApplicationLinkPath</span><span class="sxs-lookup"><span data-stu-id="3ed17-126">desktopApplicationLinkPath</span></span>|<span data-ttu-id="3ed17-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="3ed17-127">String</span></span>|<span data-ttu-id="3ed17-128">Definir la DesktopApplicationLinkPath de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3ed17-128">Define the DesktopApplicationLinkPath of the app</span></span>|

## <a name="relationships"></a><span data-ttu-id="3ed17-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3ed17-129">Relationships</span></span>
<span data-ttu-id="3ed17-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3ed17-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3ed17-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3ed17-131">JSON Representation</span></span>
<span data-ttu-id="3ed17-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3ed17-132">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskDesktopApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskDesktopApp",
  "startLayoutTileSize": "String",
  "name": "String",
  "path": "String",
  "desktopApplicationId": "String",
  "desktopApplicationLinkPath": "String"
}
```





