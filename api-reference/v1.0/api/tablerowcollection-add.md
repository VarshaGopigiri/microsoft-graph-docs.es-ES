---
title: 'TableRowCollection: add'
description: 'Agrega filas al final de la tabla. Tenga en cuenta que la API puede aceptar varios datos de las filas con esta API. Adición de una fila a la vez, se podría producir una degradación del rendimiento. El enfoque recomendado sería por lotes las filas juntos en una única llamada en lugar de realizar la inserción de fila única. Para obtener mejores resultados, recopilar las filas que se va a insertar en el lado de la aplicación y llevar a cabo las filas único Agregar operación. Experimente con el número de filas para determinar el número de filas que se use en la llamada a la API único ideal. '
ms.openlocfilehash: fc2b89a25ade4b9d85844716370d95d52689de9d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030119"
---
# <a name="tablerowcollection-add"></a>TableRowCollection: add

Agrega filas al final de la tabla. Tenga en cuenta que la API puede aceptar varios datos de las filas con esta API. Adición de una fila a la vez, se podría producir una degradación del rendimiento. El enfoque recomendado sería por lotes las filas juntos en una única llamada en lugar de realizar la inserción de fila única. Para obtener mejores resultados, recopilar las filas que se va a insertar en el lado de la aplicación y llevar a cabo las filas único Agregar operación. Experimente con el número de filas para determinar el número de filas que se use en la llamada a la API único ideal. 

## <a name="error-handling"></a>Control de errores

En ocasiones, esta solicitud puede recibir el error HTTP 504. La respuesta adecuada a este error es repetir la solicitud.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/add

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Workbook-Session-Id  | Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|index|Int32|Opcional. Especifica la posición relativa de la nueva fila. Si es null, se produce la adición al final. Las filas situadas debajo de la fila insertada se desplazan hacia abajo. Indizado con cero.|
|values|Json|Opcional. Matriz bidimensional de valores sin formato de la fila de la tabla.|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookTableRow](../resources/tablerow.md) objeto en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
En este ejemplo se insertan dos filas de datos al final de la tabla. 

##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "tablerowcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows/add
Content-type: application/json
Content-length: 51

{
  "index": 5,
  "values": [
    [1, 2, 3],
    [4, 5, 6]
  ]
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRowCollection: add",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/api/tablerowcollection-add.md/tablerowcollection_add/values:
      Inconsistent types between parameter (Collection) and table (None)",
    "Error: /api-reference/v1.0/api/tablerowcollection-add.md/tablerowcollection_add/values:
      Type mismatch between example and table. Parameter name: values; example type (Collection(Collection)) is a collection, while the table description type (microsoft.graph.Json) is not."
  ],
  "tocPath": ""
}-->
