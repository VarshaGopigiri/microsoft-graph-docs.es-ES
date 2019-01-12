---
title: Crear tabla
description: Use esta API para crear un objeto Table.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: b402a047165a03b2631c0045041e1f50a95de710
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984993"
---
# <a name="create-table"></a>Crear tabla

Use esta API para crear un objeto Table.
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
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Workbook-Session-Id  | Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro           | Tipo      |Descripción|
|:---------------|:----------|:----------|
| Dirección  | string| Dirección de intervalo. Si llama a esta API desde la ruta de acceso `worksheets/{id or name}/tables/add`, no tiene que proporcionar el prefijo del nombre de hoja en la dirección. En cambio, si la llama desde la ruta de acceso `workbook/tables/add`, deberá proporcionar el nombre de la hoja en la que se debe crear la tabla (ejemplo: `sheet1!A1:D4`)|
| hasHeaders  | boolean|Valor booleano que indica si el intervalo tiene etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará de forma automática el encabezado desplazando los datos hacia abajo una fila.|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `201 Created` código de respuesta y [WorkbookTable](../resources/table.md) objeto en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_table_from_worksheet"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/tables/{id}/add
Content-type: application/json
Content-length: 109

{
  "address": "A1:D8",
  "hasHeaders": false
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTable"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 109

{
  "id": "99",
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Table",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
