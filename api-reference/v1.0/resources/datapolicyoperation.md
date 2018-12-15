# <a name="datapolicyoperation-resource-type"></a>tipo de recurso dataPolicyOperation

Representa una operación de la directiva de datos enviados. Contiene la información necesaria para realizar un seguimiento del estado de una operación. Por ejemplo, un administrador de la compañía puede enviar una solicitud de operación de directiva de datos para exportar datos de un empleado de la compañía y, a continuación, más adelante realizar un seguimiento de dicha solicitud.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener dataPolicyOperation](../api/datapolicyoperation-get.md) | [dataPolicyOperation](datapolicyoperation.md) |Recuperar las propiedades del objeto **dataPolicyOperation** .|
|[Exportar datos personales](../api/user-exportpersonaldata.md) | Ninguno |Enviar una solicitud de operación de directiva de datos para exportar los datos del usuario organizativa que más adelante se pueden leer mediante [Get dataPolicyOperation](../api/datapolicyoperation-get.md)|

## <a name="properties"></a>Propiedades

> **Nota:** Todas las propiedades de este recurso son de sólo lectura.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|completedDateTime|DateTimeOffset|Representa la solicitud para esta operación de la directiva de datos se ha completado, en la hora UTC, con el formato ISO 8601. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. NULL hasta que se complete la operación.|
|id|String| Clave única para esta operación. |
|status|string| Los valores posibles son: `notStarted`, `running`, `complete`, `failed` y `unknownFutureValue`.|
|storageLocation|String|La ubicación de la dirección URL a donde se va a exportar datos para las solicitudes de exportación.|
|userId|String|El identificador para el usuario en quien se realiza la operación.|
|submittedDateTime|DateTimeOffset|Representa para esta operación de datos se envió la solicitud, en la hora UTC, con el formato ISO 8601. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|progreso|String|Especifica el progreso de una operación.|

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.dataPolicyOperation"
}-->

```json
{
  "completedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "status": "string",
  "storageLocation": "String",
  "userId": "String",
  "submittedDateTime": "String (timestamp)", 
  "progress": "String (double)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "dataPolicyOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
