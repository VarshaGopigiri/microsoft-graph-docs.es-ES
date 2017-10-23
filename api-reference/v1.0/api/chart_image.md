# <a name="chart-image"></a>Chart: Image

Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|height|número|Opcional. Alto deseado de la imagen resultante.|
|width|número|Opcional. Ancho deseado de la imagen resultante.|
|fittingMode|string|Opcional. Método usado para escalar el gráfico a las dimensiones especificadas (si se han establecido el alto y el ancho)".  Valores posibles: `Fit`, `FitAndCenter`, `Fill`.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la cadena de imagen en base 64 en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')
Content-type: application/json
Content-length: 77

{
  "height": {
  },
  "width": {
  },
  "fittingMode": "fittingMode-value"
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 3

{
"value" : "base-64 chart image string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart: Image",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
