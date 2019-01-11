---
title: Tipo de recurso iosVppApp
description: Contiene las propiedades y las propiedades heredadas de las aplicaciones del Programa de Compras por Volumen (VPP) de iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8c85fe2220a9bbc9df6933951c779c5d898eadab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888752"
---
# <a name="iosvppapp-resource-type"></a>Tipo de recurso iosVppApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades y las propiedades heredadas de las aplicaciones del Programa de Compras por Volumen (VPP) de iOS.

Hereda de [mobileApp](../resources/intune-apps-mobileapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosVppApps](../api/intune-apps-iosvppapp-list.md)|Colección [iosVppApp](../resources/intune-apps-iosvppapp.md)|Enumere las propiedades y las relaciones de los objetos [iosVppApp](../resources/intune-apps-iosvppapp.md).|
|[Obtener iosVppApp](../api/intune-apps-iosvppapp-get.md)|[iosVppApp](../resources/intune-apps-iosvppapp.md)|Lea las propiedades y las relaciones del objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).|
|[Crear iosVppApp](../api/intune-apps-iosvppapp-create.md)|[iosVppApp](../resources/intune-apps-iosvppapp.md)|Cree un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).|
|[Eliminar iosVppApp](../api/intune-apps-iosvppapp-delete.md)|Ninguna|Elimina un [iosVppApp](../resources/intune-apps-iosvppapp.md).|
|[Actualizar iosVppApp](../api/intune-apps-iosvppapp-update.md)|[iosVppApp](../resources/intune-apps-iosvppapp.md)|Actualice las propiedades de un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).|
|[acción revokeAllLicenses](../api/intune-apps-iosvppapp-revokealllicenses.md)|Ninguno|REVOKE todos los asignados iOS VPP licencias para indicar la aplicación.|
|[acción revokeUserLicense](../api/intune-apps-iosvppapp-revokeuserlicense.md)|Ninguno|Licencia de usuario de REVOKE asignado iOS VPP para dado app.|
|[acción revokeDeviceLicense](../api/intune-apps-iosvppapp-revokedevicelicense.md)|Ninguno|REVOKE asignado iOS VPP dispositivo licencia para dada la aplicación.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|displayName|Cadena|Título de la aplicación importado o proporcionado por el administrador. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|descripción|Cadena|Descripción de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|publicador|Cadena|Publicador de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|largeIcon|[mimeContent](../resources/intune-shared-mimecontent.md)|Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|isFeatured|Booleano|Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|owner|Cadena|Propietario de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|developer|Cadena|Desarrollador de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|notas|Cadena|Notas de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|uploadState|Int32|El estado de carga. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|publishingState|[mobileAppPublishingState](../resources/intune-apps-mobileapppublishingstate.md)|Estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|usedLicenseCount|Int32|Número de licencias VPP en uso.|
|totalLicenseCount|Int32|Número total de licencias VPP.|
|releaseDateTime|DateTimeOffset|Fecha y hora de publicación de la aplicación de VPP.|
|appStoreUrl|Cadena|Dirección URL de la tienda.|
|licensingType|[vppLicensingType](../resources/intune-apps-vpplicensingtype.md)|Tipo de licencia compatible.|
|applicableDeviceType|[iosDeviceType](../resources/intune-apps-iosdevicetype.md)|Tipo de dispositivo iOS aplicable.|
|vppTokenOrganizationName|Cadena|Organización asociada al token del Programa de Compras por Volumen de Apple|
|vppTokenAccountType|[vppTokenAccountType](../resources/intune-shared-vpptokenaccounttype.md)|Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado. Los valores posibles son: `business` y `education`. Los valores posibles son: `business` y `education`.|
|vppTokenAppleId|Cadena|Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.|
|bundleId|Cadena|Nombre de la identidad.|
|vppTokenId|Cadena|Identificador del símbolo (token) VPP asociado con esta aplicación.|
|revokeLicenseActionResults|colección de [iosVppAppRevokeLicensesActionResult](../resources/intune-apps-iosvppapprevokelicensesactionresult.md)|Resultados de revocación acciones de licencia en esta aplicación.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|installSummary|[mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md)|Resumen de instalación de las aplicaciones para móviles. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|deviceStatuses|colección de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|La lista de los Estados de instalación para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|userStatuses|colección de [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|La lista de los Estados de instalación para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|assignedLicenses|colección de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|Las licencias que se ha asignado a esta aplicación.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppApp",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "uploadState": 1024,
  "publishingState": "String",
  "usedLicenseCount": 1024,
  "totalLicenseCount": 1024,
  "releaseDateTime": "String (timestamp)",
  "appStoreUrl": "String",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportUserLicensing": true,
    "supportDeviceLicensing": true,
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "String",
  "vppTokenAccountType": "String",
  "vppTokenAppleId": "String",
  "bundleId": "String",
  "vppTokenId": "String",
  "revokeLicenseActionResults": [
    {
      "@odata.type": "microsoft.graph.iosVppAppRevokeLicensesActionResult",
      "userId": "String",
      "managedDeviceId": "String",
      "totalLicensesCount": 1024,
      "failedLicensesCount": 1024,
      "actionFailureReason": "String",
      "actionName": "String",
      "actionState": "String",
      "startDateTime": "String (timestamp)",
      "lastUpdatedDateTime": "String (timestamp)"
    }
  ]
}
```





