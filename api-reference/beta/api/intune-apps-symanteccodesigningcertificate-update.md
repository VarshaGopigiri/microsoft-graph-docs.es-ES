---
title: Actualizar symantecCodeSigningCertificate
description: Actualizar las propiedades de un objeto symantecCodeSigningCertificate.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7d95627e9a2c678097be0c3cb818a03906e8a06f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824741"
---
# <a name="update-symanteccodesigningcertificate"></a>Actualizar symantecCodeSigningCertificate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementApps.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/symantecCodeSigningCertificate
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave de la entidad.|
|content|Binario|El certificado de firma de código de Symantec de Windows en el formato de datos sin procesar.|
|status|[certificateStatus](../resources/intune-apps-certificatestatus.md)|El estado de Cert aprovisiona o no configurado. Los valores posibles son: `notProvisioned` y `provisioned`.|
|password|String|La contraseña requerida para el archivo .pfx.|
|subjectName|cadena|El nombre de sujeto para el certificado.|
|subject|Cadena|El valor de asunto para el certificado.|
|issuerName|Cadena|El nombre para el certificado del emisor.|
|emisor|Cadena|El valor de emisor para el certificado.|
|expirationDateTime|DateTimeOffset|La fecha de caducidad del certificado.|
|uploadDateTime|DateTimeOffset|El tipo del certificado de firma de código como Symantec Cert.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/symantecCodeSigningCertificate
Content-type: application/json
Content-length: 352

{
  "content": "Y29udGVudA==",
  "status": "provisioned",
  "password": "Password value",
  "subjectName": "Subject Name value",
  "subject": "Subject value",
  "issuerName": "Issuer Name value",
  "issuer": "Issuer value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 470

{
  "@odata.type": "#microsoft.graph.symantecCodeSigningCertificate",
  "id": "00ffe83e-e83e-00ff-3ee8-ff003ee8ff00",
  "content": "Y29udGVudA==",
  "status": "provisioned",
  "password": "Password value",
  "subjectName": "Subject Name value",
  "subject": "Subject value",
  "issuerName": "Issuer Name value",
  "issuer": "Issuer value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00"
}
```





