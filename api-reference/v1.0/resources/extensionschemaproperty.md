---
title: Tipo de recurso extensionSchemaProperty
description: Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición schemaExtension.
ms.openlocfilehash: 1ea2fca1812765aab49d548dd3cd3ed0575e30aa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029246"
---
# <a name="extensionschemaproperty-resource-type"></a>Tipo de recurso extensionSchemaProperty

Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición [schemaExtension](schemaextension.md).


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|String| El nombre de la propiedad fuertemente tipada definida como parte de una extensión de esquema.|
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
