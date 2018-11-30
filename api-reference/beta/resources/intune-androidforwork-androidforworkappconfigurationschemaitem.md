---
title: Tipo de recurso androidForWorkAppConfigurationSchemaItem
description: Elemento de configuración único dentro del esquema de configuración personalizada de la aplicación de Android for Work.
ms.openlocfilehash: 74f75eb57f6e7fc667499ef69f887c89d5e8a414
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083772"
---
# <a name="androidforworkappconfigurationschemaitem-resource-type"></a><span data-ttu-id="5be89-103">Tipo de recurso androidForWorkAppConfigurationSchemaItem</span><span class="sxs-lookup"><span data-stu-id="5be89-103">androidForWorkAppConfigurationSchemaItem resource type</span></span>

> <span data-ttu-id="5be89-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5be89-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5be89-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5be89-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5be89-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5be89-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5be89-107">Elemento de configuración único dentro del esquema de configuración personalizada de la aplicación de Android for Work.</span><span class="sxs-lookup"><span data-stu-id="5be89-107">Single configuration item inside an Android for Work application's custom configuration schema.</span></span>
## <a name="properties"></a><span data-ttu-id="5be89-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5be89-108">Properties</span></span>
|<span data-ttu-id="5be89-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5be89-109">Property</span></span>|<span data-ttu-id="5be89-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5be89-110">Type</span></span>|<span data-ttu-id="5be89-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5be89-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5be89-112">schemaItemKey</span><span class="sxs-lookup"><span data-stu-id="5be89-112">schemaItemKey</span></span>|<span data-ttu-id="5be89-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="5be89-113">String</span></span>|<span data-ttu-id="5be89-114">La clave única que usa la aplicación para identificar el elemento</span><span class="sxs-lookup"><span data-stu-id="5be89-114">Unique key the application uses to identify the item</span></span>|
|<span data-ttu-id="5be89-115">displayName</span><span class="sxs-lookup"><span data-stu-id="5be89-115">displayName</span></span>|<span data-ttu-id="5be89-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="5be89-116">String</span></span>|<span data-ttu-id="5be89-117">Nombre legible</span><span class="sxs-lookup"><span data-stu-id="5be89-117">Human readable name</span></span>|
|<span data-ttu-id="5be89-118">description</span><span class="sxs-lookup"><span data-stu-id="5be89-118">description</span></span>|<span data-ttu-id="5be89-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="5be89-119">String</span></span>|<span data-ttu-id="5be89-120">Descripción de lo que controla el elemento dentro de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5be89-120">Description of what the item controls within the application</span></span>|
|<span data-ttu-id="5be89-121">defaultBoolValue</span><span class="sxs-lookup"><span data-stu-id="5be89-121">defaultBoolValue</span></span>|<span data-ttu-id="5be89-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="5be89-122">Boolean</span></span>|<span data-ttu-id="5be89-123">Valor predeterminado para los elementos de tipo booleano, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5be89-123">Default value for boolean type items, if specified by the app developer</span></span>|
|<span data-ttu-id="5be89-124">defaultIntValue</span><span class="sxs-lookup"><span data-stu-id="5be89-124">defaultIntValue</span></span>|<span data-ttu-id="5be89-125">Int32</span><span class="sxs-lookup"><span data-stu-id="5be89-125">Int32</span></span>|<span data-ttu-id="5be89-126">Valor predeterminado para los elementos de tipo entero, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5be89-126">Default value for integer type items, if specified by the app developer</span></span>|
|<span data-ttu-id="5be89-127">defaultStringValue</span><span class="sxs-lookup"><span data-stu-id="5be89-127">defaultStringValue</span></span>|<span data-ttu-id="5be89-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="5be89-128">String</span></span>|<span data-ttu-id="5be89-129">Valor predeterminado para los elementos de tipo cadena, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5be89-129">Default value for string type items, if specified by the app developer</span></span>|
|<span data-ttu-id="5be89-130">defaultStringArrayValue</span><span class="sxs-lookup"><span data-stu-id="5be89-130">defaultStringArrayValue</span></span>|<span data-ttu-id="5be89-131">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="5be89-131">String collection</span></span>|<span data-ttu-id="5be89-132">Valor predeterminado para los elementos de tipo matriz de cadenas, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5be89-132">Default value for string array type items, if specified by the app developer</span></span>|
|<span data-ttu-id="5be89-133">dataType</span><span class="sxs-lookup"><span data-stu-id="5be89-133">dataType</span></span>|[<span data-ttu-id="5be89-134">androidForWorkAppConfigurationSchemaItemDataType</span><span class="sxs-lookup"><span data-stu-id="5be89-134">androidForWorkAppConfigurationSchemaItemDataType</span></span>](../resources/intune-androidforwork-androidforworkappconfigurationschemaitemdatatype.md)|<span data-ttu-id="5be89-135">El tipo de valor que se describe en este artículo.</span><span class="sxs-lookup"><span data-stu-id="5be89-135">The type of value this item describes.</span></span> <span data-ttu-id="5be89-136">Los valores posibles son: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray` y `hidden`.</span><span class="sxs-lookup"><span data-stu-id="5be89-136">Possible values are: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray`, `hidden`.</span></span>|
|<span data-ttu-id="5be89-137">selecciones</span><span class="sxs-lookup"><span data-stu-id="5be89-137">selections</span></span>|<span data-ttu-id="5be89-138">Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="5be89-138">[keyValuePair](../resources/intune-shared-keyvaluepair.md) collection</span></span>|<span data-ttu-id="5be89-139">Lista de los pares nombre-valor legibles para los valores válidos que se pueden establecer para este elemento (solo elementos de selección de opciones múltiples)</span><span class="sxs-lookup"><span data-stu-id="5be89-139">List of human readable name/value pairs for the valid values that can be set for this item (Choice and Multiselect items only)</span></span>|

## <a name="relationships"></a><span data-ttu-id="5be89-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5be89-140">Relationships</span></span>
<span data-ttu-id="5be89-141">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5be89-141">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5be89-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5be89-142">JSON Representation</span></span>
<span data-ttu-id="5be89-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5be89-143">Here is a JSON representation of the resource.</span></span>
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





