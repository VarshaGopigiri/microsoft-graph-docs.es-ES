---
title: tipo de recurso iosLobAppProvisioningConfiguration
description: En este tema se ofrece descripciones de los métodos declarados, propiedades y relaciones expuestas por el recurso de configuración de aprovisionamiento de aplicaciones de Lob de IOS.
ms.openlocfilehash: 07ae7c53f481aa6f2c9ad083881752591ab421fd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087178"
---
# <a name="ioslobappprovisioningconfiguration-resource-type"></a>tipo de recurso iosLobAppProvisioningConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

En este tema se ofrece descripciones de los métodos declarados, propiedades y relaciones expuestas por el recurso de configuración de aprovisionamiento de aplicaciones de Lob de IOS.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista iosLobAppProvisioningConfigurations](../api/intune-apps-ioslobappprovisioningconfiguration-list.md)|colección de [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md)|Propiedades de la lista y relaciones de los objetos [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) .|
|[Obtener iosLobAppProvisioningConfiguration](../api/intune-apps-ioslobappprovisioningconfiguration-get.md)|[iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md)|Leer las propiedades y las relaciones del objeto [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) .|
|[Crear iosLobAppProvisioningConfiguration](../api/intune-apps-ioslobappprovisioningconfiguration-create.md)|[iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md)|Crear un nuevo objeto [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) .|
|[Eliminar iosLobAppProvisioningConfiguration](../api/intune-apps-ioslobappprovisioningconfiguration-delete.md)|Ninguno|Elimina un [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md).|
|[Actualizar iosLobAppProvisioningConfiguration](../api/intune-apps-ioslobappprovisioningconfiguration-update.md)|[iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md)|Actualizar las propiedades de un objeto [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) .|
|[Acción assign](../api/intune-apps-ioslobappprovisioningconfiguration-assign.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|expirationDateTime|DateTimeOffset|Fecha de caducidad opcional de perfiles y la hora.|
|payloadFileName|String|Nombre de archivo de carga (*.mobileprovision | *.xml).|
|carga útil|Binario|Carga útil. (Matriz de bytes codificada UTF8)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|groupAssignments|colección de [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md)|Las asignaciones de grupo asociado.|
|asignaciones|colección de [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md)|Las asignaciones de grupo asociado para IosLobAppProvisioningConfiguration.|
|deviceStatuses|colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md)|La lista de los Estados de instalación de dispositivo para esta configuración de la aplicación móvil.|
|userStatuses|Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)|La lista de los Estados de instalación de usuario para esta configuración de la aplicación móvil.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosLobAppProvisioningConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfiguration",
  "id": "String (identifier)",
  "expirationDateTime": "String (timestamp)",
  "payloadFileName": "String",
  "payload": "binary",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```





