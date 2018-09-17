# <a name="cloudappsecuritystate-resource-type"></a>Tipo de recurso cloudAppSecurityState

Contiene información con estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
|destinationServiceIp|Cadena|Dirección IP de destino de la conexión a la aplicación o servicio en la nube.|
|destinationServiceName|Cadena|Nombre de aplicación o servicio en la nube (por ejemplo "Salesforce", "DropBox", etc.).|
|riskScore|Cadena|Puntuación de riesgo calculado/generado por el proveedor de la aplicación o servicio en la nube. Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.cloudAppSecurityState"
}-->

```json
{
  "destinationServiceIp": "String",
  "destinationServiceName": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "cloudAppSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->