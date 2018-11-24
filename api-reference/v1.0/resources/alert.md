# <a name="alert-resource-type"></a>tipo de recurso de alerta

Representa los posibles problemas de seguridad dentro de inquilino de un cliente que han identificado las soluciones de seguridad de Microsoft o socio. Usar alertas para unificar y simplificar la administración de problemas de seguridad a través de todas las soluciones integradas. Para obtener más información, vea las consultas de ejemplo en [El Explorador de gráfico](https://developer.microsoft.com/graph/graph-explorer).

Las alertas se pueden recuperar de proveedores de seguridad diferentes que aparecen en la [Información general de seguridad de Microsoft Graph](security-api-overview.md).

## <a name="methods"></a>Métodos

| Método   | Tipo de valor devuelto|Descripción|
|:---------------|:--------|:----------|
|[Get alert](../api/alert_get.md) | [alerta](alert.md) |Leer propiedades y relaciones de un objeto de alerta.|
|[Update alert](../api/alert_update.md) | [alerta](alert.md) |Actualizar un objeto de alerta. |
|[List alerts](../api/alert_list.md) | colección de [alerta](alert.md) |Obtener una colección de objetos de alerta.|

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|activityGroupName|String|Nombre o el alias del grupo de actividades (atacante) se expresarán esta alerta.|
|assignedTo|String|Nombre del analista de la alerta se asigna a para la evaluación de errores, investigación o corrección (admite [Actualizar](../api/alert_update.md)).|
|azureSubscriptionId|String|Identificador de suscripción de Azure, presente si esta alerta está relacionada con un recurso de Azure.|
|azureTenantId |String|Identificador del inquilino. Azure Active Directory Obligatorio.|
|.|String|Categoría de la alerta (por ejemplo, credentialTheft, ransomware, etcetera).|
|closedDateTime|DateTimeOffset|Hora a la que se ha cerrado la alerta. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 tendrá este aspecto: `'2014-01-01T00:00:00Z'` (admite [Actualizar](../api/alert_update.md)).|
|cloudAppStates|colección de [cloudAppSecurityState](cloudappsecuritystate.md)|Información con seguimiento de estado relacionadas con la seguridad generada por el proveedor acerca de la aplicación en la nube/s relacionados con esta alerta.|
|comments|Colección String|Comentarios proporcionado por el cliente de alerta (para la administración de alertas del cliente) (admite [Actualizar](../api/alert_update.md)).|
|confidence|Int32|Confianza de la lógica de detección (el porcentaje entre 1 y 100).|
|createdDateTime |DateTimeOffset|Hora en que se creó la alerta por el proveedor de alerta. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Obligatorio.|
|descripción|String|Descripción de la alerta.|
|detectionIds|Colección String|Conjunto de alertas relacionadas con esta entidad alerta (cada alerta se inserta en el SIEM como un registro independiente).|
|eventDateTime |DateTimeOffset|Hora a la que se produjo el evento o eventos que sirven como desencadenador que se va a generar la alerta. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Obligatorio.|
|comentarios|alertFeedback|Comentarios de analistas de la alerta. Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`. (admite la [actualización](../api/alert_update.md))|
|fileStates|colección de [fileSecurityState](filesecuritystate.md)|Información con seguimiento de estado relacionadas con la seguridad generada por el proveedor acerca de los archivos relacionados con esta alerta.|
|hostStates|colección de [hostSecurityState](hostsecuritystate.md)|Información con seguimiento de estado relacionadas con la seguridad generada por el proveedor acerca de los hosts relacionados con esta alerta.|
|id |String|Identificador GUID/único generado por el proveedor. Solo lectura. Obligatorio.|
|lastModifiedDateTime|DateTimeOffset|Hora a la que se modificó por última vez la entidad de alerta. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|malwareStates|colección de [malwareState](malwarestate.md)|Inteligencia de amenaza perteneciente a malware relacionados con esta alerta.|
|networkConnections|colección [networkConnection](networkconnection.md)|Información con seguimiento de estado relacionadas con la seguridad generada por el proveedor acerca de las conexiones de red relacionadas con esta alerta.|
|procesos|colección de [proceso](process.md)|Información con seguimiento de estado relacionadas con la seguridad generada por el proveedor sobre el proceso o los procesos relacionados con esta alerta.|
|recommendedActions|Colección String|Proveedor/proveedor recomienda acciones que desea realizar como resultado de la alerta (por ejemplo, aislar máquina, enforce2FA, host de crear una nueva imagen).|
|registryKeyStates|colección de [registryKeyState](registrykeystate.md)|Generados por el proveedor acerca de las claves del registro de información con estado relacionadas con la seguridad relacionados con esta alerta.|
|gravedad |alertSeverity|Gravedad de alerta - establecida por el proveedor o proveedor. Los valores posibles son: `unknown`, `informational`, `low`, `medium` y `high`. Obligatorio.|
|sourceMaterials|Colección String|Hipervínculos (URI) para el material de origen relacionados con la alerta, por ejemplo, interfaz de usuario del proveedor para las alertas o búsqueda de registro, etcetera.|
|status |alertStatus|Estado de alerta del ciclo de vida (escenario). Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`. (admite [Actualizar](../api/alert_update.md)). Obligatorio.|
|de cierre|Colección String|Etiquetas definidos por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo "HVA", "Han visto", etcetera.) (admite [Actualizar](../api/alert_update.md)).|
|title |String|Título de la alerta. Obligatorio.|
|desencadenadores|colección de [alertTrigger](alerttrigger.md)|Información relacionada con la seguridad acerca de las propiedades específicas que desencadenan la alerta (propiedades que aparecen en la alerta). Alertas pueden contener información acerca de varios usuarios, hosts, archivos, las direcciones ip. Este campo indica qué propiedades desencadenan la generación de alertas.|
|userStates|colección de [userSecurityState](usersecuritystate.md)|Información de estado relacionada con la seguridad generado por el proveedor acerca de las cuentas de usuario relacionados con esta alerta.|
|vendorInformation |[securityVendorInformation](securityvendorinformation.md)|Tipo complejo que contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker). Obligatorio.|
|vulnerabilityStates|colección de [vulnerabilityState](vulnerabilitystate.md)|Inteligencia de amenaza perteneciente a uno o más de las vulnerabilidades relacionadas con esta alerta.|

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