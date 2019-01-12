---
title: Tipo de recurso androidForWorkAppConfigurationSchemaItem
description: Elemento de configuración único dentro del esquema de configuración personalizada de la aplicación de Android for Work.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 7e8500df3065c68ae8ddc2ad85413aa4d31f8980
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923456"
---
# <a name="androidforworkappconfigurationschemaitem-resource-type"></a><span data-ttu-id="ee45a-103">Tipo de recurso androidForWorkAppConfigurationSchemaItem</span><span class="sxs-lookup"><span data-stu-id="ee45a-103">androidForWorkAppConfigurationSchemaItem resource type</span></span>

> <span data-ttu-id="ee45a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee45a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee45a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee45a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ee45a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ee45a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ee45a-107">Elemento de configuración único dentro del esquema de configuración personalizada de la aplicación de Android for Work.</span><span class="sxs-lookup"><span data-stu-id="ee45a-107">Single configuration item inside an Android for Work application's custom configuration schema.</span></span>
## <a name="properties"></a><span data-ttu-id="ee45a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee45a-108">Properties</span></span>
|<span data-ttu-id="ee45a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee45a-109">Property</span></span>|<span data-ttu-id="ee45a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee45a-110">Type</span></span>|<span data-ttu-id="ee45a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee45a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ee45a-112">schemaItemKey</span><span class="sxs-lookup"><span data-stu-id="ee45a-112">schemaItemKey</span></span>|<span data-ttu-id="ee45a-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee45a-113">String</span></span>|<span data-ttu-id="ee45a-114">La clave única que usa la aplicación para identificar el elemento</span><span class="sxs-lookup"><span data-stu-id="ee45a-114">Unique key the application uses to identify the item</span></span>|
|<span data-ttu-id="ee45a-115">displayName</span><span class="sxs-lookup"><span data-stu-id="ee45a-115">displayName</span></span>|<span data-ttu-id="ee45a-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee45a-116">String</span></span>|<span data-ttu-id="ee45a-117">Nombre legible</span><span class="sxs-lookup"><span data-stu-id="ee45a-117">Human readable name</span></span>|
|<span data-ttu-id="ee45a-118">description</span><span class="sxs-lookup"><span data-stu-id="ee45a-118">description</span></span>|<span data-ttu-id="ee45a-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee45a-119">String</span></span>|<span data-ttu-id="ee45a-120">Descripción de lo que controla el elemento dentro de la aplicación</span><span class="sxs-lookup"><span data-stu-id="ee45a-120">Description of what the item controls within the application</span></span>|
|<span data-ttu-id="ee45a-121">defaultBoolValue</span><span class="sxs-lookup"><span data-stu-id="ee45a-121">defaultBoolValue</span></span>|<span data-ttu-id="ee45a-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="ee45a-122">Boolean</span></span>|<span data-ttu-id="ee45a-123">Valor predeterminado para los elementos de tipo booleano, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee45a-123">Default value for boolean type items, if specified by the app developer</span></span>|
|<span data-ttu-id="ee45a-124">defaultIntValue</span><span class="sxs-lookup"><span data-stu-id="ee45a-124">defaultIntValue</span></span>|<span data-ttu-id="ee45a-125">Int32</span><span class="sxs-lookup"><span data-stu-id="ee45a-125">Int32</span></span>|<span data-ttu-id="ee45a-126">Valor predeterminado para los elementos de tipo entero, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee45a-126">Default value for integer type items, if specified by the app developer</span></span>|
|<span data-ttu-id="ee45a-127">defaultStringValue</span><span class="sxs-lookup"><span data-stu-id="ee45a-127">defaultStringValue</span></span>|<span data-ttu-id="ee45a-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee45a-128">String</span></span>|<span data-ttu-id="ee45a-129">Valor predeterminado para los elementos de tipo cadena, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee45a-129">Default value for string type items, if specified by the app developer</span></span>|
|<span data-ttu-id="ee45a-130">defaultStringArrayValue</span><span class="sxs-lookup"><span data-stu-id="ee45a-130">defaultStringArrayValue</span></span>|<span data-ttu-id="ee45a-131">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="ee45a-131">String collection</span></span>|<span data-ttu-id="ee45a-132">Valor predeterminado para los elementos de tipo matriz de cadenas, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee45a-132">Default value for string array type items, if specified by the app developer</span></span>|
|<span data-ttu-id="ee45a-133">dataType</span><span class="sxs-lookup"><span data-stu-id="ee45a-133">dataType</span></span>|[<span data-ttu-id="ee45a-134">androidForWorkAppConfigurationSchemaItemDataType</span><span class="sxs-lookup"><span data-stu-id="ee45a-134">androidForWorkAppConfigurationSchemaItemDataType</span></span>](../resources/intune-androidforwork-androidforworkappconfigurationschemaitemdatatype.md)|<span data-ttu-id="ee45a-135">El tipo de valor que se describe en este artículo.</span><span class="sxs-lookup"><span data-stu-id="ee45a-135">The type of value this item describes.</span></span> <span data-ttu-id="ee45a-136">Los valores posibles son: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray` y `hidden`.</span><span class="sxs-lookup"><span data-stu-id="ee45a-136">Possible values are: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray`, `hidden`.</span></span>|
|<span data-ttu-id="ee45a-137">selecciones</span><span class="sxs-lookup"><span data-stu-id="ee45a-137">selections</span></span>|<span data-ttu-id="ee45a-138">Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="ee45a-138">[keyValuePair](../resources/intune-shared-keyvaluepair.md) collection</span></span>|<span data-ttu-id="ee45a-139">Lista de los pares nombre-valor legibles para los valores válidos que se pueden establecer para este elemento (solo elementos de selección de opciones múltiples)</span><span class="sxs-lookup"><span data-stu-id="ee45a-139">List of human readable name/value pairs for the valid values that can be set for this item (Choice and Multiselect items only)</span></span>|

## <a name="relationships"></a><span data-ttu-id="ee45a-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ee45a-140">Relationships</span></span>
<span data-ttu-id="ee45a-141">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ee45a-141">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ee45a-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee45a-142">JSON Representation</span></span>
<span data-ttu-id="ee45a-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ee45a-143">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchemaItem",
  "schemaItemKey": "String",
  "displayName": "String",
  "description": "String",
  "defaultBoolValue": true,
  "defaultIntValue": 1024,
  "defaultStringValue": "String",
  "defaultStringArrayValue": [
    "String"
  ],
  "dataType": "String",
  "selections": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ]
}
```





