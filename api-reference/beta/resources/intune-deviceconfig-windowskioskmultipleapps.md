---
title: tipo de recurso windowsKioskMultipleApps
description: La clase que se usa para identificar la configuración de la aplicación de varios modos para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3770f8c63be230dff97e43d3706ed35d79826751
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977132"
---
# <a name="windowskioskmultipleapps-resource-type"></a><span data-ttu-id="ce0cc-103">tipo de recurso windowsKioskMultipleApps</span><span class="sxs-lookup"><span data-stu-id="ce0cc-103">windowsKioskMultipleApps resource type</span></span>

> <span data-ttu-id="ce0cc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce0cc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ce0cc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce0cc-107">La clase que se usa para identificar la configuración de la aplicación de varios modos para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="ce0cc-107">The class used to identify the MultiMode app configuration for the kiosk configuration</span></span>

<span data-ttu-id="ce0cc-108">Hereda de [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce0cc-108">Inherits from [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ce0cc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce0cc-109">Properties</span></span>
|<span data-ttu-id="ce0cc-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce0cc-110">Property</span></span>|<span data-ttu-id="ce0cc-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce0cc-111">Type</span></span>|<span data-ttu-id="ce0cc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce0cc-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ce0cc-113">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ce0cc-113">apps</span></span>|<span data-ttu-id="ce0cc-114">colección de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="ce0cc-114">[windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md) collection</span></span>|<span data-ttu-id="ce0cc-115">Estos son el único almacén de aplicaciones de Windows que estará disponible para iniciar desde el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-115">These are the only Windows Store Apps that will be available to launch from the Start menu.</span></span>|
|<span data-ttu-id="ce0cc-116">showTaskBar</span><span class="sxs-lookup"><span data-stu-id="ce0cc-116">showTaskBar</span></span>|<span data-ttu-id="ce0cc-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="ce0cc-117">Boolean</span></span>|<span data-ttu-id="ce0cc-118">Esta opción le permite al administrador especificar si se muestra la barra de tareas o no.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-118">This setting allows the admin to specify whether the Task Bar is shown or not.</span></span>|
|<span data-ttu-id="ce0cc-119">disallowDesktopApps</span><span class="sxs-lookup"><span data-stu-id="ce0cc-119">disallowDesktopApps</span></span>|<span data-ttu-id="ce0cc-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="ce0cc-120">Boolean</span></span>|<span data-ttu-id="ce0cc-121">Esta opción indica que se permiten aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-121">This setting indicates that desktop apps are allowed.</span></span> <span data-ttu-id="ce0cc-122">De forma predeterminada en true.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-122">Default to true.</span></span>|
|<span data-ttu-id="ce0cc-123">startMenuLayoutXml</span><span class="sxs-lookup"><span data-stu-id="ce0cc-123">startMenuLayoutXml</span></span>|<span data-ttu-id="ce0cc-124">Binario</span><span class="sxs-lookup"><span data-stu-id="ce0cc-124">Binary</span></span>|<span data-ttu-id="ce0cc-125">Permite a los administradores invalidar el diseño de inicio predeterminado y se evita que el usuario que lo modifique.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-125">Allows admins to override the default Start layout and prevents the user from changing it.</span></span><span data-ttu-id="ce0cc-126">Para modificar el diseño, se especifica un archivo XML basado en el esquema de modificación del diseño.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-126"> The layout is modified by specifying an XML file based on a layout modification schema.</span></span> <span data-ttu-id="ce0cc-127">XML debe estar en formato binario.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-127">XML needs to be in Binary format.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ce0cc-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ce0cc-128">Relationships</span></span>
<span data-ttu-id="ce0cc-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ce0cc-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ce0cc-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce0cc-130">JSON Representation</span></span>
<span data-ttu-id="ce0cc-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ce0cc-131">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskMultipleApps"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskMultipleApps",
  "apps": [
    {
      "@odata.type": "microsoft.graph.windowsKioskUWPApp",
      "startLayoutTileSize": "String",
      "name": "String",
      "appUserModelId": "String",
      "appId": "String",
      "containedAppId": "String"
    }
  ],
  "showTaskBar": true,
  "disallowDesktopApps": true,
  "startMenuLayoutXml": "binary"
}
```





