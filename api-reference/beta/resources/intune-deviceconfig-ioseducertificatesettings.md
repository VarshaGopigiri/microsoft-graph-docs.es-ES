---
title: tipo de recurso iosEduCertificateSettings
description: Confianza certificados raíz y PFX para iOS EDU.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bf6b0da4d3ff7af562ae99e81e10f52351bd735d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822081"
---
# <a name="ioseducertificatesettings-resource-type"></a>tipo de recurso iosEduCertificateSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Confianza certificados raíz y PFX para iOS EDU.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|trustedRootCertificate|Binario|Certificado raíz de confianza.|
|certFileName|Cadena|Nombre de archivo para mostrar en la interfaz de usuario.|
|certificationAuthority|Cadena|Entidad de certificación PKCS.|
|certificationAuthorityName|Cadena|Nombre de la autoridad de certificación PKCS.|
|certificateTemplateName|Cadena|Nombre de la plantilla de certificado PKCS.|
|renewalThresholdPercentage|Int32|Porcentaje de umbral de renovación de certificado. Valores válidos de 1 a 99|
|certificateValidityPeriodValue|Int32|Valor para el período de validez del certificado.|
|certificateValidityPeriodScale|[certificateValidityPeriodScale](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|Escala para el período de validez del certificado. Los valores posibles son: `days`, `months` y `years`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosEduCertificateSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosEduCertificateSettings",
  "trustedRootCertificate": "binary",
  "certFileName": "String",
  "certificationAuthority": "String",
  "certificationAuthorityName": "String",
  "certificateTemplateName": "String",
  "renewalThresholdPercentage": 1024,
  "certificateValidityPeriodValue": 1024,
  "certificateValidityPeriodScale": "String"
}
```





