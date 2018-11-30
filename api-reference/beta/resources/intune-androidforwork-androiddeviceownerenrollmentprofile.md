---
title: tipo de recurso androidDeviceOwnerEnrollmentProfile
description: Perfil de inscripción usado al inscribir dispositivos COSU mediante la administración en la nube de Google.
ms.openlocfilehash: 0ca468a624f5b1793b09eb6b4d9d9e003cae3ac7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084204"
---
# <a name="androiddeviceownerenrollmentprofile-resource-type"></a>tipo de recurso androidDeviceOwnerEnrollmentProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Perfil de inscripción usado al inscribir dispositivos COSU mediante la administración en la nube de Google.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista androidDeviceOwnerEnrollmentProfiles](../api/intune-androidforwork-androiddeviceownerenrollmentprofile-list.md)|colección de [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md)|Propiedades de la lista y relaciones de los objetos [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) .|
|[Obtener androidDeviceOwnerEnrollmentProfile](../api/intune-androidforwork-androiddeviceownerenrollmentprofile-get.md)|[androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md)|Leer las propiedades y las relaciones del objeto [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) .|
|[Crear androidDeviceOwnerEnrollmentProfile](../api/intune-androidforwork-androiddeviceownerenrollmentprofile-create.md)|[androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md)|Crear un nuevo objeto [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) .|
|[Eliminar androidDeviceOwnerEnrollmentProfile](../api/intune-androidforwork-androiddeviceownerenrollmentprofile-delete.md)|Ninguno|Elimina un [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md).|
|[Actualizar androidDeviceOwnerEnrollmentProfile](../api/intune-androidforwork-androiddeviceownerenrollmentprofile-update.md)|[androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md)|Actualizar las propiedades de un objeto [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) .|
|[Acción revokeToken](../api/intune-androidforwork-androiddeviceownerenrollmentprofile-revoketoken.md)|Ninguna|Todavía no documentado|
|[Acción createToken](../api/intune-androidforwork-androiddeviceownerenrollmentprofile-createtoken.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|accountId|String|GUID del espacio empresarial al que pertenece el perfil de inscripción.|
|id|String|GUID único del perfil de inscripción.|
|displayName|String|Nombre para mostrar del perfil de inscripción.|
|descripción|String|Descripción del perfil de inscripción.|
|createdDateTime|DateTimeOffset|Fecha y hora en que se creó el perfil de inscripción.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en que se modificó el perfil de inscripción por última vez.|
|tokenValue|String|Valor del token creado más recientemente para este perfil de inscripción.|
|tokenCreationDateTime|DateTimeOffset|Fecha hora en que se creó el token creado más recientemente.|
|tokenExpirationDateTime|DateTimeOffset|Fecha y hora en que expirará el token creado más recientemente.|
|enrolledDeviceCount|Int32|Número total de dispositivos Android que se han inscrito con este perfil de inscripción.|
|qrCodeContent|String|Cadena usada para generar un código QR para el token.|
|qrCodeImage|[mimeContent](../resources/intune-shared-mimecontent.md)|Cadena usada para generar un código QR para el token.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidDeviceOwnerEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerEnrollmentProfile",
  "accountId": "String",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "tokenValue": "String",
  "tokenCreationDateTime": "String (timestamp)",
  "tokenExpirationDateTime": "String (timestamp)",
  "enrolledDeviceCount": 1024,
  "qrCodeContent": "String",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  }
}
```





