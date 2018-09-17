# <a name="alert-resource-type"></a>tipo de recurso de alerta

Representa los posibles problemas de seguridad dentro de la cuenta empresarial de un cliente que las soluciones de seguridad de Microsoft o de un socio han identificado. Usar alertas para unificar y simplificar la administración de problemas de seguridad a través de todas las soluciones integradas. Para obtener más información, vea las consultas de ejemplo en [Probador de Graph](https://developer.microsoft.com/en-us/graph/graph-explorer).

Las alertas se pueden recuperar de los siguientes proveedores: Azure Security Center y Azure Active Directory Identity Protection. En los meses siguientes se integrarán proveedores de alerta adicionales.

## <a name="methods"></a>Métodos

| Método   | Tipo de valor devuelto|Descripción|
|:---------------|:--------|:----------|
|[Obtener alerta](../api/alert_get.md) | [alerta](alert.md) |Lee propiedades y relaciones de un objeto de alerta.|
|[Actualizar alerta](../api/alert_update.md) | [alerta](alert.md) |Actualiza un objeto de alerta. |
|[Alertas de lista](../api/alert_list.md) | colección de [alert](alert.md) |Obtiene una colección de objetos de alerta.|

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|activityGroupName|Cadena|Nombre o alias del grupo de actividades (atacante) al que se atribuye esta alerta.|
|assignedTo|Cadena|Nombre del analista que se le ha asignado a la alerta para la evaluación de errores, investigación o corrección (admite la [actualización](../api/alert_update.md)).|
|azureSubscriptionId|Cadena|Identificador de suscripción de Azure, presente si esta alerta está relacionada con un recurso de Azure.|
|azureTenantId *|Cadena|Identificador de la cuenta empresarial de Azure Active Directory.|
|category|Cadena|Categoría de la alerta (por ejemplo, credentialTheft, ransomware, etc.).|
|closedDateTime|DateTimeOffset|Hora a la que se ha cerrado la alerta. El tipo Timestamp (marca de hora) representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 tendría este aspecto: `'2014-01-01T00:00:00Z'` (admite la [actualización](../api/alert_update.md)).|
|cloudAppStates|colección de [cloudAppSecurityState](cloudappsecuritystate.md)|Información con seguimiento de estado sobre la seguridad generada por el proveedor acerca de la aplicación/es en la nube relacionada/s con esta alerta.|
|comments|Colección de cadenas|Comentarios proporcionados por el cliente sobre la alerta (para la administración de alertas del cliente) (admite la [actualización](../api/alert_update.md)).|
|confidence|Int32|Confianza de la lógica de detección (porcentaje entre 1 y 100).|
|createdDateTime *|DateTimeOffset|Hora a la que el proveedor de alerta creó la alerta. El tipo Timestamp (marca de hora) representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|descripción|Cadena|Descripción de la alerta.|
|detectionIds|Colección de cadenas|Conjunto de alertas relacionadas con esta entidad de alerta (cada alerta se inserta en el SIEM como un registro independiente).|
|eventDateTime *|DateTimeOffset|Hora a la que se produjo el evento o eventos que sirve(n) como desencadenador(es) para generar la alerta. El tipo Timestamp (marca de hora) representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|feedback|alertFeedback|Comentarios del analista sobre la alerta. Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`. (admite la [actualización](../api/alert_update.md))|
|fileStates|colección de [fileSecurityState](filesecuritystate.md)|Información con seguimiento de estado sobre la seguridad generada por el proveedor acerca del archivo o archivos relacionados con esta alerta.|
|hostStates|colección de [hostSecurityState](hostsecuritystate.md)|Información con seguimiento de estado sobre la seguridad generada por el proveedor acerca del host o hosts relacionados con esta alerta.|
|id *|Cadena|Identificador GUID/único generado por el proveedor. (Solo lectura)|
|lastModifiedDateTime|DateTimeOffset|Hora a la que se modificó por última vez la entidad de alerta. El tipo Timestamp (marca de hora) representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|malwareStates|colección de [malwareState](malwarestate.md)|Inteligencia sobre amenazas perteneciente a malware relacionados con esta alerta.|
|networkConnections|colección de [networkConnection](networkconnection.md)|Información con seguimiento de estado sobre la seguridad generada por el proveedor acerca de la conexión o conexiones de red relacionadas con esta alerta.|
|processes|colección de [process](process.md)|Información con seguimiento de estado sobre la seguridad generada por el proveedor acerca del proceso o procesos relacionados con esta alerta.|
|recommendedActions|Colección de cadenas|La acción o acciones que realizar recomendadas por el proveedor como resultado de la alerta (por ejemplo, aislar la máquina, enforce2FA, restablecer la imagen inicial del host).|
|registryKeyStates|colección de [registryKeyState](registrykeystate.md)|Información con seguimiento de estado sobre la seguridad generada por el proveedor acerca de las claves de registro relacionadas con esta alerta.|
|severity *|alertSeverity|Gravedad de alerta - establecida por el proveedor. Los valores posibles son: `unknown`, `informational`, `low`, `medium` y `high`.|
|sourceMaterials|Colección de cadenas|Hipervínculos (URI) al material de origen relacionado con la alerta, por ejemplo, la interfaz de usuario del proveedor para las alertas o la búsqueda de registros, etc.|
|status *|alertStatus|Estado del ciclo de vida de la alerta (fase). Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`. (admite la [actualización](../api/alert_update.md))|
|tags|Colección de cadenas|Etiquetas definidas por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo, "HVA", "SAW", etc.) (admite la [actualización](../api/alert_update.md)).|
|title *|Cadena|Título de la alerta.|
|triggers|colección de [alertTrigger](alerttrigger.md)|Información sobre la seguridad acerca de las propiedades específicas que desencadenaron la alerta (propiedades que aparecen en la alerta). Las alertas pueden contener información acerca de varios usuarios, hosts, archivos y direcciones ip. Este campo indica qué propiedades desencadenaron la generación de alertas.|
|userStates|colección de [userSecurityState](usersecuritystate.md)|Información con seguimiento de estado sobre la seguridad generada por el proveedor acerca de las cuentas de usuario relacionadas con esta alerta.|
|vendorInformation *|[securityVendorInformation](securityvendorinformation.md)|Tipo complejo que contiene detalles sobre el vendor del producto o servicio de seguridad, el proveedor y el subproveedor (por ejemplo, vendor=Microsoft; proveedor=Windows Defender ATP; subproveedor=AppLocker).|
|vulnerabilityStates|colección de [vulnerabilityState](vulnerabilitystate.md)|Inteligencia sobre amenazas perteneciente a una o más vulnerabilidades relacionadas con esta alerta.|
(\* Indica un campo obligatorio.)

