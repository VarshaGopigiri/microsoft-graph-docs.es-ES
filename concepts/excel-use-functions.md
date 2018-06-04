# <a name="use-workbook-functions-in-excel-with-microsoft-graph"></a>Usar funciones de libro en Excel con Microsoft Graph

Puede invocar cualquier función de libro con la sintaxis siguiente: `POST /workbook/functions/{function-name}`. Especifique los argumentos de la función en el cuerpo con un objeto JSON. Las cadenas `value` y `error` resultantes de la función se devuelven en el objeto de resultado de la función. El valor `error` de `null` indica que la función se ha ejecutado correctamente.

La lista completa de funciones admitidas se encuentra [aquí](https://support.office.com/es-ES/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188). Consulte la firma de la función para obtener tipos de datos y nombres de parámetros específicos.

_Notas importantes:_
* El parámetro de entrada de intervalo se suministra mediante un objeto range en lugar de la cadena de dirección de intervalo.  
* El parámetro de índice es “1 indexado”, a diferencia del “índice 0” usado en la mayoría de las API.

Ejemplo: **BUSCARV**

En una hoja de cálculo de Excel, la función `vlookup` admite estos argumentos:

1. **valor_buscado** (obligatorio) El valor que quiere buscar.
2. **matriz_buscar_en** (obligatorio) El rango de celdas donde se encuentra el valor de búsqueda. Recuerde que el valor de búsqueda siempre tiene que estar en la primera columna del rango para que BUSCARV funcione correctamente. Por ejemplo, si el valor de búsqueda se encuentra en la celda C2, el rango tiene que empezar con C.
3. **indicador_columnas** (obligatorio) El número de columna en el rango que contiene el valor devuelto. Por ejemplo, si especifica B2:D11 como el rango, B será la primera columna, C la segunda, etc.
4. **búsqueda_en_rango** (opcional) El valor lógico que especifica si quiere usar **BUSCARV** para encontrar una coincidencia exacta o una coincidencia aproximada. De forma opcional, puede especificar **VERDADERO** si quiere obtener una coincidencia aproximada, o bien **FALSO** si quiere obtener una coincidencia exacta del valor devuelto. Si no especifica nada, el valor predeterminado será siempre VERDADERO o coincidencia aproximada.

Dentro de una celda, la función `vlookup` es similar a esta:

= BUSCARV(valor de búsqueda, rango que contiene el valor de búsqueda, el número de columna en el rango que contiene el valor devuelto, de forma opcional, especifique VERDADERO para obtener una coincidencia aproximada o FALSO para una coincidencia exacta)

(Vea la documentación de la [Función de Excel BUSCARV](https://support.office.com/es-ES/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1)).


##### <a name="request"></a>Solicitud:
En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `vlookup` y pasar estos parámetros con la API de REST de Excel.

```http
POST https://graph.microsoft.com/beta/me/drive/root:/book1.xlsx:/workbook/functions/vlookup
content-type: Application/Json
authorization: Bearer {access-token}
workbook-session-id: {session-id}

{
    "lookupValue": "Temperature",
    "tableArray": { "Address": "Sheet1!E1:G5" },
    "colIndexNum": 2,
    "rangeLookup": false
}
```

##### <a name="response"></a>Respuesta

```http
HTTP code: 200 OK
content-type: application/json;odata.metadata

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#workbookFunctionResult",
    "@odata.type": "#microsoft.graph.workbookFunctionResult",
    "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/root/workbook/functions/vlookup()",
    "error": null,
    "value": "28.3"
}
```

Ejemplo: `median`

En una hoja de cálculo de Excel, la función `median` admite una matriz de uno o más rangos de entrada.

Dentro de una celda, la función `median` es similar a este ejemplo:

=MEDIANA(A2:A6)

(Vea la documentación de la [Función de Excel MEDIANA](https://support.office.com/es-ES/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2)).

##### <a name="request"></a>Solicitud
En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `median` y uno o más rangos de entrada con la API de REST de Excel.

```http
POST https://graph.microsoft.com/beta/me/drive/root:/book1.xlsx:/workbook/functions/median
content-type: Application/Json
authorization: Bearer {access-token}
workbook-session-id: {session-id}

{
"values" :  [
        { "address": "Sheet2!A1:A5" },
        { "address": "Sheet2!B1:B5" },
      ]
}
```

##### <a name="response"></a>Respuesta

```http
HTTP code: 200 OK
content-type: application/json;odata.metadata

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#workbookFunctionResult",
  "@odata.type": "#microsoft.graph.workbookFunctionResult",
  "@odata.id": "/users('2abcad6a-2fca-4b6e-9577-e358a757d77d')/drive/root/workbook/functions/median()",
  "error": null,
  "value": 30
}
```

## <a name="see-also"></a>Vea también
* [Administrar sesiones en Excel con Microsoft Graph](excel-manage-sessions.md)
* [Escribir en un libro de Excel con Microsoft Graph](excel-write-to-workbook.md)
* [Actualizar el formato de un rango en Excel con Microsoft Graph](excel-update-range-format.md)
* [Mostrar una imagen de gráfico de Excel con Microsoft Graph](excel-display-chart-image.md)
* [Usar la API de REST de Excel](../api-reference/v1.0/resources/excel.md)
