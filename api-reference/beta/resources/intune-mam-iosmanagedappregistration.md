---
title: Tipo de recurso iosManagedAppRegistration
description: Representa los detalles de sincronización de una aplicación para iOS, con capacidades de administración, para un usuario específico.
localization_priority: Normal
ms.openlocfilehash: fbbb2579ebfb77d8a98acd21339d98cae9fad8e0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836389"
---
# <a name="iosmanagedappregistration-resource-type"></a>Tipo de recurso iosManagedAppRegistration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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
|managedDeviceId|Cadena|El identificador de dispositivo administrado del dispositivo host. Valor puede estar vacío, incluso cuando se administra el dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|azureADDeviceId|Cadena|El identificador de dispositivo de Azure Active Directory del dispositivo host. Valor puede estar vacío, incluso cuando el dispositivo de host es Azure Active Directory registrada. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|deviceModel|Cadena|El modelo de dispositivo para el actual registro de la aplicación heredada de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|entradas deviceManufacturer|Cadena|El fabricante del dispositivo para el actual registro de la aplicación heredada de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
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
  "managedDeviceId": "String",
  "azureADDeviceId": "String",
  "deviceModel": "String",
  "deviceManufacturer": "String",
  "flaggedReasons": [
    "String"
  ],
  "userId": "String",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
    "bundleId": "String"
  },
  "id": "String (identifier)",
  "version": "String"
}
```