## <a name="relationships"></a>Relaciones

Ninguna.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.alert"
}-->

```json
{
  "activityGroupName": "String",
  "assignedTo": "String",
  "azureSubscriptionId": "String",
  "azureTenantId": "String",
  "category": "String",
  "closedDateTime": "String (timestamp)",
  "cloudAppStates": [{"@odata.type": "microsoft.graph.cloudAppSecurityState"}],
  "comments": ["String"],
  "confidence": 1024,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "detectionIds": ["String"],
  "eventDateTime": "String (timestamp)",
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "fileStates": [{"@odata.type": "microsoft.graph.fileSecurityState"}],
  "hostStates": [{"@odata.type": "microsoft.graph.hostSecurityState"}],
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "malwareStates": [{"@odata.type": "microsoft.graph.malwareState"}],
  "networkConnections": [{"@odata.type": "microsoft.graph.networkConnection"}],
  "processes": [{"@odata.type": "microsoft.graph.process"}],
  "recommendedActions": ["String"],
  "registryKeyStates": [{"@odata.type": "microsoft.graph.registryKeyState"}],
  "severity": "@odata.type: microsoft.graph.alertSeverity",
  "sourceMaterials": ["String"],
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "title": "String",
  "triggers": [{"@odata.type": "microsoft.graph.alertTrigger"}],
  "userStates": [{"@odata.type": "microsoft.graph.userSecurityState"}],
  "vendorInformation": {"@odata.type": "microsoft.graph.securityVendorInformation"},
  "vulnerabilityStates": [{"@odata.type": "microsoft.graph.vulnerabilityState"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alert resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->