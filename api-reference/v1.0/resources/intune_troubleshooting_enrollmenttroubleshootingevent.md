# <a name="enrollmenttroubleshootingevent-resource-type"></a>Tipo de recurso enrollmentTroubleshootingEvent

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Evento que representa un error de inscripción.

Hereda de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar enrollmentTroubleshootingEvents](../api/intune_troubleshooting_enrollmenttroubleshootingevent_list.md)|Colección [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md)|Enumere las propiedades y las relaciones de los objetos [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).|
|[Obtener enrollmentTroubleshootingEvent](../api/intune_troubleshooting_enrollmenttroubleshootingevent_get.md)|[enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md)|Lea las propiedades y las relaciones del objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).|
|[Crear enrollmentTroubleshootingEvent](../api/intune_troubleshooting_enrollmenttroubleshootingevent_create.md)|[enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md)|Cree un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).|
|[Eliminar enrollmentTroubleshootingEvent](../api/intune_troubleshooting_enrollmenttroubleshootingevent_delete.md)|Ninguno|Elimina un [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).|
|[Actualizar enrollmentTroubleshootingEvent](../api/intune_troubleshooting_enrollmenttroubleshootingevent_update.md)|[enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md)|Actualice las propiedades de un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)|
|eventDateTime|DateTimeOffset|Hora en que ocurrió el evento. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)|
|correlationId|Cadena|Id. utilizado para rastrear el error en el servicio. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)|
|managedDeviceIdentifier|Cadena|Identificador del dispositivo creado o recopilado por Intune.|
|operatingSystem|Cadena|Sistema operativo.|
|osVersion|Cadena|Versión del sistema operativo.|
|userId|Cadena|Identificador del usuario que intentó inscribir el dispositivo.|
|deviceId|Cadena|Identificador de dispositivo de Azure AD.|
|enrollmentType|Cadena|Tipo de la inscripción. Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.|
|failureCategory|Cadena|Categoría general del error. Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced` y `clientDisconnected`.|
|failureReason|Cadena|Motivo del error detallado.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.enrollmentTroubleshootingEvent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.enrollmentTroubleshootingEvent",
  "id": "String (identifier)",
  "eventDateTime": "String (timestamp)",
  "correlationId": "String",
  "managedDeviceIdentifier": "String",
  "operatingSystem": "String",
  "osVersion": "String",
  "userId": "String",
  "deviceId": "String",
  "enrollmentType": "String",
  "failureCategory": "String",
  "failureReason": "String"
}
```



