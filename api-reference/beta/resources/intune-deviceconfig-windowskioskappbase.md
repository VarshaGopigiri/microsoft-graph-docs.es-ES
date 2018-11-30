---
title: tipo de recurso windowsKioskAppBase
description: La clase base para un tipo de aplicaciones
ms.openlocfilehash: bbd2a961e86e698ff0b9a98401927c518beafe49
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085478"
---
# <a name="windowskioskappbase-resource-type"></a><span data-ttu-id="47168-103">tipo de recurso windowsKioskAppBase</span><span class="sxs-lookup"><span data-stu-id="47168-103">windowsKioskAppBase resource type</span></span>

> <span data-ttu-id="47168-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="47168-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="47168-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="47168-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="47168-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="47168-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="47168-107">La clase base para un tipo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="47168-107">The base class for a type of apps</span></span>
## <a name="properties"></a><span data-ttu-id="47168-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47168-108">Properties</span></span>
|<span data-ttu-id="47168-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="47168-109">Property</span></span>|<span data-ttu-id="47168-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="47168-110">Type</span></span>|<span data-ttu-id="47168-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="47168-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="47168-112">startLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="47168-112">startLayoutTileSize</span></span>|[<span data-ttu-id="47168-113">windowsAppStartLayoutTileSize</span><span class="sxs-lookup"><span data-stu-id="47168-113">windowsAppStartLayoutTileSize</span></span>](../resources/intune-deviceconfig-windowsappstartlayouttilesize.md)|<span data-ttu-id="47168-114">El tamaño del icono de aplicación para el diseño de inicio.</span><span class="sxs-lookup"><span data-stu-id="47168-114">The app tile size for the start layout.</span></span> <span data-ttu-id="47168-115">Los valores posibles son: `hidden`, `small`, `medium`, `wide` y `large`.</span><span class="sxs-lookup"><span data-stu-id="47168-115">Possible values are: `hidden`, `small`, `medium`, `wide`, `large`.</span></span>|
|<span data-ttu-id="47168-116">name</span><span class="sxs-lookup"><span data-stu-id="47168-116">name</span></span>|<span data-ttu-id="47168-117">String</span><span class="sxs-lookup"><span data-stu-id="47168-117">String</span></span>|<span data-ttu-id="47168-118">Representa el nombre descriptivo de una aplicación</span><span class="sxs-lookup"><span data-stu-id="47168-118">Represents the friendly name of an app</span></span>|

## <a name="relationships"></a><span data-ttu-id="47168-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="47168-119">Relationships</span></span>
<span data-ttu-id="47168-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="47168-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="47168-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="47168-121">JSON Representation</span></span>
<span data-ttu-id="47168-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="47168-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskAppBase"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskAppBase",
  "startLayoutTileSize": "String",
  "name": "String"
}
```





