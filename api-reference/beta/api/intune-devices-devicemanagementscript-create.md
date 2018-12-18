---
title: Crear deviceManagementScript
description: Crear un nuevo objeto deviceManagementScript.
author: tfitzmac
ms.openlocfilehash: 862b9c3ba50f879e92e47b50e6efaf0bcf41927a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315438"
---
# <a name="create-devicemanagementscript"></a>Crear deviceManagementScript

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un nuevo objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .
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
POST /deviceManagement/deviceManagementScripts
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto deviceManagementScript.

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el deviceManagementScript.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para la secuencia de comandos de administración de dispositivos.|
|displayName|String|Nombre de la secuencia de comandos de administración de dispositivos.|
|descripción|String|Descripción opcional de la secuencia de comandos de administración de dispositivos.|
|runSchedule|[runSchedule](../resources/intune-devices-runschedule.md)|El intervalo para ejecutar la secuencia de comandos. Si no ha definido la secuencia de comandos se ejecutará una vez|
|scriptContent|Binario|El contenido de la secuencia de comandos.|
|createdDateTime|DateTimeOffset|La fecha y hora de que creación de la secuencia de comandos de administración de dispositivos.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de que última modificación de la secuencia de comandos de administración de dispositivos.|
|runAsAccount|[runAsAccountType](../resources/intune-shared-runasaccounttype.md)|Indica el tipo de la secuencia de comandos de administración de dispositivos se ejecuta en el contexto de ejecución. Los valores posibles son: `system` y `user`.|
|enforceSignatureCheck|Boolean|Indicar si se debe comprobar la firma de la secuencia de comandos.|
|fileName|String|Nombre de archivo de secuencia de comandos.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts
Content-type: application/json
Content-length: 422

{
  "@odata.type": "#microsoft.graph.deviceManagementScript",
  "displayName": "Display Name value",
  "description": "Description value",
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  },
  "scriptContent": "c2NyaXB0Q29udGVudA==",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "runAsAccount": "user",
  "enforceSignatureCheck": true,
  "fileName": "File Name value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 530

{
  "@odata.type": "#microsoft.graph.deviceManagementScript",
  "id": "59ea4525-4525-59ea-2545-ea592545ea59",
  "displayName": "Display Name value",
  "description": "Description value",
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  },
  "scriptContent": "c2NyaXB0Q29udGVudA==",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "runAsAccount": "user",
  "enforceSignatureCheck": true,
  "fileName": "File Name value"
}
```





