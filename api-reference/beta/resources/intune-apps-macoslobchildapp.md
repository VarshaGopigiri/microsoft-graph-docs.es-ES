---
title: tipo de recurso macOSLobChildApp
description: Contiene las propiedades de la aplicación de LOB de Mac OS en un paquete de agrupación
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 43f207bb2cebccdd01c791694674c6fbf96b631f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954235"
---
# <a name="macoslobchildapp-resource-type"></a><span data-ttu-id="4a088-103">tipo de recurso macOSLobChildApp</span><span class="sxs-lookup"><span data-stu-id="4a088-103">macOSLobChildApp resource type</span></span>

> <span data-ttu-id="4a088-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a088-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a088-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a088-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4a088-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4a088-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4a088-107">Contiene las propiedades de la aplicación de LOB de Mac OS en un paquete de agrupación</span><span class="sxs-lookup"><span data-stu-id="4a088-107">Contains properties the MacOS LOB App in a bundle package</span></span>
## <a name="properties"></a><span data-ttu-id="4a088-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a088-108">Properties</span></span>
|<span data-ttu-id="4a088-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a088-109">Property</span></span>|<span data-ttu-id="4a088-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a088-110">Type</span></span>|<span data-ttu-id="4a088-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a088-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a088-112">bundleId</span><span class="sxs-lookup"><span data-stu-id="4a088-112">bundleId</span></span>|<span data-ttu-id="4a088-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="4a088-113">String</span></span>|<span data-ttu-id="4a088-114">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="4a088-114">The Identity Name.</span></span>|
|<span data-ttu-id="4a088-115">buildNumber</span><span class="sxs-lookup"><span data-stu-id="4a088-115">buildNumber</span></span>|<span data-ttu-id="4a088-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="4a088-116">String</span></span>|<span data-ttu-id="4a088-117">El número de compilación de línea de Mac OS de aplicación de negocio (LoB).</span><span class="sxs-lookup"><span data-stu-id="4a088-117">The build number of MacOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="4a088-118">versionNumber</span><span class="sxs-lookup"><span data-stu-id="4a088-118">versionNumber</span></span>|<span data-ttu-id="4a088-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="4a088-119">String</span></span>|<span data-ttu-id="4a088-120">El número de versión de línea de Mac OS de aplicación de negocio (LoB).</span><span class="sxs-lookup"><span data-stu-id="4a088-120">The version number of MacOS Line of Business (LoB) app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4a088-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4a088-121">Relationships</span></span>
<span data-ttu-id="4a088-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4a088-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4a088-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a088-123">JSON Representation</span></span>
<span data-ttu-id="4a088-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4a088-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSLobChildApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSLobChildApp",
  "bundleId": "String",
  "buildNumber": "String",
  "versionNumber": "String"
}
```





