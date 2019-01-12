---
title: tipo de recurso windowsKioskDesktopApp
description: La clase base para un tipo de aplicaciones
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a9b808bfd67e1b14e0b11fe84da48b77b4d965ba
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947333"
---
# <a name="windowskioskdesktopapp-resource-type"></a><span data-ttu-id="c912c-103">tipo de recurso windowsKioskDesktopApp</span><span class="sxs-lookup"><span data-stu-id="c912c-103">windowsKioskDesktopApp resource type</span></span>

> <span data-ttu-id="c912c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c912c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c912c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c912c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c912c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c912c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c912c-107">La clase base para un tipo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c912c-107">The base class for a type of apps</span></span>

<span data-ttu-id="c912c-108">Hereda de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="c912c-108">Inherits from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c912c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c912c-109">Properties</span></span>
|<span data-ttu-id="c912c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c912c-110">Property</span></span>|<span data-ttu-id="c912c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c912c-111">Type</span></span>|<span data-ttu-id="c912c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c912c-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c912c-113">startLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="c912c-113">startLayoutTileSize</span></span>|[<span data-ttu-id="c912c-114">windowsAppStartLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="c912c-114">windowsAppStartLayoutTileSize</span></span>](../resources/intune-deviceconfig-windowsappstartlayouttilesize.md)|<span data-ttu-id="c912c-115">El tamaño del mosaico de aplicación para el diseño de inicio Inherited desde [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md).</span><span class="sxs-lookup"><span data-stu-id="c912c-115">The app tile size for the start layout Inherited from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md).</span></span> <span data-ttu-id="c912c-116">Los valores posibles son: `hidden`, `small`, `medium`, `wide` y `large`.</span><span class="sxs-lookup"><span data-stu-id="c912c-116">Possible values are: `hidden`, `small`, `medium`, `wide`, `large`.</span></span>|
|<span data-ttu-id="c912c-117">name</span><span class="sxs-lookup"><span data-stu-id="c912c-117">name</span></span>|<span data-ttu-id="c912c-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="c912c-118">String</span></span>|<span data-ttu-id="c912c-119">Representa el nombre descriptivo de una aplicación heredada de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="c912c-119">Represents the friendly name of an app Inherited from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span></span>|
|<span data-ttu-id="c912c-120">ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="c912c-120">path</span></span>|<span data-ttu-id="c912c-121">String</span><span class="sxs-lookup"><span data-stu-id="c912c-121">String</span></span>|<span data-ttu-id="c912c-122">Definir la ruta de acceso de una aplicación de escritorio</span><span class="sxs-lookup"><span data-stu-id="c912c-122">Define the path of a desktop app</span></span>|
|<span data-ttu-id="c912c-123">desktopApplicationId</span><span class="sxs-lookup"><span data-stu-id="c912c-123">desktopApplicationId</span></span>|<span data-ttu-id="c912c-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="c912c-124">String</span></span>|<span data-ttu-id="c912c-125">Definir la DesktopApplicationID de la aplicación</span><span class="sxs-lookup"><span data-stu-id="c912c-125">Define the DesktopApplicationID of the app</span></span>|
|<span data-ttu-id="c912c-126">desktopApplicationLinkPath</span><span class="sxs-lookup"><span data-stu-id="c912c-126">desktopApplicationLinkPath</span></span>|<span data-ttu-id="c912c-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="c912c-127">String</span></span>|<span data-ttu-id="c912c-128">Definir la DesktopApplicationLinkPath de la aplicación</span><span class="sxs-lookup"><span data-stu-id="c912c-128">Define the DesktopApplicationLinkPath of the app</span></span>|

## <a name="relationships"></a><span data-ttu-id="c912c-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c912c-129">Relationships</span></span>
<span data-ttu-id="c912c-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c912c-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c912c-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c912c-131">JSON Representation</span></span>
<span data-ttu-id="c912c-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c912c-132">Here is a JSON representation of the resource.</span></span>
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





