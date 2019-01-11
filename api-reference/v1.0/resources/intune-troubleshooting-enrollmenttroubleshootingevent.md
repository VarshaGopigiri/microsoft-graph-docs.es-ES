---
title: Tipo de recurso enrollmentTroubleshootingEvent
description: Evento que representa un error de inscripción.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 416dee647ae79f8da1871e9c126038ee21c688a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805358"
---
# <a name="enrollmenttroubleshootingevent-resource-type"></a>Tipo de recurso enrollmentTroubleshootingEvent

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Evento que representa un error de inscripción.

Hereda de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar enrollmentTroubleshootingEvents](../api/intune-troubleshooting-enrollmenttroubleshootingevent-list.md)|Colección [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md)|Enumere las propiedades y las relaciones de los objetos [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).|
|[Obtener enrollmentTroubleshootingEvent](../api/intune-troubleshooting-enrollmenttroubleshootingevent-get.md)|[enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md)|Lea las propiedades y las relaciones del objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).|
|[Crear enrollmentTroubleshootingEvent](../api/intune-troubleshooting-enrollmenttroubleshootingevent-create.md)|[enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md)|Cree un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).|
|[Eliminar enrollmentTroubleshootingEvent](../api/intune-troubleshooting-enrollmenttroubleshootingevent-delete.md)|Ninguno|Elimina un [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).|
|[Actualizar enrollmentTroubleshootingEvent](../api/intune-troubleshooting-enrollmenttroubleshootingevent-update.md)|[enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md)|Actualice las propiedades de un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)|
|eventDateTime|DateTimeOffset|Hora en que ocurrió el evento. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)|
|correlationId|Cadena|Id. utilizado para rastrear el error en el servicio. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)|
|managedDeviceIdentifier|Cadena|Identificador del dispositivo creado o recopilado por Intune.|
|operatingSystem|Cadena|Sistema operativo.|
|osVersion|Cadena|Versión del sistema operativo.|
|userId|Cadena|Identificador del usuario que intentó inscribir el dispositivo.|
|deviceId|Cadena|Identificador de dispositivo de Azure AD.|
|enrollmentType|[deviceEnrollmentType](../resources/intune-shared-deviceenrollmenttype.md)|Tipo de la inscripción. Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.|
|failureCategory|[deviceEnrollmentFailureReason](../resources/intune-troubleshooting-deviceenrollmentfailurereason.md)|Categoría general del error. Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected` y `userAbandonment`.|
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

<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: Enum deviceEnrollmentFailureReason has some values specified and others unspecified."
  ],
}
-->



