---
title: Actualizar deviceConfigurationDeviceOverview
description: Actualice las propiedades de un objeto deviceConfigurationDeviceOverview.
ms.openlocfilehash: 7eecc3e7871ae1ec8891c5f3f8c7dfde9d517c00
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030663"
---
# <a name="update-deviceconfigurationdeviceoverview"></a>Actualizar deviceConfigurationDeviceOverview

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).
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
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|pendingCount|Int32|Número de dispositivos pendientes|
|notApplicableCount|Int32|Número de dispositivos no aplicables|
|successCount|Int32|Número de dispositivos correctos|
|errorCount|Int32|Número de dispositivos con error|
|failedCount|Int32|Número de dispositivos erróneos|
|lastUpdateDateTime|DateTimeOffset|Última hora de actualización|
|configurationVersion|Int32|Versión de la directiva para esa información general|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
Content-type: application/json
Content-length: 284

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 333

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
  "id": "62d48e3a-8e3a-62d4-3a8e-d4623a8ed462",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```



