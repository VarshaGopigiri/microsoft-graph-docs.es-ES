# <a name="workbook-resource-type"></a>Tipo de recurso Workbook

Workbook es el objeto de nivel superior que contiene los objetos de libro relacionados, como hojas de cálculo, tablas, intervalos, etc.

## <a name="properties"></a>Propiedades
Ninguno

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Crear una sesión](../api/workbook_createsession.md) | [workbookSessionInfo](workbooksessioninfo.md) |Crear una sesión de libro para iniciar una sesión persistente o no persistente.|
|[Cerrar sesión](../api/workbook_closesession.md) | Ninguno |Cerrar una sesión existente.|
|[Actualizar sesión](../api/workbook_refreshsession.md) | Ninguno |Actualizar una sesión existente.|


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|names|Colección [NamedItem](nameditem.md)|Representa una colección de elementos con nombre en el ámbito del libro (intervalos y constantes con nombre). Solo lectura.|
|tables|Colección [Table](table.md)|Representa una colección de tablas asociadas con el libro. Solo lectura.|
|worksheets|Colección [Worksheet](worksheet.md)|Representa una colección de hojas de cálculo asociadas con el libro. Solo lectura.|

## <a name="functions"></a>Funciones

[Funciones de Excel](#functions): Para invocar una función de libro, use la sintaxis `POST /workbook/functions/{function-name}` y proporcione los argumentos de la función en el cuerpo mediante un objeto JSON. Las cadenas `value` y `error` resultantes de la función se devuelven en el objeto de resultado de la función. El valor `error` de `null` indica que la función se ha ejecutado correctamente. 

La lista completa de funciones admitidas se encuentra [aquí](https://support.office.com/en-us/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188). Consulte la firma de la función para obtener tipos de datos y nombres de parámetros específicos.

_Notas importantes:_ 
* El parámetro de entrada de intervalo se suministra mediante un objeto range en lugar de la cadena de dirección de intervalo.  
* El parámetro de índice es 1 indexado, a diferencia del índice 0 usado en la mayoría de las API. 

Ejemplo: 

En el ejemplo siguiente, para llamar a la función `vlookup`, se pasan el valor de búsqueda, el rango de entrada y el valor que se devolverá. 

Solicitud: 

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

Respuesta:

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

Ejemplo: 

En el ejemplo siguiente, para llamar a la función `median`, se pasan los intervalos de entrada en una matriz. 

Solicitud: 

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

Respuesta:

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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Workbook resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
