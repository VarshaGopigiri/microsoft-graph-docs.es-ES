# <a name="filesecuritystate-resource-type"></a>Tipo de recurso fileSecurityState

Contiene información sobre el archivo (no proceso) relacionado con la alerta.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|fileHash|[fileHash](filehash.md)|Tipo complejo que contiene los valores de hash de archivo (criptográficos y dependientes de la ubicación).|
|name|Cadena|Nombre de archivo (sin ruta de acceso).|
|path|Cadena|Ruta de acceso completa al archivo del archivo/imageFile.|
|riskScore|Cadena|Puntuación de riesgo calculado/generado por el proveedor del archivo de alerta. Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileSecurityState"
}-->

```json
{
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "name": "String",
  "path": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->