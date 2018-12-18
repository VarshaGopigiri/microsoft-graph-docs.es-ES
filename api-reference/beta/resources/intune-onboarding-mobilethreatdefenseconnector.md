---
title: Tipo de recurso mobileThreatDefenseConnector
description: Entidad que representa una conexión a un partner de Mobile Threat Defense.
author: tfitzmac
ms.openlocfilehash: f47942cece4653de20b2c954249545f5dd691e3b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306632"
---
# <a name="mobilethreatdefenseconnector-resource-type"></a>Tipo de recurso mobileThreatDefenseConnector

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que representa una conexión a un partner de Mobile Threat Defense.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileThreatDefenseConnectors](../api/intune-onboarding-mobilethreatdefenseconnector-list.md)|Colección [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md)|Enumere las propiedades y las relaciones de los objetos [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).|
|[Obtener mobileThreatDefenseConnector](../api/intune-onboarding-mobilethreatdefenseconnector-get.md)|[mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md)|Lea las propiedades y las relaciones del objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).|
|[Crear mobileThreatDefenseConnector](../api/intune-onboarding-mobilethreatdefenseconnector-create.md)|[mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md)|Cree un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).|
|[Eliminar mobileThreatDefenseConnector](../api/intune-onboarding-mobilethreatdefenseconnector-delete.md)|Ninguna|Elimina un [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).|
|[Actualizar mobileThreatDefenseConnector](../api/intune-onboarding-mobilethreatdefenseconnector-update.md)|[mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md)|Actualice las propiedades de un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Todavía no documentado|
|lastHeartbeatDateTime|DateTimeOffset|Fecha y hora del último latido recibido del Partner de sincronización de datos|
|partnerState|[mobileThreatPartnerTenantState](../resources/intune-onboarding-mobilethreatpartnertenantstate.md)|Estado de socio de sincronización de datos para esta cuenta. Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.|
|androidEnabled|Boolean|Para Android, establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.|
|iosEnabled|Boolean|Para iOS, obtiene o establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.|
|windowsEnabled|Boolean|Para Windows, obtener o establecer si se deben usar datos desde el asociado de sincronización de datos durante las evaluaciones de cumplimiento|
|macEnabled|Boolean|Para Mac, obtener o establecer si se deben usar datos desde el asociado de sincronización de datos durante las evaluaciones de cumplimiento|
|androidDeviceBlockedOnMissingPartnerData|Boolean|Para Android, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.|
|iosDeviceBlockedOnMissingPartnerData|Boolean|Para iOS, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.|
|windowsDeviceBlockedOnMissingPartnerData|Boolean|Para Windows, establecer si Intune debe recibir datos desde el asociado de sincronización de datos antes de marcar un dispositivo compatible con|
|macDeviceBlockedOnMissingPartnerData|Boolean|Para Mac, obtener o establecer si Intune debe recibir datos desde el asociado de sincronización de datos antes de marcar un dispositivo compatible con|
|partnerUnsupportedOsVersionBlocked|Boolean|Obtiene o establece si se deben bloquear los dispositivos de las plataformas habilitadas que no cumplan los requisitos de versión mínima.|
|partnerUnresponsivenessThresholdInDays|Int32|Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.|
|allowPartnerToCollectIOSApplicationMetadata|Boolean|Para los dispositivos IOS, permite que el Administrador de configuración si el socio de sincronización de datos también puede recopilar los metadatos sobre las aplicaciones instaladas desde Intune|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileThreatDefenseConnector"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "String (identifier)",
  "lastHeartbeatDateTime": "String (timestamp)",
  "partnerState": "String",
  "androidEnabled": true,
  "iosEnabled": true,
  "windowsEnabled": true,
  "macEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "windowsDeviceBlockedOnMissingPartnerData": true,
  "macDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 1024,
  "allowPartnerToCollectIOSApplicationMetadata": true
}
```





