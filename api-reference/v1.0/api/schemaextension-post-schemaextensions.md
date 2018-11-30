---
title: Crear schemaExtensions
description: Crear una nueva definición de schemaExtension para extender a un tipo de recurso compatible.
ms.openlocfilehash: b66cdc9d589520bbdf3557c4d1ea791f75def984
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030017"
---
# <a name="create-schemaextension"></a>Crear schemaExtensions

Crear una nueva definición de [schemaExtension](../resources/schemaextension.md) para extender a un [tipo de recurso compatible](/graph/extensibility-overview#supported-resources).

Las extensiones de esquema permiten agregar datos personalizados fuertemente tipados a un recurso. La aplicación que crea una extensión de esquema es la propietaria de la aplicación. Dependiendo del [estado](/graph/extensibility-overview#schema-extensions-lifecycle) de la extensión, solamente el propietario de la aplicación puede actualizar o eliminar la extensión. 

Vea ejemplos de cómo [definir una extensión de esquema que describe un curso de aprendizaje](/graph/extensibility-schema-groups#2-register-a-schema-extension-definition-that-describes-a-training-course), utilice la definición de la extensión de esquema para [crear un nuevo grupo con los datos del curso de aprendizaje](/graph/extensibility-schema-groups#3-create-a-new-group-with-extended-data), y [agregue datos del curso de aprendizaje a un grupo existente](/graph/extensibility-schema-groups#4-add-update-or-remove-custom-data-in-an-existing-group).

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
POST /schemaExtensions
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [schemaExtension](../resources/schemaextension.md).

En la tabla siguiente se muestran las propiedades necesarias para crear una extensión de esquema.

| Parámetro | Tipo | Descripción|
|:---------------|:--------|:----------|
|description|String|Descripción de la extensión de esquema.|
|id|Cadena|Identificador único para la definición de la extensión de esquema. <br>Puede asignar un valor de dos maneras: <ul><li>Concatenar el nombre de uno de los dominios comprobados con un nombre para la extensión del esquema con el fin de formar una cadena única en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}. Por ejemplo: `contoso_mySchema`. NOTA: Solo se admiten los dominios comprobados bajo los siguientes dominios de primer nivel: `.com`, `.net`, `.gov`, `.edu` o `.org`. </li><li>Proporcionar un nombre de esquema y permitir a Microsoft Graph utilizar ese nombre de esquema para completar la asignación del **id.** en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Un ejemplo sería `extkvbmkofy_mySchema`.</li></ul>Una vez creada, esta propiedad no se puede modificar. |
|owner|String|(Opcional) El `appId` de la aplicación que es el propietario de la extensión del esquema. Esta propiedad se puede proporcionar en la creación, para establecer el propietario.  Si no se proporciona, entonces la aplicación de llamada `appId` se establecerá como la propietaria. Así, por ejemplo, si crea una nueva definición de extensión de esquema mediante el Probador de gráfico, **debe** proporcionar la propiedad owner. Una vez establecida, esta propiedad es de solo lectura y no se puede cambiar.|
|properties|Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)|La colección de tipos y nombres de propiedad que conforman la definición de la extensión de esquema.|
|targetTypes|Colección de cadenas|Conjunto de tipos de recursos de Microsoft Graph (compatibles con extensiones de esquema) a los que se puede aplicar la definición de extensión de esquema.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request-1"></a>Solicitud 1

El primer ejemplo se muestra mediante un nombre de dominio comprobado, `graphlearn`, y un nombre de esquema, `courses`, para formar una cadena única para la propiedad **id** de la definición de la extensión de esquema. La cadena única se basa en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.

En el cuerpo de la solicitud, proporcione la representación JSON del objeto [schemaExtension](../resources/schemaextension.md).
<!-- {
  "blockType": "request",
  "name": "create_schemaextension_from_schemaextensions_1"
}-->
```http
POST https://graph.microsoft.com/v1.0/schemaExtensions
Content-type: application/json

{
    "id":"graphlearn_courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "properties": [
        {
            "name": "courseId",
            "type": "Integer"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```

##### <a name="response-1"></a>Respuesta 1

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 420

{
    "id": "graphlearn_courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "status": "InDevelopment",
    "owner": "24d3b144-21ae-4080-943f-7067b395b913",
    "properties": [
        {
            "name": "courseId",
            "type": "String"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```

##### <a name="request-2"></a>Solicitud 2

El segundo ejemplo muestra la especificación de un nombre de esquema, `courses`, en la propiedad **id** de la solicitud, junto con la representación JSON del resto de las propiedades del objeto [schemaExtension](../resources/schemaextension.md). Microsoft Graph asignará y devolverá un valor de cadena único en la respuesta.

<!-- {
  "blockType": "request",
  "name": "create_schemaextension_from_schemaextensions_2"
}-->
```http
POST https://graph.microsoft.com/v1.0/schemaExtensions
Content-type: application/json

{
    "id":"courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "properties": [
        {
            "name": "courseId",
            "type": "Integer"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```

##### <a name="response-2"></a>Respuesta 2

La respuesta incluye una cadena única en la propiedad **id** que se basa en el nombre del esquema proporcionado en la solicitud, junto con el resto de la definición de esquema recién creada. El valor de **id** en la respuesta se basa en el formato, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán en una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 420

{
    "id": "extk9eruy7c_courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "status": "InDevelopment",
    "owner": "24d3b144-21ae-4080-943f-7067b395b913",
    "properties": [
        {
            "name": "courseId",
            "type": "String"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```


## <a name="see-also"></a>Consulte también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->