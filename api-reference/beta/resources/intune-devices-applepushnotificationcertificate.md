---
title: Tipo de recurso applePushNotificationCertificate
description: Certificado de notificación de inserción de Apple.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3cc0b4a3e35027f79dd79ab065de9632e9585873
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810867"
---
# <a name="applepushnotificationcertificate-resource-type"></a>Tipo de recurso applePushNotificationCertificate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Certificado de notificación de inserción de Apple.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener applePushNotificationCertificate](../api/intune-devices-applepushnotificationcertificate-get.md)|[applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md)|Lea las propiedades y las relaciones del objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).|
|[Actualizar applePushNotificationCertificate](../api/intune-devices-applepushnotificationcertificate-update.md)|[applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md)|Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).|
|[Función downloadApplePushNotificationCertificateSigningRequest](../api/intune-devices-applepushnotificationcertificate-downloadapplepushnotificationcertificatesigningrequest.md)|cadena|Descargar solicitud de firma de certificado de notificación de inserción de Apple|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del certificado|
|appleIdentifier|String|Id. de Apple de la cuenta que se usó para crear el certificado push MDM.|
|topicIdentifier|String|Id. del tema|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación del certificado de notificación push de Apple.|
|expirationDateTime|DateTimeOffset|Fecha y hora de la expiración del certificado de notificación push de Apple.|
|certificateUploadStatus|Cadena|El estado de carga del certificado.|
|certificateUploadFailureReason|Cadena|No se pudo la razón por la carga de certificado.|
|certificado|String|Todavía no documentado|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.applePushNotificationCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.applePushNotificationCertificate",
  "id": "String (identifier)",
  "appleIdentifier": "String",
  "topicIdentifier": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "certificateUploadStatus": "String",
  "certificateUploadFailureReason": "String",
  "certificate": "String"
}
```





