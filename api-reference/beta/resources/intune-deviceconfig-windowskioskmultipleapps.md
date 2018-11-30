---
title: tipo de recurso windowsKioskMultipleApps
description: La clase que se usa para identificar la configuración de la aplicación de varios modos para la configuración de quiosco
ms.openlocfilehash: 2b52cbe343c4a8d81391ad448e8f10f64fef295e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085784"
---
# <a name="windowskioskmultipleapps-resource-type"></a><span data-ttu-id="871e0-103">tipo de recurso windowsKioskMultipleApps</span><span class="sxs-lookup"><span data-stu-id="871e0-103">windowsKioskMultipleApps resource type</span></span>

> <span data-ttu-id="871e0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="871e0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="871e0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="871e0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="871e0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="871e0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="871e0-107">La clase que se usa para identificar la configuración de la aplicación de varios modos para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="871e0-107">The class used to identify the MultiMode app configuration for the kiosk configuration</span></span>

<span data-ttu-id="871e0-108">Hereda de [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="871e0-108">Inherits from [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)</span></span>

## <a name="properties"></a><span data-ttu-id="871e0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="871e0-109">Properties</span></span>
|<span data-ttu-id="871e0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="871e0-110">Property</span></span>|<span data-ttu-id="871e0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="871e0-111">Type</span></span>|<span data-ttu-id="871e0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="871e0-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="871e0-113">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="871e0-113">apps</span></span>|<span data-ttu-id="871e0-114">colección de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="871e0-114">[windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md) collection</span></span>|<span data-ttu-id="871e0-115">Estos son el único almacén de aplicaciones de Windows que estará disponible para iniciar desde el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="871e0-115">These are the only Windows Store Apps that will be available to launch from the Start menu.</span></span>|
|<span data-ttu-id="871e0-116">showTaskBar</span><span class="sxs-lookup"><span data-stu-id="871e0-116">showTaskBar</span></span>|<span data-ttu-id="871e0-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="871e0-117">Boolean</span></span>|<span data-ttu-id="871e0-118">Esta opción le permite al administrador especificar si se muestra la barra de tareas o no.</span><span class="sxs-lookup"><span data-stu-id="871e0-118">This setting allows the admin to specify whether the Task Bar is shown or not.</span></span>|
|<span data-ttu-id="871e0-119">disallowDesktopApps</span><span class="sxs-lookup"><span data-stu-id="871e0-119">disallowDesktopApps</span></span>|<span data-ttu-id="871e0-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="871e0-120">Boolean</span></span>|<span data-ttu-id="871e0-121">Esta opción indica que se permiten aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="871e0-121">This setting indicates that desktop apps are allowed.</span></span> <span data-ttu-id="871e0-122">De forma predeterminada en true.</span><span class="sxs-lookup"><span data-stu-id="871e0-122">Default to true.</span></span>|
|<span data-ttu-id="871e0-123">startMenuLayoutXml</span><span class="sxs-lookup"><span data-stu-id="871e0-123">startMenuLayoutXml</span></span>|<span data-ttu-id="871e0-124">Binario</span><span class="sxs-lookup"><span data-stu-id="871e0-124">Binary</span></span>|<span data-ttu-id="871e0-125">Permite a los administradores invalidar el diseño de inicio predeterminado y se evita que el usuario que lo modifique.</span><span class="sxs-lookup"><span data-stu-id="871e0-125">Allows admins to override the default Start layout and prevents the user from changing it.</span></span><span data-ttu-id="871e0-126">Para modificar el diseño, se especifica un archivo XML basado en el esquema de modificación del diseño.</span><span class="sxs-lookup"><span data-stu-id="871e0-126"> The layout is modified by specifying an XML file based on a layout modification schema.</span></span> <span data-ttu-id="871e0-127">XML debe estar en formato binario.</span><span class="sxs-lookup"><span data-stu-id="871e0-127">XML needs to be in Binary format.</span></span>|

## <a name="relationships"></a><span data-ttu-id="871e0-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="871e0-128">Relationships</span></span>
<span data-ttu-id="871e0-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="871e0-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="871e0-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="871e0-130">JSON Representation</span></span>
<span data-ttu-id="871e0-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="871e0-131">Here is a JSON representation of the resource.</span></span>
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





