---
title: tipo de recurso androidManagedStoreAppConfigurationSchemaItem
description: Elemento de configuración único dentro de esquema de configuración personalizada de la aplicación Android.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 08c73a177e176ddf82ae64c4eb6b8efd0c662c97
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927971"
---
# <a name="androidmanagedstoreappconfigurationschemaitem-resource-type"></a>tipo de recurso androidManagedStoreAppConfigurationSchemaItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Elemento de configuración único dentro de esquema de configuración personalizada de la aplicación Android.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|schemaItemKey|Cadena|La clave única que usa la aplicación para identificar el elemento|
|displayName|Cadena|Nombre legible|
|description|Cadena|Descripción de lo que controla el elemento dentro de la aplicación|
|defaultBoolValue|Booleano|Valor predeterminado para los elementos de tipo booleano, si lo especifica el desarrollador de aplicaciones|
|defaultIntValue|Int32|Valor predeterminado para los elementos de tipo entero, si lo especifica el desarrollador de aplicaciones|
|defaultStringValue|Cadena|Valor predeterminado para los elementos de tipo cadena, si lo especifica el desarrollador de aplicaciones|
|defaultStringArrayValue|Colección de cadenas|Valor predeterminado para los elementos de tipo matriz de cadenas, si lo especifica el desarrollador de aplicaciones|
|dataType|[androidManagedStoreAppConfigurationSchemaItemDataType](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschemaitemdatatype.md)|El tipo de valor que se describe en este artículo. Los valores posibles son: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray` y `hidden`.|
|selecciones|Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)|Lista de los pares nombre-valor legibles para los valores válidos que se pueden establecer para este elemento (solo elementos de selección de opciones múltiples)|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidManagedStoreAppConfigurationSchemaItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidManagedStoreAppConfigurationSchemaItem",
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





