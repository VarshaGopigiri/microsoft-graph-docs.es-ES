# <a name="physicaladdress-resource-type"></a>Tipo de recurso physicalAddress

Representa la dirección postal de un recurso, como un contacto o un evento.


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|city|String|Ciudad.|
|countryOrRegion|String|País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".|
|postalCode|String|Código postal.|
|state|String|Estado.|
|street|String|Calle.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.physicalAddress"
}-->

```json
{
  "city": "string",
  "countryOrRegion": "string",
  "postalCode": "string",
  "state": "string",
  "street": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "physicalAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
