---
title: Actualizar intuneBrandingProfile
description: Actualizar las propiedades de un objeto intuneBrandingProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0840852d0668cc6e2b4d18b4345792166a2d5193
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964469"
---
# <a name="update-intunebrandingprofile"></a>Actualizar intuneBrandingProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .
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
PATCH /deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md).

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



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}
Content-type: application/json
Content-length: 1209

{
  "profileName": "Profile Name value",
  "profileDescription": "Profile Description value",
  "isDefaultProfile": true,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "contactITName": "Contact ITName value",
  "contactITPhoneNumber": "Contact ITPhone Number value",
  "contactITEmailAddress": "Contact ITEmail Address value",
  "contactITNotes": "Contact ITNotes value",
  "privacyUrl": "https://example.com/privacyUrl/",
  "onlineSupportSiteUrl": "https://example.com/onlineSupportSiteUrl/",
  "onlineSupportSiteName": "Online Support Site Name value",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1,
    "g": 1,
    "b": 1
  },
  "showLogo": true,
  "showDisplayNameNextToLogo": true,
  "themeColorLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1377

{
  "@odata.type": "#microsoft.graph.intuneBrandingProfile",
  "id": "fcd6136c-136c-fcd6-6c13-d6fc6c13d6fc",
  "profileName": "Profile Name value",
  "profileDescription": "Profile Description value",
  "isDefaultProfile": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "contactITName": "Contact ITName value",
  "contactITPhoneNumber": "Contact ITPhone Number value",
  "contactITEmailAddress": "Contact ITEmail Address value",
  "contactITNotes": "Contact ITNotes value",
  "privacyUrl": "https://example.com/privacyUrl/",
  "onlineSupportSiteUrl": "https://example.com/onlineSupportSiteUrl/",
  "onlineSupportSiteName": "Online Support Site Name value",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1,
    "g": 1,
    "b": 1
  },
  "showLogo": true,
  "showDisplayNameNextToLogo": true,
  "themeColorLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```





