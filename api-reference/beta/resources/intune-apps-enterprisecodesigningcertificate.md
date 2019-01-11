---
title: tipo de recurso enterpriseCodeSigningCertificate
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 14ed023a831257dc28a9922e1e698a79ec13c951
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842136"
---
# <a name="enterprisecodesigningcertificate-resource-type"></a>tipo de recurso enterpriseCodeSigningCertificate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista enterpriseCodeSigningCertificates](../api/intune-apps-enterprisecodesigningcertificate-list.md)|colección de [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md)|Propiedades de la lista y relaciones de los objetos [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .|
|[Obtener enterpriseCodeSigningCertificate](../api/intune-apps-enterprisecodesigningcertificate-get.md)|[enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md)|Leer las propiedades y las relaciones del objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .|
|[Crear enterpriseCodeSigningCertificate](../api/intune-apps-enterprisecodesigningcertificate-create.md)|[enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md)|Crear un nuevo objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .|
|[Eliminar enterpriseCodeSigningCertificate](../api/intune-apps-enterprisecodesigningcertificate-delete.md)|Ninguno|Elimina un [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md).|
|[Actualizar enterpriseCodeSigningCertificate](../api/intune-apps-enterprisecodesigningcertificate-update.md)|[enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md)|Actualizar las propiedades de un objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave de la entidad.|
|content|Binario|El certificado de firma de código de empresa de Windows, en el formato de datos sin procesar.|
|status|[certificateStatus](../resources/intune-apps-certificatestatus.md)|El estado del certificado aprovisiona o no configurado. Los valores posibles son: `notProvisioned` y `provisioned`.|
|subjectName|cadena|El nombre de sujeto para el certificado.|
|subject|Cadena|El valor de asunto para el certificado.|
|issuerName|Cadena|El nombre para el certificado del emisor.|
|emisor|Cadena|El valor de emisor para el certificado.|
|expirationDateTime|DateTimeOffset|La fecha de caducidad del certificado.|
|uploadDateTime|DateTimeOffset|La fecha de la hora del certificado de firma de código cuando se carga.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.enterpriseCodeSigningCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.enterpriseCodeSigningCertificate",
  "id": "String (identifier)",
  "content": "binary",
  "status": "String",
  "subjectName": "String",
  "subject": "String",
  "issuerName": "String",
  "issuer": "String",
  "expirationDateTime": "String (timestamp)",
  "uploadDateTime": "String (timestamp)"
}
```





