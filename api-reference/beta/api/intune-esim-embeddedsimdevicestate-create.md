---
title: Crear embeddedSIMDeviceState
description: Crear un nuevo objeto embeddedSIMDeviceState.
author: tfitzmac
ms.openlocfilehash: bacf4e0beb240a9c6e60792c7d2a853ac37dcce4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340974"
---
# <a name="create-embeddedsimdevicestate"></a>Crear embeddedSIMDeviceState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un nuevo objeto [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/deviceStates
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto embeddedSIMDeviceState.

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el embeddedSIMDeviceState.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para el estado del dispositivo SIM incrustado. Valor asignado al crear generada por el sistema.|
|createdDateTime|DateTimeOffset|La hora en que se creó el estado del dispositivo SIM incrustado. Servicio generado al lado.|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez el estado del dispositivo SIM incrustado. Se actualizó el lado de servicio.|
|lastSyncDateTime|DateTimeOffset|El tiempo que el dispositivo SIM incrustado protegida por última vez. Se actualizó el lado de servicio.|
|universalIntegratedCircuitCardIdentifier|String|La Universal circuito integrado tarjeta de identificador (UICCID) que identifica el hardware en el que es un perfil que se va a implementar.|
|deviceName|String|Nombre de dispositivo al que estaba la suscripción a aprovisiona a JOE de escritorio, por ejemplo|
|userName|String|Nombre de usuario que se aprovisionó la suscripción como, por ejemplo, joe@contoso.com|
|state|[embeddedSIMDeviceStateValue](../resources/intune-esim-embeddedsimdevicestatevalue.md)|El estado de la operación de perfil aplicada al dispositivo. Los valores posibles son: `notEvaluated`, `failed`, `installing`, `installed`, `deleting`, `error`, `deleted` y `removedByUser`.|
|stateDetails|String|Descripción del estado de aprovisionamiento de la cadena.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/deviceStates
Content-type: application/json
Content-length: 361

{
  "@odata.type": "#microsoft.graph.embeddedSIMDeviceState",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "universalIntegratedCircuitCardIdentifier": "Universal Integrated Circuit Card Identifier value",
  "deviceName": "Device Name value",
  "userName": "User Name value",
  "state": "failed",
  "stateDetails": "State Details value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 529

{
  "@odata.type": "#microsoft.graph.embeddedSIMDeviceState",
  "id": "908884a3-84a3-9088-a384-8890a3848890",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "universalIntegratedCircuitCardIdentifier": "Universal Integrated Circuit Card Identifier value",
  "deviceName": "Device Name value",
  "userName": "User Name value",
  "state": "failed",
  "stateDetails": "State Details value"
}
```





