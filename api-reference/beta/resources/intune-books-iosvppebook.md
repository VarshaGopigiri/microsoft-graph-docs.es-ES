---
title: Tipo de recurso iosVppEBook
description: Una clase que contiene las propiedades del libro electrónico de VPP de iOS.
ms.openlocfilehash: 9012584e619277716516582ce1e995446e019b7d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087986"
---
# <a name="iosvppebook-resource-type"></a>Tipo de recurso iosVppEBook

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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
|id|String|Clave de la entidad. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|displayName|String|Nombre del libro electrónico Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|descripción|String|Descripción. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|publicador|String|Publicador. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|publishedDateTime|DateTimeOffset|La fecha y la hora en que se publicó el libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|largeCover|[mimeContent](../resources/intune-shared-mimecontent.md)|Cubierta de libro. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó el archivo del libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|informationUrl|String|La dirección URL para obtener más información. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|privacyInformationUrl|String|La dirección URL de la declaración de privacidad. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
|vppTokenId|Guid|El Id. de token de VPP.|
|appleId|String|El ID de Apple asociado a un token de VPP.|
|vppOrganizationName|String|El nombre de la organización del token de VPP.|
|géneros|Colección string|Géneros.|
|language|String|Idioma.|
|vendedor|String|Vendedor.|
|totalLicenseCount|Int32|Número total de licencias.|
|usedLicenseCount|Int32|Número de licencias usadas.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categories|colección de [managedEBookCategory](../resources/intune-books-managedebookcategory.md)|La lista de categorías para este libro electrónico. Heredado de [managedEBook](../resources/intune-books-managedebook.md)|
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





