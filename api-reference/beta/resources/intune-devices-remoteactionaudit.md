---
title: tipo de recurso remoteActionAudit
description: Informe de remotas acciones iniciadas en los dispositivos que pertenecen a un inquilino determinados.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ad583f13311e5baece70c5ec28ca8f7c73f5349e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972596"
---
# <a name="remoteactionaudit-resource-type"></a>tipo de recurso remoteActionAudit

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Informe de remotas acciones iniciadas en los dispositivos que pertenecen a un inquilino determinados.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista remoteActionAudits](../api/intune-devices-remoteactionaudit-list.md)|colección de [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md)|Propiedades de la lista y relaciones de los objetos [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) .|
|[Obtener remoteActionAudit](../api/intune-devices-remoteactionaudit-get.md)|[remoteActionAudit](../resources/intune-devices-remoteactionaudit.md)|Leer las propiedades y las relaciones del objeto [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) .|
|[Crear remoteActionAudit](../api/intune-devices-remoteactionaudit-create.md)|[remoteActionAudit](../resources/intune-devices-remoteactionaudit.md)|Crear un nuevo objeto [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) .|
|[Eliminar remoteActionAudit](../api/intune-devices-remoteactionaudit-delete.md)|Ninguno|Elimina un [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md).|
|[Actualizar remoteActionAudit](../api/intune-devices-remoteactionaudit-update.md)|[remoteActionAudit](../resources/intune-devices-remoteactionaudit.md)|Actualizar las propiedades de un objeto [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|ID de informe.|
|deviceDisplayName|String|Nombre del dispositivo Intune.|
|userName|Cadena|\[en desuso\] use InitiatedByUserPrincipalName en su lugar.|
|initiatedByUserPrincipalName|Cadena|Usuario que inició la acción de dispositivo, formato es UPN.|
|action|[remoteAction](../resources/intune-devices-remoteaction.md)|El nombre de la acción. Los valores posibles son: `unknown`, `factoryReset`, `removeCompanyData`, `resetPasscode`, `remoteLock`, `enableLostMode`, `disableLostMode`, `locateDevice`, `rebootNow`, `recoverPasscode`, `cleanWindowsDevice`, `logoutSharedAppleDeviceActiveUser`, `quickScan`, `fullScan`, `windowsDefenderUpdateSignatures`, `factoryResetKeepEnrollmentData`, `updateDeviceAccount`, `automaticRedeployment`, `shutDown` .|
|requestDateTime|DateTimeOffset|Hora en que se emitió la acción, dado en UTC.|
|deviceOwnerUserPrincipalName|Cadena|UPN del propietario del dispositivo.|
|deviceIMEI|Cadena|IMEI del dispositivo.|
|actionState|[actionState](../resources/intune-shared-actionstate.md)|Estado de acción. Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.remoteActionAudit"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.remoteActionAudit",
  "id": "String (identifier)",
  "deviceDisplayName": "String",
  "userName": "String",
  "initiatedByUserPrincipalName": "String",
  "action": "String",
  "requestDateTime": "String (timestamp)",
  "deviceOwnerUserPrincipalName": "String",
  "deviceIMEI": "String",
  "actionState": "String"
}
```





