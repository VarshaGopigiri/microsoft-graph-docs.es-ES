# <a name="auditevent-resource-type"></a>Tipo de recurso auditEvent

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades del evento de auditoría.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar auditEvents](../api/intune_auditing_auditevent_list.md)|Colección [auditEvent](../resources/intune_auditing_auditevent.md)|Enumere las propiedades y las relaciones de los objetos [auditEvent](../resources/intune_auditing_auditevent.md).|
|[Obtener auditEvent](../api/intune_auditing_auditevent_get.md)|[auditEvent](../resources/intune_auditing_auditevent.md)|Lea las propiedades y las relaciones del objeto [auditEvent](../resources/intune_auditing_auditevent.md).|
|[Crear auditEvent](../api/intune_auditing_auditevent_create.md)|[auditEvent](../resources/intune_auditing_auditevent.md)|Cree un objeto [auditEvent](../resources/intune_auditing_auditevent.md).|
|[Eliminar auditEvent](../api/intune_auditing_auditevent_delete.md)|Ninguna|Elimina un [auditEvent](../resources/intune_auditing_auditevent.md).|
|[Actualizar auditEvent](../api/intune_auditing_auditevent_update.md)|[auditEvent](../resources/intune_auditing_auditevent.md)|Actualice las propiedades de un objeto [auditEvent](../resources/intune_auditing_auditevent.md).|
|[Función getAuditCategories](../api/intune_auditing_auditevent_getauditcategories.md)|Colección de cadenas|Todavía no documentado|
|[Función getAuditActivityTypes](../api/intune_auditing_auditevent_getauditactivitytypes.md)|Colección de cadenas|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|displayName|cadena|Nombre para mostrar del evento.|
|componentName|cadena|Nombre del componente.|
|actor|[auditActor](../resources/intune_auditing_auditactor.md)|Usuario y aplicación de AAD que están asociados al evento de auditoría.|
|actividad|cadena|Nombre descriptivo de la actividad.|
|activityDateTime|DateTimeOffset|La fecha y hora en UTC a la que se realizó la actividad.|
|activityType|cadena|El tipo de actividad que se realizó.|
|activityOperationType|cadena|El tipo de operación HTTP de la actividad.|
|activityResult|cadena|El resultado de la actividad.|
|correlationId|Guid|El identificador de la solicitud de cliente que se usa para correlacionar las actividades dentro del sistema.|
|recursos|Colección [auditResource](../resources/intune_auditing_auditresource.md)|Recursos que se están modificando.|
|categoría|cadena|Categoría de auditoría.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.auditEvent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditEvent",
  "id": "String (identifier)",
  "displayName": "String",
  "componentName": "String",
  "actor": {
    "@odata.type": "microsoft.graph.auditActor",
    "type": "String",
    "permissions": [
      "String"
    ],
    "userPermissions": [
      "String"
    ],
    "applicationId": "String",
    "applicationDisplayName": "String",
    "userPrincipalName": "String",
    "servicePrincipalName": "String",
    "ipAddress": "String",
    "userId": "String"
  },
  "activity": "String",
  "activityDateTime": "String (timestamp)",
  "activityType": "String",
  "activityOperationType": "String",
  "activityResult": "String",
  "correlationId": "<Unknown Primitive Type Edm.Guid>",
  "resources": [
    {
      "@odata.type": "microsoft.graph.auditResource",
      "displayName": "String",
      "modifiedProperties": [
        {
          "@odata.type": "microsoft.graph.auditProperty",
          "displayName": "String",
          "oldValue": "String",
          "newValue": "String"
        }
      ],
      "type": "String",
      "resourceId": "String"
    }
  ],
  "category": "String"
}
```



