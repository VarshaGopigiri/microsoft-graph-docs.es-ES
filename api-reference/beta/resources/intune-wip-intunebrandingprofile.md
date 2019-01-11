---
title: tipo de recurso intuneBrandingProfile
description: Esta entidad contiene datos que se usan para personalizar la apariencia de nivel de inquilino de las aplicaciones de Portal de empresa, así como el portal web del usuario final.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d2ee2fee902b4aca542810dc058b7d16aaedb9c6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820611"
---
# <a name="intunebrandingprofile-resource-type"></a>tipo de recurso intuneBrandingProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta entidad contiene datos que se usan para personalizar la apariencia de nivel de inquilino de las aplicaciones de Portal de empresa, así como el portal web del usuario final.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista intuneBrandingProfiles](../api/intune-wip-intunebrandingprofile-list.md)|colección de [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)|Propiedades de la lista y relaciones de los objetos [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .|
|[Obtener intuneBrandingProfile](../api/intune-wip-intunebrandingprofile-get.md)|[intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)|Leer las propiedades y las relaciones del objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .|
|[Crear intuneBrandingProfile](../api/intune-wip-intunebrandingprofile-create.md)|[intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)|Crear un nuevo objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .|
|[Eliminar intuneBrandingProfile](../api/intune-wip-intunebrandingprofile-delete.md)|Ninguno|Elimina un [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md).|
|[Actualizar intuneBrandingProfile](../api/intune-wip-intunebrandingprofile-update.md)|[intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)|Actualizar las propiedades de un objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de perfil|
|nombre del perfil|Cadena|Nombre del perfil|
|profileDescription|Cadena|Descripción del perfil|
|isDefaultProfile|Booleano|Presenta si se utiliza el perfil de forma predeterminada.|
|createdDateTime|DateTimeOffset|Cuando se creó el BrandingProfile.|
|lastModifiedDateTime|DateTimeOffset|Cuando el BrandingProfile se modificó por última vez.|
|displayName|Cadena|Nombre de la compañía u organización que se muestra a los usuarios finales.|
|contactITName|Cadena|Nombre de la persona u organización responsable del soporte técnico de TI.|
|contactITPhoneNumber|Cadena|Número de teléfono de la persona u organización responsable del soporte técnico de TI.|
|contactITEmailAddress|Cadena|Dirección de correo electrónico de la persona u organización responsable del soporte técnico de TI.|
|contactITNotes|Cadena|Comentarios de texto con respecto a la persona u organización responsable del soporte técnico de TI.|
|privacyUrl|Cadena|Dirección URL de la directiva de privacidad de la empresa u organización.|
|onlineSupportSiteUrl|Cadena|Dirección URL del sitio del departamento de soporte técnico de la empresa u organización.|
|onlineSupportSiteName|Cadena|Nombre para mostrar del sitio del departamento de soporte técnico de la empresa u organización.|
|themeColor|[rgbColor](../resources/intune-shared-rgbcolor.md)|Color de tema principal utilizado en el portal web y las aplicaciones del Portal de empresa.|
|showLogo|Booleano|Booleano que indica si se muestran o no las imágenes de logotipo proporcionadas por el administrador.|
|showDisplayNameNextToLogo|Booleano|Booleano que indica si se muestra o no el nombre para mostrar proporcionado por el administrador.|
|themeColorLogo|[mimeContent](../resources/intune-shared-mimecontent.md)|Imagen de logotipo que se muestra en las aplicaciones de Portal de empresa de fondos de color del tema.|
|lightBackgroundLogo|[mimeContent](../resources/intune-shared-mimecontent.md)|Imagen de logotipo que se muestra en las aplicaciones de Portal de empresa de fondos claras.|
|landingPageCustomizedImage|[mimeContent](../resources/intune-shared-mimecontent.md)|Imagen personalizada que se muestra en la página de inicio de aplicaciones de Portal de empresa|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.intuneBrandingProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.intuneBrandingProfile",
  "id": "String (identifier)",
  "profileName": "String",
  "profileDescription": "String",
  "isDefaultProfile": true,
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "contactITName": "String",
  "contactITPhoneNumber": "String",
  "contactITEmailAddress": "String",
  "contactITNotes": "String",
  "privacyUrl": "String",
  "onlineSupportSiteUrl": "String",
  "onlineSupportSiteName": "String",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1024,
    "g": 1024,
    "b": 1024
  },
  "showLogo": true,
  "showDisplayNameNextToLogo": true,
  "themeColorLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  }
}
```





