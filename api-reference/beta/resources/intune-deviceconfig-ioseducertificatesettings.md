---
title: tipo de recurso iosEduCertificateSettings
description: Confianza certificados raíz y PFX para iOS EDU.
author: tfitzmac
ms.openlocfilehash: 8e373a7c878dd06870b13a32c428f837d741964c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332329"
---
# <a name="ioseducertificatesettings-resource-type"></a>tipo de recurso iosEduCertificateSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Confianza certificados raíz y PFX para iOS EDU.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|trustedRootCertificate|Binario|Certificado raíz de confianza.|
|certFileName|String|Nombre de archivo para mostrar en la interfaz de usuario.|
|certificationAuthority|String|Entidad de certificación PKCS.|
|certificationAuthorityName|String|Nombre de la autoridad de certificación PKCS.|
|certificateTemplateName|String|Nombre de la plantilla de certificado PKCS.|
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





