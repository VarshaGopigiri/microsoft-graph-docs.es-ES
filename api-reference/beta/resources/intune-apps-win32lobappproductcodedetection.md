---
title: tipo de recurso win32LobAppProductCodeDetection
description: Contiene las propiedades de código y la versión de producto para detectar una aplicación de Win32
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a3a461661d2b2a37cd7f4e9a37561ea682ea0e0f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812476"
---
# <a name="win32lobappproductcodedetection-resource-type"></a><span data-ttu-id="7d534-103">tipo de recurso win32LobAppProductCodeDetection</span><span class="sxs-lookup"><span data-stu-id="7d534-103">win32LobAppProductCodeDetection resource type</span></span>

> <span data-ttu-id="7d534-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d534-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d534-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d534-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7d534-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7d534-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7d534-107">Contiene las propiedades de código y la versión de producto para detectar una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="7d534-107">Contains product code and version properties to detect a Win32 App</span></span>

<span data-ttu-id="7d534-108">Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="7d534-108">Inherits from [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span></span>

## <a name="properties"></a><span data-ttu-id="7d534-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d534-109">Properties</span></span>
|<span data-ttu-id="7d534-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d534-110">Property</span></span>|<span data-ttu-id="7d534-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d534-111">Type</span></span>|<span data-ttu-id="7d534-112">Description</span><span class="sxs-lookup"><span data-stu-id="7d534-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7d534-113">productCode</span><span class="sxs-lookup"><span data-stu-id="7d534-113">productCode</span></span>|<span data-ttu-id="7d534-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d534-114">String</span></span>|<span data-ttu-id="7d534-115">El código de producto de aplicación de línea de negocio (LoB) de Win32.</span><span class="sxs-lookup"><span data-stu-id="7d534-115">The product code of Win32 Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="7d534-116">productVersionOperator</span><span class="sxs-lookup"><span data-stu-id="7d534-116">productVersionOperator</span></span>|[<span data-ttu-id="7d534-117">win32LobAppDetectionOperator</span><span class="sxs-lookup"><span data-stu-id="7d534-117">win32LobAppDetectionOperator</span></span>](../resources/intune-apps-win32lobappdetectionoperator.md)|<span data-ttu-id="7d534-118">El operador para detectar la versión del producto.</span><span class="sxs-lookup"><span data-stu-id="7d534-118">The operator to detect product version.</span></span> <span data-ttu-id="7d534-119">Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.</span><span class="sxs-lookup"><span data-stu-id="7d534-119">Possible values are: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.</span></span>|
|<span data-ttu-id="7d534-120">productVersion</span><span class="sxs-lookup"><span data-stu-id="7d534-120">productVersion</span></span>|<span data-ttu-id="7d534-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d534-121">String</span></span>|<span data-ttu-id="7d534-122">La versión del producto de aplicación de línea de negocio (LoB) de Win32.</span><span class="sxs-lookup"><span data-stu-id="7d534-122">The product version of Win32 Line of Business (LoB) app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7d534-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7d534-123">Relationships</span></span>
<span data-ttu-id="7d534-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7d534-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7d534-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7d534-125">JSON Representation</span></span>
<span data-ttu-id="7d534-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7d534-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppProductCodeDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppProductCodeDetection",
  "productCode": "String",
  "productVersionOperator": "String",
  "productVersion": "String"
}
```





