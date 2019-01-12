---
title: Tipo de recurso iosVppEBook
description: Una clase que contiene las propiedades del libro electrónico de VPP de iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4a0db53609932fc5b602ca03757e38c218dee4f2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952478"
---
# <a name="iosvppebook-resource-type"></a>Tipo de recurso iosVppEBook

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades del libro electrónico de VPP de iOS.

Hereda de [managedEBook](../resources/intune-books-managedebook.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosVppEBooks](../api/intune-books-iosvppebook-list.md)|Colección [iosVppEBook](../resources/intune-books-iosvppebook.md)|Enumere las propiedades y las relaciones de los objetos [iosVppEBook](../resources/intune-books-iosvppebook.md).|
|[Obtener iosVppEBook](../api/intune-books-iosvppebook-get.md)|[iosVppEBook](../resources/intune-books-iosvppebook.md)|Lea las propiedades y las relaciones del objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).|
|[Crear iosVppEBook](../api/intune-books-iosvppebook-create.md)|[iosVppEBook](../resources/intune-books-iosvppebook.md)|Cree un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).|
|[Eliminar iosVppEBook](../api/intune-books-iosvppebook-delete.md)|Ninguna|Elimina un [iosVppEBook](../resources/intune-books-iosvppebook.md).|
|[Actualizar iosVppEBook](../api/intune-books-iosvppebook-update.md)|[iosVppEBook](../resources/intune-books-iosvppebook.md)|Actualice las propiedades de un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).|

## <a name="properties"></a>Propiedades
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

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|La lista de asignaciones para este libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|installSummary|[eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md)|Resumen de instalación de las aplicaciones para móviles. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|deviceStates|Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)|La lista de estados de asignaciones para este libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|userStateSummary|Colección [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)|La lista de estados de asignaciones para este libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppEBook"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "publishedDateTime": "String (timestamp)",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "informationUrl": "String",
  "privacyInformationUrl": "String",
  "vppTokenId": "Guid",
  "appleId": "String",
  "vppOrganizationName": "String",
  "genres": [
    "String"
  ],
  "language": "String",
  "seller": "String",
  "totalLicenseCount": 1024,
  "usedLicenseCount": 1024
}
```



