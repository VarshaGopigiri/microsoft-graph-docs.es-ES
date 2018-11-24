# <a name="operationerror-resource-type"></a>tipo de recurso operationError



Se describen los errores en [teamsAsyncOperation](teamsasyncoperation.md).

## <a name="operationerror-properties"></a>Propiedades de operationError
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|código|cadena (sólo lectura)|Código de error de la operación.|
|mensaje|cadena (sólo lectura)|Mensaje de error de la operación.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.operationError"
}-->

```json
{
    "code": "TeamUnavailable",
    "message": "The team was not found."
}
```

<!-- uuid: 069fadaa-52db-4ced-85d5-74f7caa2c66f
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation error resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
