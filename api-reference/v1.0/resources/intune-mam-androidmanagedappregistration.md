---
title: Tipo de recurso androidManagedAppRegistration
description: Representa los detalles de sincronización de una aplicación para Android, con capacidades de administración, para un usuario específico.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 234ee00dd6d2a84720358a889466fd1763e3c80f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970013"
---
# <a name="androidmanagedappregistration-resource-type"></a>Tipo de recurso androidManagedAppRegistration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa los detalles de sincronización de una aplicación para Android, con capacidades de administración, para un usuario específico.
El recurso ManagedAppRegistration representa los detalles de una aplicación, con capacidad de administración, usado por un miembro de la organización.

Hereda de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidManagedAppRegistrations](../api/intune-mam-androidmanagedappregistration-list.md)|Colección [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md)|Enumere las propiedades y las relaciones de los objetos [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).|
|[Obtener androidManagedAppRegistration](../api/intune-mam-androidmanagedappregistration-get.md)|[androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md)|Lea las propiedades y las relaciones del objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).|
|[Crear androidManagedAppRegistration](../api/intune-mam-androidmanagedappregistration-create.md)|[androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md)|Cree un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|lastSyncDateTime|DateTimeOffset|Fecha y hora de la última sincronización de la aplicación con el servicio de administración. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|applicationVersion|String|Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|managementSdkVersion|String|Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|platformVersion|String|Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|deviceType|String|Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|deviceTag|String|Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo. No garantiza que las aplicaciones se relacionen en todas las condiciones. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|deviceName|String|Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|flaggedReasons|colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)|Cero o más razones por las que se ha marcado el registro de una aplicación. Por ejemplo, una aplicación que se ejecuta en un dispositivo liberado. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|userId|String|Identificador de usuario al que pertenece este registro de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|appIdentifier|[mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)|Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|id|String|Clave de la entidad. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|
|version|String|Versión de la entidad. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|

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
  "@odata.type": "microsoft.graph.androidManagedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
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
    "packageId": "String"
  },
  "id": "String (identifier)",
  "version": "String"
}
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-mam-androidmanagedappregistration.md/microsoft.graph.androidManagedAppRegistration/flaggedReasons:
      Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->



