---
title: tipo de recurso windowsKioskUWPApp
description: La clase base para un tipo de aplicaciones
ms.openlocfilehash: 8d0d6c609eec4b8194bb72d2fb723d1816873e75
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085777"
---
# <a name="windowskioskuwpapp-resource-type"></a><span data-ttu-id="bf71c-103">tipo de recurso windowsKioskUWPApp</span><span class="sxs-lookup"><span data-stu-id="bf71c-103">windowsKioskUWPApp resource type</span></span>

> <span data-ttu-id="bf71c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf71c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf71c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf71c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bf71c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf71c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf71c-107">La clase base para un tipo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bf71c-107">The base class for a type of apps</span></span>

<span data-ttu-id="bf71c-108">Hereda de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="bf71c-108">Inherits from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="bf71c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf71c-109">Properties</span></span>
|<span data-ttu-id="bf71c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf71c-110">Property</span></span>|<span data-ttu-id="bf71c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf71c-111">Type</span></span>|<span data-ttu-id="bf71c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf71c-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf71c-113">startLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="bf71c-113">startLayoutTileSize</span></span>|[<span data-ttu-id="bf71c-114">windowsAppStartLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="bf71c-114">windowsAppStartLayoutTileSize</span></span>](../resources/intune-deviceconfig-windowsappstartlayouttilesize.md)|<span data-ttu-id="bf71c-115">El tamaño del mosaico de aplicación para el diseño de inicio Inherited desde [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md).</span><span class="sxs-lookup"><span data-stu-id="bf71c-115">The app tile size for the start layout Inherited from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md).</span></span> <span data-ttu-id="bf71c-116">Los valores posibles son: `hidden`, `small`, `medium`, `wide` y `large`.</span><span class="sxs-lookup"><span data-stu-id="bf71c-116">Possible values are: `hidden`, `small`, `medium`, `wide`, `large`.</span></span>|
|<span data-ttu-id="bf71c-117">name</span><span class="sxs-lookup"><span data-stu-id="bf71c-117">name</span></span>|<span data-ttu-id="bf71c-118">String</span><span class="sxs-lookup"><span data-stu-id="bf71c-118">String</span></span>|<span data-ttu-id="bf71c-119">Representa el nombre descriptivo de una aplicación heredada de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span><span class="sxs-lookup"><span data-stu-id="bf71c-119">Represents the friendly name of an app Inherited from [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)</span></span>|
|<span data-ttu-id="bf71c-120">appUserModelId</span><span class="sxs-lookup"><span data-stu-id="bf71c-120">appUserModelId</span></span>|<span data-ttu-id="bf71c-121">String</span><span class="sxs-lookup"><span data-stu-id="bf71c-121">String</span></span>|<span data-ttu-id="bf71c-122">Esta es la única aplicación de usuario modelo de identificador (AUMID) que estará disponible para iniciar el uso en el modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="bf71c-122">This is the only Application User Model ID (AUMID) that will be available to launch use while in Kiosk Mode</span></span>|
|<span data-ttu-id="bf71c-123">appId</span><span class="sxs-lookup"><span data-stu-id="bf71c-123">appId</span></span>|<span data-ttu-id="bf71c-124">cadena</span><span class="sxs-lookup"><span data-stu-id="bf71c-124">String</span></span>|<span data-ttu-id="bf71c-125">Esto hace referencia a un App Intune que será destino para las mismas asignaciones de configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="bf71c-125">This references an Intune App that will be target to the same assignments as Kiosk configuration</span></span>|
|<span data-ttu-id="bf71c-126">containedAppId</span><span class="sxs-lookup"><span data-stu-id="bf71c-126">containedAppId</span></span>|<span data-ttu-id="bf71c-127">String</span><span class="sxs-lookup"><span data-stu-id="bf71c-127">String</span></span>|<span data-ttu-id="bf71c-128">Esto hace referencia a una aplicación contenida desde un App Intune</span><span class="sxs-lookup"><span data-stu-id="bf71c-128">This references an contained App from an Intune App</span></span>|

## <a name="relationships"></a><span data-ttu-id="bf71c-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bf71c-129">Relationships</span></span>
<span data-ttu-id="bf71c-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bf71c-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bf71c-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bf71c-131">JSON Representation</span></span>
<span data-ttu-id="bf71c-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bf71c-132">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskUWPApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskUWPApp",
  "startLayoutTileSize": "String",
  "name": "String",
  "appUserModelId": "String",
  "appId": "String",
  "containedAppId": "String"
}
```





