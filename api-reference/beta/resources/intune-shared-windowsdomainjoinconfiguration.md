---
title: tipo de recurso windowsDomainJoinConfiguration
description: Configuración de dispositivo de unirse a un dominio Windows.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b2184233549cdf52c3708de2a35c5c647e9beba3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990757"
---
# <a name="windowsdomainjoinconfiguration-resource-type"></a>tipo de recurso windowsDomainJoinConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de dispositivo de unirse a un dominio Windows.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windowsDomainJoinConfigurations](../api/intune-shared-windowsdomainjoinconfiguration-list.md)|colección de [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md)|Propiedades de la lista y relaciones de los objetos [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .|
|[Obtener windowsDomainJoinConfiguration](../api/intune-shared-windowsdomainjoinconfiguration-get.md)|[windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md)|Leer las propiedades y las relaciones del objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .|
|[Crear windowsDomainJoinConfiguration](../api/intune-shared-windowsdomainjoinconfiguration-create.md)|[windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md)|Crear un nuevo objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .|
|[Eliminar windowsDomainJoinConfiguration](../api/intune-shared-windowsdomainjoinconfiguration-delete.md)|Ninguno|Elimina un [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md).|Eliminar un objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .|
|[Actualizar windowsDomainJoinConfiguration](../api/intune-shared-windowsdomainjoinconfiguration-update.md)|[windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md)|Actualizar las propiedades de un objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|**Configuración de dispositivos**|
|activeDirectoryDomainName|Cadena|Nombre de dominio de Active Directory para unirse a.|
|computerNameStaticPrefix|Cadena|Prefijo fijo que se usará para el nombre del equipo.|
|computerNameSuffixRandomCharCount|Int32|Genera de forma dinámica los caracteres que se utilizan como sufijo de nombre de equipo. Valores válidos 3 a 14|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|organizationalUnit|Cadena|Unidad organizativa (OU) donde se creará la cuenta de equipo. Si este parámetro es NULL, se usará el contenedor de objetos de equipo conocido como publicado en el dominio.|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Booleano|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|**Configuración de dispositivos**|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|groupAssignments|colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|networkAccessConfigurations|Colección [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|Referencia a las configuraciones de dispositivos necesarios para la conectividad de red|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Estado de instalación de configuración del dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.  Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Objetos de respuesta contendrá las propiedades relevantes para el contexto de la llamada.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsDomainJoinConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsDomainJoinConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "computerNameStaticPrefix": "String",
  "computerNameSuffixRandomCharCount": 1024,
  "activeDirectoryDomainName": "String"
}
```



