---
title: Tipo de recurso iosManagedAppRegistration
description: Representa los detalles de sincronización de una aplicación para iOS, con capacidades de administración, para un usuario específico.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 224c86f2671902fc84e4346f42b5af56d14419ac
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971742"
---
# <a name="iosmanagedappregistration-resource-type"></a>Tipo de recurso iosManagedAppRegistration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa los detalles de sincronización de una aplicación para iOS, con capacidades de administración, para un usuario específico.
El recurso ManagedAppRegistration representa los detalles de una aplicación, con capacidad de administración, usado por un miembro de la organización.

Hereda de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosManagedAppRegistrations](../api/intune-mam-iosmanagedappregistration-list.md)|Colección [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md)|Enumere las propiedades y las relaciones de los objetos [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md).|
|[Obtener iosManagedAppRegistration](../api/intune-mam-iosmanagedappregistration-get.md)|[iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md)|Lea las propiedades y las relaciones del objeto [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|lastSyncDateTime|DateTimeOffset|Fecha y hora de la última sincronización de la aplicación con el servicio de administración. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|applicationVersion|Cadena|Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|managementSdkVersion|Cadena|Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|platformVersion|Cadena|Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|deviceType|Cadena|Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|deviceTag|Cadena|Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo. No garantiza que las aplicaciones se relacionen en todas las condiciones. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|deviceName|Cadena|Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|flaggedReasons|colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)|Cero o más razones por las que se ha marcado el registro de una aplicación. Por ejemplo, una aplicación que se ejecuta en un dispositivo liberado. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|userId|Cadena|Identificador de usuario al que pertenece este registro de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|appIdentifier|[mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)|Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|id|Cadena|Clave de la entidad. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|version|Cadena|Versión de la entidad. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|appliedPolicies|Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|Ya se habían aplicado cero o más directivas en la aplicación registrada cuando se sincronizó por última vez con el servicio de administración. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|intendedPolicies|Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|El administrador esperaba cero o más directivas hasta el momento. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|operaciones|Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)|Se activaron cero o más operaciones de larga duración en el registro de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosManagedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
  "createdDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "applicationVersion": "String",
  "managementSdkVersion": "String",
  "platformVersion": "String",
  "deviceType": "String",
  "deviceTag": "String",
  "deviceName": "String",
  "flaggedReasons": [
    "String"
  ],
  "userId": "String",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier",
    "bundleId": "String"
  },
  "id": "String (identifier)",
  "version": "String"
}
```


<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-mam-iosmanagedappregistration.md/microsoft.graph.iosManagedAppRegistration/flaggedReasons:
      Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->
