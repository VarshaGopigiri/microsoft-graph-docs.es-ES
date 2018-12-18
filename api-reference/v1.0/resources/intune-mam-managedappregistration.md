---
title: Tipo de recurso managedAppRegistration
description: El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.
author: tfitzmac
ms.openlocfilehash: 218a36a283febe646afcc6f9c9bcbd0ed5abf46a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347792"
---
# <a name="managedappregistration-resource-type"></a>Tipo de recurso managedAppRegistration

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
|deviceTag|String|Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo. No garantiza que las aplicaciones se relacionen en todas las condiciones.|
|deviceName|Cadena|Nombre del dispositivo host|
|flaggedReasons|colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)|Cero o más razones por las que se ha marcado el registro de una aplicación. Por ejemplo, una aplicación que se ejecuta en el dispositivo liberado|
|userId|String|El identificador de usuario al que pertenece este registro de la aplicación.|
|appIdentifier|[mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)|El identificador del paquete de aplicación|
|id|String|Clave de la entidad.|
|version|String|Versión de la entidad.|

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


<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-mam-managedappregistration.md/microsoft.graph.managedAppRegistration/flaggedReasons:
      Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->
