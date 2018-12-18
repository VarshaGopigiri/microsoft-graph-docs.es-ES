---
title: Actualizar depOnboardingSetting
description: Actualizar las propiedades de un objeto depOnboardingSetting.
author: tfitzmac
ms.openlocfilehash: d4a50c485da98a182562ca5bd353d71dd854b4f4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326785"
---
# <a name="update-deponboardingsetting"></a>Actualizar depOnboardingSetting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementServiceConfig.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|UUID para el objeto|
|appleIdentifier|String|El identificador de Apple se utiliza para obtener el token actual.|
|tokenExpirationDateTime|DateTimeOffset|Cuando caduca el token.|
|lastModifiedDateTime|DateTimeOffset|Cuando el servicio fue onboarded.|
|lastSuccessfulSyncDateTime|DateTimeOffset|Cuando el syned último servicio con Intune|
|lastSyncTriggeredDateTime|DateTimeOffset|Cuando Intune solicitada por última vez una sincronización.|
|shareTokenWithSchoolDataSyncService|Boolean|Si el símbolo (token) de la característica Dep compartir está habilitada o no con el servicio de sincronización de datos de School.|
|lastSyncErrorCode|Int32|Código de error que informa Apple durante la última sincronización de la característica dep.|
|TokenType en|[depTokenType](../resources/intune-enrollment-deptokentype.md)|Obtiene o establece el tipo de símbolo (token) de la característica Dep. Los valores posibles son: `none`, `dep` y `appleSchoolManager`.|
|tokenName|String|Nombre descriptivo para la característica Dep símbolo (token)|
|syncedDeviceCount|Int32|Obtiene sincronizado recuento de dispositivo|
|defaultProfileDisplayName|String|Obtiene sincronizado recuento de dispositivo|
|dataSharingConsentGranted|Boolean|Concede de consentimiento para uso compartido con Apple Dep servicio de datos|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}
Content-type: application/json
Content-length: 589

{
  "appleIdentifier": "Apple Identifier value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "lastSuccessfulSyncDateTime": "2017-01-01T00:03:28.120883-08:00",
  "lastSyncTriggeredDateTime": "2017-01-01T00:00:02.0916369-08:00",
  "shareTokenWithSchoolDataSyncService": true,
  "lastSyncErrorCode": 1,
  "tokenType": "dep",
  "tokenName": "Token Name value",
  "syncedDeviceCount": 1,
  "defaultProfileDisplayName": "Default Profile Display Name value",
  "dataSharingConsentGranted": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 697

{
  "@odata.type": "#microsoft.graph.depOnboardingSetting",
  "id": "40342229-2229-4034-2922-344029223440",
  "appleIdentifier": "Apple Identifier value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "lastSuccessfulSyncDateTime": "2017-01-01T00:03:28.120883-08:00",
  "lastSyncTriggeredDateTime": "2017-01-01T00:00:02.0916369-08:00",
  "shareTokenWithSchoolDataSyncService": true,
  "lastSyncErrorCode": 1,
  "tokenType": "dep",
  "tokenName": "Token Name value",
  "syncedDeviceCount": 1,
  "defaultProfileDisplayName": "Default Profile Display Name value",
  "dataSharingConsentGranted": true
}
```





