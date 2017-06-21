# <a name="update-chartdatalabels"></a>Actualizar chartdatalabels

Actualiza las propiedades del objeto chartdatalabels.
## <a name="prerequisites"></a>Requisitos previos
Se requieren los siguientes **ámbitos** para ejecutar esta API: 

    * Files.ReadWrite

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/datalabels
```
## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales
| Nombre       | Descripción|
|:-----------|:-----------|
| Authorization  | {token} de portador. Necesario. |


## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|position|string|Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.|
|separator|string|Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.|
|showBubbleSize|boolean|Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.|
|showCategoryName|boolean|Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.|
|showLegendKey|boolean|Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.|
|showPercentage|boolean|Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.|
|showSeriesName|boolean|Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.|
|showValue|boolean|Valor booleano que representa si el valor de la etiqueta de datos es visible o no.|

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartDataLabels](../resources/chartdatalabels.md) actualizado en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_chartdatalabels"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/datalabels
Content-type: application/json
Content-length: 134

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartDataLabels"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartdatalabels",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->