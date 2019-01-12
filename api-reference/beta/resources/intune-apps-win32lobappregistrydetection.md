---
title: tipo de recurso win32LobAppRegistryDetection
description: Contiene las propiedades del registro para detectar una aplicación de Win32
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 23362d7613d198bdd848205cbf20944e9a592f04
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923904"
---
# <a name="win32lobappregistrydetection-resource-type"></a><span data-ttu-id="824b7-103">tipo de recurso win32LobAppRegistryDetection</span><span class="sxs-lookup"><span data-stu-id="824b7-103">win32LobAppRegistryDetection resource type</span></span>

> <span data-ttu-id="824b7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="824b7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="824b7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="824b7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="824b7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="824b7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="824b7-107">Contiene las propiedades del registro para detectar una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="824b7-107">Contains registry properties to detect a Win32 App</span></span>

<span data-ttu-id="824b7-108">Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="824b7-108">Inherits from [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span></span>

## <a name="properties"></a><span data-ttu-id="824b7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="824b7-109">Properties</span></span>
|<span data-ttu-id="824b7-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="824b7-110">Property</span></span>|<span data-ttu-id="824b7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="824b7-111">Type</span></span>|<span data-ttu-id="824b7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="824b7-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="824b7-113">check32BitOn64System</span><span class="sxs-lookup"><span data-stu-id="824b7-113">check32BitOn64System</span></span>|<span data-ttu-id="824b7-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="824b7-114">Boolean</span></span>|<span data-ttu-id="824b7-115">Un valor que indica si esta ruta de acceso del registro para comprobar la aplicación de 32 bits en el sistema de 64 bits</span><span class="sxs-lookup"><span data-stu-id="824b7-115">A value indicating whether this registry path is for checking 32-bit app on 64-bit system</span></span>|
|<span data-ttu-id="824b7-116">ruta de acceso clave</span><span class="sxs-lookup"><span data-stu-id="824b7-116">keyPath</span></span>|<span data-ttu-id="824b7-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="824b7-117">String</span></span>|<span data-ttu-id="824b7-118">La ruta de la clave del registro para detectar la aplicación de línea de negocio (LoB) de Win32</span><span class="sxs-lookup"><span data-stu-id="824b7-118">The registry key path to detect Win32 Line of Business (LoB) app</span></span>|
|<span data-ttu-id="824b7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="824b7-119">valueName</span></span>|<span data-ttu-id="824b7-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="824b7-120">String</span></span>|<span data-ttu-id="824b7-121">El nombre del valor del registro</span><span class="sxs-lookup"><span data-stu-id="824b7-121">The registry value name</span></span>|
|<span data-ttu-id="824b7-122">tipo de detección</span><span class="sxs-lookup"><span data-stu-id="824b7-122">detectionType</span></span>|[<span data-ttu-id="824b7-123">win32LobAppRegistryDetectionType</span><span class="sxs-lookup"><span data-stu-id="824b7-123">win32LobAppRegistryDetectionType</span></span>](../resources/intune-apps-win32lobappregistrydetectiontype.md)|<span data-ttu-id="824b7-124">El tipo de detección de datos del registro.</span><span class="sxs-lookup"><span data-stu-id="824b7-124">The registry data detection type.</span></span> <span data-ttu-id="824b7-125">Los valores posibles son: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.</span><span class="sxs-lookup"><span data-stu-id="824b7-125">Possible values are: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.</span></span>|
|<span data-ttu-id="824b7-126">operator</span><span class="sxs-lookup"><span data-stu-id="824b7-126">operator</span></span>|[<span data-ttu-id="824b7-127">win32LobAppDetectionOperator</span><span class="sxs-lookup"><span data-stu-id="824b7-127">win32LobAppDetectionOperator</span></span>](../resources/intune-apps-win32lobappdetectionoperator.md)|<span data-ttu-id="824b7-128">El operador para la detección de datos del registro.</span><span class="sxs-lookup"><span data-stu-id="824b7-128">The operator for registry data detection.</span></span> <span data-ttu-id="824b7-129">Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.</span><span class="sxs-lookup"><span data-stu-id="824b7-129">Possible values are: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.</span></span>|
|<span data-ttu-id="824b7-130">detectionValue</span><span class="sxs-lookup"><span data-stu-id="824b7-130">detectionValue</span></span>|<span data-ttu-id="824b7-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="824b7-131">String</span></span>|<span data-ttu-id="824b7-132">El valor de detección del registro</span><span class="sxs-lookup"><span data-stu-id="824b7-132">The registry detection value</span></span>|

## <a name="relationships"></a><span data-ttu-id="824b7-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="824b7-133">Relationships</span></span>
<span data-ttu-id="824b7-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="824b7-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="824b7-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="824b7-135">JSON Representation</span></span>
<span data-ttu-id="824b7-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="824b7-136">Here is a JSON representation of the resource.</span></span>
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





