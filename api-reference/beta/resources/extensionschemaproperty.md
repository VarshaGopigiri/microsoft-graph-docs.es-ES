---
title: Tipo de recurso extensionSchemaProperty
description: Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición schemaExtension.
localization_priority: Normal
ms.openlocfilehash: 44769bab4a4f4b40a80d896bed2311554ea5e8ad
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889862"
---
# <a name="extensionschemaproperty-resource-type"></a>Tipo de recurso extensionSchemaProperty

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición [schemaExtension](schemaextension.md).


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|Cadena| El nombre de la propiedad fuertemente tipada definido como parte de una extensión de esquema.|
|type|String| Tipo de la propiedad que se define como parte de una extensión de esquema.  Los valores permitidos son *Binary, Boolean, DateTime, Integer* y *String*.  Consulte la tabla siguiente para obtener más detalles.|

#### <a name="supported-property-data-types"></a>Tipos de datos de propiedad admitidos 
Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:

| Tipo de propiedad | Observaciones |
|-------------|------------|
| Binario | Máximo de 256 bytes. |
| Booleano | No se admite para los mensajes, eventos y publicaciones. |
| DateTime | Debe especificarse en el formato ISO 8601. Se almacenarán en UTC. |
| Entero | Valor de 32 bits. No se admite para los mensajes, eventos y publicaciones. |
| Cadena | 256 caracteres como máximo. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.extensionSchemaProperty"
}-->

```json
{
  "name": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "extensionSchemaProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
