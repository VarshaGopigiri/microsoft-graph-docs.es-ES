---
title: Actualizar windowsManagementAppHealthState
description: Actualizar las propiedades de un objeto windowsManagementAppHealthState.
author: tfitzmac
ms.openlocfilehash: 72beed52f76531aacd3ba0c48e350954bd4ac525
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309089"
---
# <a name="update-windowsmanagementapphealthstate"></a>Actualizar windowsManagementAppHealthState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementManagedDevices.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsManagementApp/healthStates/{windowsManagementAppHealthStateId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para el estado de mantenimiento de aplicación de administración de Windows|
|healthState|[healthState](../resources/intune-devices-healthstate.md)|Estado de mantenimiento de aplicación de administración de Windows. Los valores posibles son: `unknown`, `healthy` y `unhealthy`.|
|installedVersion|String|La versión instalada de aplicación de administración de Windows.|
|lastCheckInDateTime|DateTimeOffset|Aplicación de administración de Windows última hora de protección.|
|deviceName|String|Nombre del dispositivo con Windows está instalada la aplicación de administración.|
|deviceOSVersion|String|Versión de sistema operativo de Windows 10 del dispositivo con Windows está instalada la aplicación de administración.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/windowsManagementApp/healthStates/{windowsManagementAppHealthStateId}
Content-type: application/json
Content-length: 230

{
  "healthState": "healthy",
  "installedVersion": "Installed Version value",
  "lastCheckInDateTime": "2016-12-31T23:59:56.413532-08:00",
  "deviceName": "Device Name value",
  "deviceOSVersion": "Device OSVersion value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 349

{
  "@odata.type": "#microsoft.graph.windowsManagementAppHealthState",
  "id": "5c7e50fb-50fb-5c7e-fb50-7e5cfb507e5c",
  "healthState": "healthy",
  "installedVersion": "Installed Version value",
  "lastCheckInDateTime": "2016-12-31T23:59:56.413532-08:00",
  "deviceName": "Device Name value",
  "deviceOSVersion": "Device OSVersion value"
}
```





