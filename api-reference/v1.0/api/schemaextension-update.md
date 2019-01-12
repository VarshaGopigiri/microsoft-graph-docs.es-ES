---
title: Actualizar schemaExtensions
description: Actualice las propiedades de la definición del schemaExtension especificado.
localization_priority: Normal
author: dkershaw10
ms.openlocfilehash: 9f8bfc77ddcb3633160f76ce5d900e4ba09af1c9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960780"
---
# <a name="update-schemaextension"></a>Actualizar schemaExtensions

Actualice las propiedades de la definición del [schemaExtension](../resources/schemaextension.md) especificado.

La actualización se aplica a todos los recursos que se incluyen en la propiedad **targetTypes** de la extensión. Estos recursos se encuentran entre los [tipos de recurso admitidos](/graph/extensibility-overview#supported-resources).

Solo la aplicación que ha creado una extensión de esquema (la aplicación propietaria) puede realizar cambios para agregar elementos a la extensión cuando esta se encuentra en los estados **InDevelopment** o **Available**. Esto significa que la aplicación no puede quitar propiedades personalizadas o tipos de recurso de destino de la definición. No obstante, sí puede cambiar la descripción de la extensión.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```http
PATCH /schemaExtensions/{id}
```

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Content-Type   | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|description|String|Descripción de la extensión de esquema.|
|properties|Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)|La colección de nombres de propiedad y tipos que conforman la definición de la extensión de esquema. Solo se admiten cambios para agregar elementos. |
|status|Cadena|El estado del ciclo de vida de la extensión de esquema. El estado inicial después de su creación es **InDevelopment**. Transiciones de los Estados posibles son de **InDevelopment** a **disponible** y **disponible** para **ya no se utiliza**.|
|targetTypes|Colección string|Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema.  Solo se admiten cambios para agregar elementos.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_schemaextension"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/schemaExtensions/{id}
Content-type: application/json
Content-length: 201

{
  "properties": [
    {
      "name":"new-name-value",
      "type":"new-type-value"
    },
    {
      "name":"additional-name-value",
      "type":"additional-type-value"
    }
  ],
}
```

##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update schemaextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
