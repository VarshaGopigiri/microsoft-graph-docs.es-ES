---
title: Crear vppToken
description: Crea un nuevo objeto vppToken.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fc4313f5e1d83a8ed202eac47ed070cf8dc1804c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914917"
---
# <a name="create-vpptoken"></a>Crear vppToken

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crea un nuevo objeto [vppToken](../resources/intune-onboarding-vpptoken.md).
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
POST /deviceAppManagement/vppTokens
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto vppToken.

En la tabla siguiente se muestran las propiedades necesarias para crear el vppToken.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Esto se genera automáticamente cuando se crea el appleVolumePurchaseProgramToken. Es la clave de la entidad.|
|organizationName|Cadena|Organización asociada al token del Programa de Compras por Volumen de Apple|
|vppTokenAccountType|[vppTokenAccountType](../resources/intune-shared-vpptokenaccounttype.md)|Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado. Los valores posibles son: `business` y `education`. Los valores posibles son: `business` y `education`.|
|Id. de Apple|Cadena|Identificador de Apple asociado al token del Programa de compras por volumen de Apple especificado.|
|expirationDateTime|DateTimeOffset|La fecha y hora de vencimiento del token del Programa de compras por volumen de Apple.|
|lastSyncDateTime|DateTimeOffset|La última vez que se realizó la sincronización de una aplicación con el servicio del programa de compras por volumen de Apple utilizando el token de ese programa de compras.|
|token|Cadena|La cadena del token del programa de compras por volumen de Apple descargada desde ese programa de compras.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de modificación asociada con el token del Programa de compras por volumen de Apple.|
|estado|[vppTokenState](../resources/intune-onboarding-vpptokenstate.md)|Estado actual del token del Programa de compras por volumen de Apple. Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`. Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.|
|tokenActionResults|colección de [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)|La colección de Estados de las acciones que se realiza en el Token de programa de compra de Apple por volumen.|
|lastSyncStatus|[vppTokenSyncStatus](../resources/intune-onboarding-vpptokensyncstatus.md)|Estado de sincronización actual de la última sincronización de la aplicación que se activó con el Token del programa de compras por volumen de Apple. Los valores posibles son: `none`, `inProgress`, `completed` y `failed`. Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.|
|automaticallyUpdateApps|Booleano|Si las aplicaciones para el token VPP se actualizarán automáticamente o no.|
|countryOrRegion|Cadena|Si las aplicaciones para el token VPP se actualizarán automáticamente o no.|
|dataSharingConsentGranted|Booleano|Concede de consentimiento para uso compartido con el programa de compra de Apple por volumen de datos.|
|displayName|Cadena|Un administrador especifica el nombre descriptivo del token.|
|locationName|Cadena|Ubicación de token devuelto desde VPP de Apple.|
|claimTokenManagementFromExternalMdm|Booleano|Administración de consentimiento para permitir que afirma token administración de MDM. externo|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [vppToken](../resources/intune-onboarding-vpptoken.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/vppTokens
Content-type: application/json
Content-length: 1004

{
  "@odata.type": "#microsoft.graph.vppToken",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "tokenActionResults": [
    {
      "@odata.type": "microsoft.graph.vppTokenActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value",
  "dataSharingConsentGranted": true,
  "displayName": "Display Name value",
  "locationName": "Location Name value",
  "claimTokenManagementFromExternalMdm": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1053

{
  "@odata.type": "#microsoft.graph.vppToken",
  "id": "9ceb2f92-2f92-9ceb-922f-eb9c922feb9c",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "tokenActionResults": [
    {
      "@odata.type": "microsoft.graph.vppTokenActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value",
  "dataSharingConsentGranted": true,
  "displayName": "Display Name value",
  "locationName": "Location Name value",
  "claimTokenManagementFromExternalMdm": true
}
```





