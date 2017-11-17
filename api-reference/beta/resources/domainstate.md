<a id="domainstate-resource-type" class="xliff"></a>
# Tipo de recurso domainState

Representa el estado de las operaciones asincrónicas programadas en un dominio.

<a id="properties" class="xliff"></a>
## Propiedades

| Propiedad   | Tipo | Descripción |
|:---------------|:--------|:----------|
| lastActionDateTime | DateTimeOffset | Marca de tiempo de la última actividad. El valor se actualiza cuando se programa una operación, se inicia la tarea asincrónica y cuando termina la operación. |
| operación | Cadena | Tipo de operación asincrónica. Los valores pueden ser *ForceDelete* o *Verification* |
| status | Cadena | Estado actual de la operación. <br> *Programada*: La operación se ha programado, pero no se ha iniciado. <br> *En curso*: La tarea se ha iniciado y está en curso. <br> *Error*: Se ha producido un error en la operación. |

<a id="json-representation" class="xliff"></a>
## Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainState"
}-->

```json
{
  "lastActionDateTime": "String (timestamp)",
  "operation": "String",
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->