---
title: tipo de recurso embeddedSIMDeviceState
description: Describe el estado de implementación incrustado de código activación de SIM en relación con un dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 15e969037a93ee11c300f7b18b0c8afcb36d0ce1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881518"
---
# <a name="embeddedsimdevicestate-resource-type"></a>tipo de recurso embeddedSIMDeviceState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Describe el estado de implementación incrustado de código activación de SIM en relación con un dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista embeddedSIMDeviceStates](../api/intune-esim-embeddedsimdevicestate-list.md)|colección de [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|Propiedades de la lista y relaciones de los objetos [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) .|
|[Obtener embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-get.md)|[embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|Leer las propiedades y las relaciones del objeto [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) .|
|[Crear embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-create.md)|[embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|Crear un nuevo objeto [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) .|
|[Eliminar embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-delete.md)|Ninguno|Elimina un [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md).|
|[Actualizar embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-update.md)|[embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|Actualizar las propiedades de un objeto [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único para el estado del dispositivo SIM incrustado. Valor asignado al crear generada por el sistema.|
|createdDateTime|DateTimeOffset|La hora en que se creó el estado del dispositivo SIM incrustado. Servicio generado al lado.|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez el estado del dispositivo SIM incrustado. Se actualizó el lado de servicio.|
|lastSyncDateTime|DateTimeOffset|El tiempo que el dispositivo SIM incrustado protegida por última vez. Se actualizó el lado de servicio.|
|universalIntegratedCircuitCardIdentifier|Cadena|La Universal circuito integrado tarjeta de identificador (UICCID) que identifica el hardware en el que es un perfil que se va a implementar.|
|deviceName|Cadena|Nombre de dispositivo al que estaba la suscripción a aprovisiona a JOE de escritorio, por ejemplo|
|userName|Cadena|Nombre de usuario que se aprovisionó la suscripción como, por ejemplo, joe@contoso.com|
|state|[embeddedSIMDeviceStateValue](../resources/intune-esim-embeddedsimdevicestatevalue.md)|El estado de la operación de perfil aplicada al dispositivo. Los valores posibles son: `notEvaluated`, `failed`, `installing`, `installed`, `deleting`, `error`, `deleted` y `removedByUser`.|
|stateDetails|Cadena|Descripción del estado de aprovisionamiento de la cadena.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.embeddedSIMDeviceState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.embeddedSIMDeviceState",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "universalIntegratedCircuitCardIdentifier": "String",
  "deviceName": "String",
  "userName": "String",
  "state": "String",
  "stateDetails": "String"
}
```





