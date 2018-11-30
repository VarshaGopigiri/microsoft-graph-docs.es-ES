---
title: tipo de recurso symantecCodeSigningCertificate
description: Todavía no documentado
ms.openlocfilehash: f867f5bf6b0cad43f32dcc5ad9320421eee6d5c5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086387"
---
# <a name="symanteccodesigningcertificate-resource-type"></a>tipo de recurso symantecCodeSigningCertificate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener symantecCodeSigningCertificate](../api/intune-apps-symanteccodesigningcertificate-get.md)|[symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md)|Leer las propiedades y las relaciones del objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .|
|[Actualizar symantecCodeSigningCertificate](../api/intune-apps-symanteccodesigningcertificate-update.md)|[symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md)|Actualizar las propiedades de un objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave de la entidad.|
|content|Binario|El certificado de firma de código de Symantec de Windows en el formato de datos sin procesar.|
|status|[certificateStatus](../resources/intune-apps-certificatestatus.md)|El estado de Cert aprovisiona o no configurado. Los valores posibles son: `notProvisioned` y `provisioned`.|
|password|String|La contraseña requerida para el archivo .pfx.|
|subjectName|cadena|El nombre de sujeto para el certificado.|
|subject|String|El valor de asunto para el certificado.|
|issuerName|String|El nombre para el certificado del emisor.|
|emisor|String|El valor de emisor para el certificado.|
|expirationDateTime|DateTimeOffset|La fecha de caducidad del certificado.|
|uploadDateTime|DateTimeOffset|El tipo del certificado de firma de código como Symantec Cert.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.symantecCodeSigningCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.symantecCodeSigningCertificate",
  "id": "String (identifier)",
  "content": "binary",
  "status": "String",
  "password": "String",
  "subjectName": "String",
  "subject": "String",
  "issuerName": "String",
  "issuer": "String",
  "expirationDateTime": "String (timestamp)",
  "uploadDateTime": "String (timestamp)"
}
```





