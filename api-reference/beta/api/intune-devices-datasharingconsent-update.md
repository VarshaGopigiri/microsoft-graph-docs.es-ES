---
title: Actualizar dataSharingConsent
description: Actualizar las propiedades de un objeto dataSharingConsent.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8e2486b6d1900369bae17853be399eccb4fe8740
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816439"
---
# <a name="update-datasharingconsent"></a>Actualizar dataSharingConsent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .
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
PATCH /deviceManagement/dataSharingConsents/{dataSharingConsentId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [dataSharingConsent](../resources/intune-devices-datasharingconsent.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El consentimiento de uso compartido de datos Id.|
|nombreDescriptivoDeServicio|Cadena|El nombre para mostrar del flujo de trabajo del servicio|
|termsUrl|Cadena|El TermsUrl para los datos de uso compartido de consentimiento|
|concedido|Booleano|El estado de concedidos para los datos de uso compartido de consentimiento|
|grantDateTime|DateTimeOffset|Esta cuenta se le conceden el consentimiento de tiempo|
|grantedByUpn|Cadena|El Upn del usuario que concederse el consentimiento para esta cuenta|
|grantedByUserId|Cadena|El identificador de usuario del usuario que concederse el consentimiento para esta cuenta|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/dataSharingConsents/{dataSharingConsentId}
Content-type: application/json
Content-length: 276

{
  "serviceDisplayName": "Service Display Name value",
  "termsUrl": "https://example.com/termsUrl/",
  "granted": true,
  "grantDateTime": "2016-12-31T23:59:55.7154191-08:00",
  "grantedByUpn": "Granted By Upn value",
  "grantedByUserId": "Granted By User Id value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 382

{
  "@odata.type": "#microsoft.graph.dataSharingConsent",
  "id": "333387f7-87f7-3333-f787-3333f7873333",
  "serviceDisplayName": "Service Display Name value",
  "termsUrl": "https://example.com/termsUrl/",
  "granted": true,
  "grantDateTime": "2016-12-31T23:59:55.7154191-08:00",
  "grantedByUpn": "Granted By Upn value",
  "grantedByUserId": "Granted By User Id value"
}
```





