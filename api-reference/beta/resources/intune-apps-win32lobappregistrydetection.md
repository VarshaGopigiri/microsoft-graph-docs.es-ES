---
title: tipo de recurso win32LobAppRegistryDetection
description: Contiene las propiedades del registro para detectar una aplicación de Win32
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: faccc030a9f15b511af4123c94687c904e60ff10
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867140"
---
# <a name="win32lobappregistrydetection-resource-type"></a><span data-ttu-id="ab5c5-103">tipo de recurso win32LobAppRegistryDetection</span><span class="sxs-lookup"><span data-stu-id="ab5c5-103">win32LobAppRegistryDetection resource type</span></span>

> <span data-ttu-id="ab5c5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab5c5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ab5c5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab5c5-107">Contiene las propiedades del registro para detectar una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="ab5c5-107">Contains registry properties to detect a Win32 App</span></span>

<span data-ttu-id="ab5c5-108">Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="ab5c5-108">Inherits from [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ab5c5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab5c5-109">Properties</span></span>
|<span data-ttu-id="ab5c5-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab5c5-110">Property</span></span>|<span data-ttu-id="ab5c5-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab5c5-111">Type</span></span>|<span data-ttu-id="ab5c5-112">Description</span><span class="sxs-lookup"><span data-stu-id="ab5c5-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab5c5-113">check32BitOn64System</span><span class="sxs-lookup"><span data-stu-id="ab5c5-113">check32BitOn64System</span></span>|<span data-ttu-id="ab5c5-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab5c5-114">Boolean</span></span>|<span data-ttu-id="ab5c5-115">Un valor que indica si esta ruta de acceso del registro para comprobar la aplicación de 32 bits en el sistema de 64 bits</span><span class="sxs-lookup"><span data-stu-id="ab5c5-115">A value indicating whether this registry path is for checking 32-bit app on 64-bit system</span></span>|
|<span data-ttu-id="ab5c5-116">ruta de acceso clave</span><span class="sxs-lookup"><span data-stu-id="ab5c5-116">keyPath</span></span>|<span data-ttu-id="ab5c5-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab5c5-117">String</span></span>|<span data-ttu-id="ab5c5-118">La ruta de la clave del registro para detectar la aplicación de línea de negocio (LoB) de Win32</span><span class="sxs-lookup"><span data-stu-id="ab5c5-118">The registry key path to detect Win32 Line of Business (LoB) app</span></span>|
|<span data-ttu-id="ab5c5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ab5c5-119">valueName</span></span>|<span data-ttu-id="ab5c5-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab5c5-120">String</span></span>|<span data-ttu-id="ab5c5-121">El nombre del valor del registro</span><span class="sxs-lookup"><span data-stu-id="ab5c5-121">The registry value name</span></span>|
|<span data-ttu-id="ab5c5-122">tipo de detección</span><span class="sxs-lookup"><span data-stu-id="ab5c5-122">detectionType</span></span>|[<span data-ttu-id="ab5c5-123">win32LobAppRegistryDetectionType</span><span class="sxs-lookup"><span data-stu-id="ab5c5-123">win32LobAppRegistryDetectionType</span></span>](../resources/intune-apps-win32lobappregistrydetectiontype.md)|<span data-ttu-id="ab5c5-124">El tipo de detección de datos del registro.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-124">The registry data detection type.</span></span> <span data-ttu-id="ab5c5-125">Los valores posibles son: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-125">Possible values are: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.</span></span>|
|<span data-ttu-id="ab5c5-126">operator</span><span class="sxs-lookup"><span data-stu-id="ab5c5-126">operator</span></span>|[<span data-ttu-id="ab5c5-127">win32LobAppDetectionOperator</span><span class="sxs-lookup"><span data-stu-id="ab5c5-127">win32LobAppDetectionOperator</span></span>](../resources/intune-apps-win32lobappdetectionoperator.md)|<span data-ttu-id="ab5c5-128">El operador para la detección de datos del registro.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-128">The operator for registry data detection.</span></span> <span data-ttu-id="ab5c5-129">Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-129">Possible values are: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.</span></span>|
|<span data-ttu-id="ab5c5-130">detectionValue</span><span class="sxs-lookup"><span data-stu-id="ab5c5-130">detectionValue</span></span>|<span data-ttu-id="ab5c5-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab5c5-131">String</span></span>|<span data-ttu-id="ab5c5-132">El valor de detección del registro</span><span class="sxs-lookup"><span data-stu-id="ab5c5-132">The registry detection value</span></span>|

## <a name="relationships"></a><span data-ttu-id="ab5c5-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ab5c5-133">Relationships</span></span>
<span data-ttu-id="ab5c5-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ab5c5-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ab5c5-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab5c5-135">JSON Representation</span></span>
<span data-ttu-id="ab5c5-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ab5c5-136">Here is a JSON representation of the resource.</span></span>
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





