# <a name="process-resource-type"></a>Tipo de recurso de proceso

Contiene información con estado acerca del proceso relacionadocon la alerta.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|accountName|Cadena|Identificador de la cuenta de usuario (contexto de la cuenta de usuario bajo el cual se ejcuta el proceso) por ejemplo, AccountName, SID, etc.|
|commandLine|Cadena|La línea de comandos de invocación del proceso completo incluidos todos los parámetros.|
|createdDateTime|DateTimeOffset|Hora a la que se inició el proceso. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|fileHash|[fileHash](filehash.md)|Tipo complejo que contiene los valores de hash de archivo (criptográficos y dependientes de la ubicación).|
|integrityLevel|processIntegrityLevel|El nivel de integridad del proceso. Los valores posibles son: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.|
|isElevated|Booleano|True si el proceso es elevado.|
|nombre|Cadena|El nombre del archivo de imagen del proceso.|
|parentProcessCreatedDateTime|DateTimeOffset|Fecha y hora en la que se inició el proceso primario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|parentProcessId|Int32|El identificador del proceso (PID) del proceso principal.|
|parentProcessName|Cadena|El nombre del archivo de imagen del proceso principal.|
|ruta|Cadena|Ruta completa, incluido el filename.|
|processId|Int32|El identificador del proceso (PID) del proceso.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.process"
}-->

```json
{
  "accountName": "String",
  "commandLine": "String",
  "createdDateTime": "String (timestamp)",
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "integrityLevel": "@odata.type: microsoft.graph.processIntegrityLevel",
  "isElevated": true,
  "name": "String",
  "parentProcessCreatedDateTime": "String (timestamp)",
  "parentProcessId": 1024,
  "parentProcessName": "String",
  "path": "String",
  "processId": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "process resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->