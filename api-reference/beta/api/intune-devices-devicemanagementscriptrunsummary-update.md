---
title: Actualizar deviceManagementScriptRunSummary
description: Actualizar las propiedades de un objeto deviceManagementScriptRunSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d2a0ba2a7dfbd44cd5e756010239caee285fe090
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954704"
---
# <a name="update-devicemanagementscriptrunsummary"></a>Actualizar deviceManagementScriptRunSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) .
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
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/runSummary
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la secuencia de comandos de administración de dispositivo ejecute entidad resumen.|
|successDeviceCount|Int32|Recuento de éxito de dispositivo.|
|errorDeviceCount|Int32|Recuento de error de dispositivo.|
|successUserCount|Int32|Recuento de usuario correcto.|
|errorUserCount|Int32|Recuento de usuario de error.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/runSummary
Content-type: application/json
Content-length: 108

{
  "successDeviceCount": 2,
  "errorDeviceCount": 0,
  "successUserCount": 0,
  "errorUserCount": 14
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 228

{
  "@odata.type": "#microsoft.graph.deviceManagementScriptRunSummary",
  "id": "514d5d38-5d38-514d-385d-4d51385d4d51",
  "successDeviceCount": 2,
  "errorDeviceCount": 0,
  "successUserCount": 0,
  "errorUserCount": 14
}
```





