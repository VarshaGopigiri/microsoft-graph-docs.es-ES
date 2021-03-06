---
title: Tipo de recurso managedAppRegistration
description: El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 69d532f7c8287b678c1f62f5b8b78c6e4a99d2ef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944820"
---
# <a name="managedappregistration-resource-type"></a>Tipo de recurso managedAppRegistration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.
El recurso ManagedAppRegistration representa los detalles de una aplicación, con capacidad de administración, usado por un miembro de la organización.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppRegistrations](../api/intune-mam-managedappregistration-list.md)|Colección [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|Enumere las propiedades y las relaciones de los objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|[Obtener managedAppRegistration](../api/intune-mam-managedappregistration-get.md)|[managedAppRegistration](../resources/intune-mam-managedappregistration.md)|Lea las propiedades y las relaciones del objeto [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|[Función getUserIdsWithFlaggedAppRegistration](../api/intune-mam-managedappregistration-getuseridswithflaggedappregistration.md)|Colección de cadenas|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|Fecha y hora de creación|
|lastSyncDateTime|DateTimeOffset|Fecha y hora de la última sincronización de la aplicación con el servicio de administración.|
|applicationVersion|Cadena|Versión de la aplicación|
|managementSdkVersion|Cadena|Versión del SDK de administración de la aplicación|
|platformVersion|Cadena|Versión del sistema operativo|
|deviceType|Cadena|Tipo de dispositivo host|
|deviceTag|Cadena|Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo. No garantiza que las aplicaciones se relacionen en todas las condiciones.|
|deviceName|Cadena|Nombre del dispositivo host|
|managedDeviceId|Cadena|El identificador de dispositivo administrado del dispositivo host. Valor puede estar vacío, incluso cuando se administra el dispositivo host.|
|azureADDeviceId|Cadena|El identificador de dispositivo de Azure Active Directory del dispositivo host. Valor puede estar vacío, incluso cuando el dispositivo de host es Azure Active Directory registrada.|
|deviceModel|Cadena|El modelo de dispositivo para el registro actual de la aplicación |
|entradas deviceManufacturer|Cadena|El fabricante del dispositivo para el registro actual de la aplicación |
|flaggedReasons|colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)|Cero o más razones por las que se ha marcado el registro de una aplicación. Por ejemplo, una aplicación que se ejecuta en el dispositivo liberado|
|userId|Cadena|El identificador de usuario al que pertenece este registro de la aplicación.|
|appIdentifier|[mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)|El identificador del paquete de aplicación|
|id|Cadena|Clave de la entidad.|
|version|Cadena|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|appliedPolicies|Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|Ya se habían aplicado cero o más directivas en la aplicación registrada cuando se sincronizó por última vez con el servicio de administración.|
|intendedPolicies|Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|El administrador esperaba cero o más directivas hasta el momento.|
|operaciones|Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)|Se activaron cero o más operaciones de larga duración en el registro de la aplicación.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppRegistration",
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
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "String (identifier)",
  "version": "String"
}
```





