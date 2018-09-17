# <a name="alerttrigger-resource-type"></a>Tipo de recurso alertTrigger

Contiene información acerca de las propiedades que han desencadenado una detección (propiedades que existen en la entidad de alerta).

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|nombre|Cadena|Nombre de la propiedad que actúa como desencadenador de la detección.|
|tipo|Cadena|Tipo de la propiedad en el par key:value para interpretación. Por ejemplo, Cadena, Booleano, etc.|
|valor|Cadena|Valor de la propiedad que actúa como desencadenador de la detección.|

## <a name="json-representation"></a>Representación JSON

Esta es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.alertTrigger"
}-->

```json
{
  "name": "String",
  "type": "String",
  "value": "String"
}

```

## <a name="example"></a>Ejemplo

```json
{
  "name": "endpointAddress",
  "type": "networkConnection.sourceAddress",
  "value": "10.154.9.40"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alertTrigger resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->