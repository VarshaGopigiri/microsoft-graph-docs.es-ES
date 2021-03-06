---
title: Actualizar iosVppEBook
description: Actualice las propiedades de un objeto iosVppEBook.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c3565a104c1f970293a9d6fc6b9ea5fcdd470228
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982347"
---
# <a name="update-iosvppebook"></a>Actualizar iosVppEBook

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).
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
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|displayName|Cadena|Nombre del libro electrónico Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|descripción|Cadena|Descripción. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|publicador|Cadena|Publicador. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|publishedDateTime|DateTimeOffset|La fecha y la hora en que se publicó el libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|largeCover|[mimeContent](../resources/intune-shared-mimecontent.md)|Cubierta de libro. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó el archivo del libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|vppTokenId|Guid|El Id. de token de VPP.|
|appleId|Cadena|El ID de Apple asociado a un token de VPP.|
|vppOrganizationName|Cadena|El nombre de la organización del token de VPP.|
|géneros|Colección string|Géneros.|
|language|Cadena|Idioma.|
|vendedor|Cadena|Vendedor.|
|totalLicenseCount|Int32|Número total de licencias.|
|usedLicenseCount|Int32|Número de licencias usadas.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}
Content-type: application/json
Content-length: 792

{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 964

{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "id": "3b9f627e-627e-3b9f-7e62-9f3b7e629f3b",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```



