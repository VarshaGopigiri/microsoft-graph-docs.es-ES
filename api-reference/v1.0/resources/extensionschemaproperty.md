---
title: Tipo de recurso extensionSchemaProperty
description: Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición schemaExtension.
localization_priority: Normal
ms.openlocfilehash: 384f60c323ca6c6fb23d2f4811a6d2cb918bf844
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880573"
---
# <a name="extensionschemaproperty-resource-type"></a>Tipo de recurso extensionSchemaProperty

Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición [schemaExtension](schemaextension.md).


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|Cadena| El nombre de la propiedad fuertemente tipada definida como parte de una extensión de esquema.|
|tipo|String| Tipo de la propiedad que se define como parte de una extensión de esquema.  Los valores permitidos son *Binary, Boolean, DateTime, Integer* y *String*.  Consulte la tabla siguiente para obtener más detalles.|

#### <a name="supported-property-data-types"></a>Tipos de datos de propiedad admitidos 
Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:

| Tipo de propiedad | Observaciones |
|-------------|------------|
| Binario | Máximo de 256 bytes. |
| Boolean | No se admite para contactos, mensajes, eventos y publicaciones. |
| DateTime | Debe especificarse en el formato ISO 8601. Se almacenarán en UTC. |
| Integer | Valor de 32 bits. No se admite para contactos, mensajes, eventos y publicaciones. |
| String | 256 caracteres como máximo. |

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
