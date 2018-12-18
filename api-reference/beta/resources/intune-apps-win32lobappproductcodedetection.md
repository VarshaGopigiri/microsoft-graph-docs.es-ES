---
title: tipo de recurso win32LobAppProductCodeDetection
description: Contiene las propiedades de código y la versión de producto para detectar una aplicación de Win32
author: tfitzmac
ms.openlocfilehash: d66dab5a43a11c480e0e30f70eb8aecbe47e1fa7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353987"
---
# <a name="win32lobappproductcodedetection-resource-type"></a><span data-ttu-id="8d4c0-103">tipo de recurso win32LobAppProductCodeDetection</span><span class="sxs-lookup"><span data-stu-id="8d4c0-103">win32LobAppProductCodeDetection resource type</span></span>

> <span data-ttu-id="8d4c0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d4c0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8d4c0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d4c0-107">Contiene las propiedades de código y la versión de producto para detectar una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="8d4c0-107">Contains product code and version properties to detect a Win32 App</span></span>

<span data-ttu-id="8d4c0-108">Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="8d4c0-108">Inherits from [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8d4c0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d4c0-109">Properties</span></span>
|<span data-ttu-id="8d4c0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d4c0-110">Property</span></span>|<span data-ttu-id="8d4c0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d4c0-111">Type</span></span>|<span data-ttu-id="8d4c0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d4c0-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d4c0-113">productCode</span><span class="sxs-lookup"><span data-stu-id="8d4c0-113">productCode</span></span>|<span data-ttu-id="8d4c0-114">String</span><span class="sxs-lookup"><span data-stu-id="8d4c0-114">String</span></span>|<span data-ttu-id="8d4c0-115">El código de producto de aplicación de línea de negocio (LoB) de Win32.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-115">The product code of Win32 Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="8d4c0-116">productVersionOperator</span><span class="sxs-lookup"><span data-stu-id="8d4c0-116">productVersionOperator</span></span>|[<span data-ttu-id="8d4c0-117">win32LobAppDetectionOperator</span><span class="sxs-lookup"><span data-stu-id="8d4c0-117">win32LobAppDetectionOperator</span></span>](../resources/intune-apps-win32lobappdetectionoperator.md)|<span data-ttu-id="8d4c0-118">El operador para detectar la versión del producto.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-118">The operator to detect product version.</span></span> <span data-ttu-id="8d4c0-119">Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-119">Possible values are: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.</span></span>|
|<span data-ttu-id="8d4c0-120">productVersion</span><span class="sxs-lookup"><span data-stu-id="8d4c0-120">productVersion</span></span>|<span data-ttu-id="8d4c0-121">String</span><span class="sxs-lookup"><span data-stu-id="8d4c0-121">String</span></span>|<span data-ttu-id="8d4c0-122">La versión del producto de aplicación de línea de negocio (LoB) de Win32.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-122">The product version of Win32 Line of Business (LoB) app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d4c0-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d4c0-123">Relationships</span></span>
<span data-ttu-id="8d4c0-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d4c0-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d4c0-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d4c0-125">JSON Representation</span></span>
<span data-ttu-id="8d4c0-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d4c0-126">Here is a JSON representation of the resource.</span></span>
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





