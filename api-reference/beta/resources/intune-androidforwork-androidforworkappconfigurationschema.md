---
title: Tipo de recurso androidForWorkAppConfigurationSchema
description: Esquema que describe la configuración personalizada de una aplicación de Android for Work.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 48b153fa23e1ca72918bf6651c2948978c05d46b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955936"
---
# <a name="androidforworkappconfigurationschema-resource-type"></a>Tipo de recurso androidForWorkAppConfigurationSchema

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esquema que describe la configuración personalizada de una aplicación de Android for Work.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidForWorkAppConfigurationSchemas](../api/intune-androidforwork-androidforworkappconfigurationschema-list.md)|Colección [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md)|Enumere las propiedades y las relaciones de los objetos [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).|
|[Obtener androidForWorkAppConfigurationSchema](../api/intune-androidforwork-androidforworkappconfigurationschema-get.md)|[androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md)|Lea las propiedades y las relaciones del objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).|
|[Crear androidForWorkAppConfigurationSchema](../api/intune-androidforwork-androidforworkappconfigurationschema-create.md)|[androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md)|Cree un objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).|
|[Eliminar androidForWorkAppConfigurationSchema](../api/intune-androidforwork-androidforworkappconfigurationschema-delete.md)|Ninguna|Elimina un [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md)|
|[Actualizar androidForWorkAppConfigurationSchema](../api/intune-androidforwork-androidforworkappconfigurationschema-update.md)|[androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md)|Actualice las propiedades de un objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad a la que corresponde el esquema del nombre del paquete Android para la aplicación|
|exampleJson|Binario|Matriz de bytes codificada UTF8 que contiene la cadena JSON de ejemplo conforme a este esquema que muestra cómo configurar los ajustes de esta aplicación|
|schemaItems|Colección [androidForWorkAppConfigurationSchemaItem](../resources/intune-androidforwork-androidforworkappconfigurationschemaitem.md)|Colección de elementos donde cada uno representa una opción de configuración con nombre en el esquema|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchema"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchema",
  "id": "String (identifier)",
  "exampleJson": "binary",
  "schemaItems": [
    {
      "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem",
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
  ]
}
```





