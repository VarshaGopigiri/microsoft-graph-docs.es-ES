---
title: Tipo de recurso androidForWorkEnrollmentProfile
description: Perfil de inscripción usado al inscribir dispositivos COSU mediante la administración en la nube de Google.
localization_priority: Normal
ms.openlocfilehash: a10e3a153cc21837ab015ab0c08e8c8b6ee0ac9b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890975"
---
# <a name="androidforworkenrollmentprofile-resource-type"></a>Tipo de recurso androidForWorkEnrollmentProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Perfil de inscripción usado al inscribir dispositivos COSU mediante la administración en la nube de Google.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidForWorkEnrollmentProfiles](../api/intune-androidforwork-androidforworkenrollmentprofile-list.md)|Colección [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|Enumere las propiedades y las relaciones de los objetos [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).|
|[Obtener androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-get.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|Lea las propiedades y las relaciones del objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).|
|[Crear androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-create.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|Cree un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).|
|[Eliminar androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-delete.md)|Ninguna|Elimina un [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).|
|[Actualizar androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-update.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|Actualice las propiedades de un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).|
|[Acción revokeToken](../api/intune-androidforwork-androidforworkenrollmentprofile-revoketoken.md)|Ninguna|Todavía no documentado|
|[Acción createToken](../api/intune-androidforwork-androidforworkenrollmentprofile-createtoken.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|accountId|Cadena|GUID del espacio empresarial al que pertenece el perfil de inscripción.|
|id|Cadena|GUID único del perfil de inscripción.|
|displayName|Cadena|Nombre para mostrar del perfil de inscripción.|
|descripción|Cadena|Descripción del perfil de inscripción.|
|createdDateTime|DateTimeOffset|Fecha y hora en que se creó el perfil de inscripción.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en que se modificó el perfil de inscripción por última vez.|
|tokenValue|Cadena|Valor del token creado más recientemente para este perfil de inscripción.|
|tokenExpirationDateTime|DateTimeOffset|Fecha y hora en que expirará el token creado más recientemente.|
|enrolledDeviceCount|Int32|Número total de dispositivos Android que se han inscrito con este perfil de inscripción.|
|qrCodeContent|Cadena|Cadena usada para generar un código QR para el token.|
|qrCodeImage|[mimeContent](../resources/intune-shared-mimecontent.md)|Cadena usada para generar un código QR para el token.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
  "accountId": "String",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "tokenValue": "String",
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





