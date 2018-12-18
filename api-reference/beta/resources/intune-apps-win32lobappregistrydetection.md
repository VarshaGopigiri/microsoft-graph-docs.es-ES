---
title: tipo de recurso win32LobAppRegistryDetection
description: Contiene las propiedades del registro para detectar una aplicación de Win32
author: tfitzmac
ms.openlocfilehash: 5adeca1b569531d15657acc2a8960bab60580dc6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347743"
---
# <a name="win32lobappregistrydetection-resource-type"></a><span data-ttu-id="0947a-103">tipo de recurso win32LobAppRegistryDetection</span><span class="sxs-lookup"><span data-stu-id="0947a-103">win32LobAppRegistryDetection resource type</span></span>

> <span data-ttu-id="0947a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0947a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0947a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0947a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0947a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0947a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0947a-107">Contiene las propiedades del registro para detectar una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="0947a-107">Contains registry properties to detect a Win32 App</span></span>

<span data-ttu-id="0947a-108">Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="0947a-108">Inherits from [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span></span>

## <a name="properties"></a><span data-ttu-id="0947a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0947a-109">Properties</span></span>
|<span data-ttu-id="0947a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0947a-110">Property</span></span>|<span data-ttu-id="0947a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="0947a-111">Type</span></span>|<span data-ttu-id="0947a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0947a-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0947a-113">check32BitOn64System</span><span class="sxs-lookup"><span data-stu-id="0947a-113">check32BitOn64System</span></span>|<span data-ttu-id="0947a-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="0947a-114">Boolean</span></span>|<span data-ttu-id="0947a-115">Un valor que indica si esta ruta de acceso del registro para comprobar la aplicación de 32 bits en el sistema de 64 bits</span><span class="sxs-lookup"><span data-stu-id="0947a-115">A value indicating whether this registry path is for checking 32-bit app on 64-bit system</span></span>|
|<span data-ttu-id="0947a-116">ruta de acceso clave</span><span class="sxs-lookup"><span data-stu-id="0947a-116">keyPath</span></span>|<span data-ttu-id="0947a-117">String</span><span class="sxs-lookup"><span data-stu-id="0947a-117">String</span></span>|<span data-ttu-id="0947a-118">La ruta de la clave del registro para detectar la aplicación de línea de negocio (LoB) de Win32</span><span class="sxs-lookup"><span data-stu-id="0947a-118">The registry key path to detect Win32 Line of Business (LoB) app</span></span>|
|<span data-ttu-id="0947a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0947a-119">valueName</span></span>|<span data-ttu-id="0947a-120">String</span><span class="sxs-lookup"><span data-stu-id="0947a-120">String</span></span>|<span data-ttu-id="0947a-121">El nombre del valor del registro</span><span class="sxs-lookup"><span data-stu-id="0947a-121">The registry value name</span></span>|
|<span data-ttu-id="0947a-122">tipo de detección</span><span class="sxs-lookup"><span data-stu-id="0947a-122">detectionType</span></span>|[<span data-ttu-id="0947a-123">win32LobAppRegistryDetectionType</span><span class="sxs-lookup"><span data-stu-id="0947a-123">win32LobAppRegistryDetectionType</span></span>](../resources/intune-apps-win32lobappregistrydetectiontype.md)|<span data-ttu-id="0947a-124">El tipo de detección de datos del registro.</span><span class="sxs-lookup"><span data-stu-id="0947a-124">The registry data detection type.</span></span> <span data-ttu-id="0947a-125">Los valores posibles son: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.</span><span class="sxs-lookup"><span data-stu-id="0947a-125">Possible values are: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.</span></span>|
|<span data-ttu-id="0947a-126">operator</span><span class="sxs-lookup"><span data-stu-id="0947a-126">operator</span></span>|[<span data-ttu-id="0947a-127">win32LobAppDetectionOperator</span><span class="sxs-lookup"><span data-stu-id="0947a-127">win32LobAppDetectionOperator</span></span>](../resources/intune-apps-win32lobappdetectionoperator.md)|<span data-ttu-id="0947a-128">El operador para la detección de datos del registro.</span><span class="sxs-lookup"><span data-stu-id="0947a-128">The operator for registry data detection.</span></span> <span data-ttu-id="0947a-129">Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.</span><span class="sxs-lookup"><span data-stu-id="0947a-129">Possible values are: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.</span></span>|
|<span data-ttu-id="0947a-130">detectionValue</span><span class="sxs-lookup"><span data-stu-id="0947a-130">detectionValue</span></span>|<span data-ttu-id="0947a-131">String</span><span class="sxs-lookup"><span data-stu-id="0947a-131">String</span></span>|<span data-ttu-id="0947a-132">El valor de detección del registro</span><span class="sxs-lookup"><span data-stu-id="0947a-132">The registry detection value</span></span>|

## <a name="relationships"></a><span data-ttu-id="0947a-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0947a-133">Relationships</span></span>
<span data-ttu-id="0947a-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0947a-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0947a-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0947a-135">JSON Representation</span></span>
<span data-ttu-id="0947a-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0947a-136">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppRegistryDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppRegistryDetection",
  "check32BitOn64System": true,
  "keyPath": "String",
  "valueName": "String",
  "detectionType": "String",
  "operator": "String",
  "detectionValue": "String"
}
```





