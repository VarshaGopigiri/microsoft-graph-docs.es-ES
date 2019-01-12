---
title: tipo de recurso officeSuiteApp
description: Contiene propiedades y propiedades heredadas para la aplicación del conjunto de aplicaciones de Office365.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f4e59f9e9167d26a626b1de44c89ca8ce6328de1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916176"
---
# <a name="officesuiteapp-resource-type"></a>tipo de recurso officeSuiteApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades y propiedades heredadas para la aplicación del conjunto de aplicaciones de Office365.

Hereda de [mobileApp](../resources/intune-apps-mobileapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista officeSuiteApps](../api/intune-apps-officesuiteapp-list.md)|colección de [officeSuiteApp](../resources/intune-apps-officesuiteapp.md)|Propiedades de la lista y relaciones de los objetos [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) .|
|[Obtener officeSuiteApp](../api/intune-apps-officesuiteapp-get.md)|[officeSuiteApp](../resources/intune-apps-officesuiteapp.md)|Leer las propiedades y las relaciones del objeto [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) .|
|[Crear officeSuiteApp](../api/intune-apps-officesuiteapp-create.md)|[officeSuiteApp](../resources/intune-apps-officesuiteapp.md)|Crear un nuevo objeto [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) .|
|[Eliminar officeSuiteApp](../api/intune-apps-officesuiteapp-delete.md)|Ninguno|Elimina un [officeSuiteApp](../resources/intune-apps-officesuiteapp.md).|
|[Actualizar officeSuiteApp](../api/intune-apps-officesuiteapp-update.md)|[officeSuiteApp](../resources/intune-apps-officesuiteapp.md)|Actualizar las propiedades de un objeto [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) .|

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
|autoAcceptEula|Booleano|El valor que acepte al CLUF automáticamente en el dispositivo de la para el usuario final.|
|Datos|colección de [officeProductId](../resources/intune-apps-officeproductid.md)|Los identificadores de producto que representan la SKU del conjunto de aplicaciones de Office365.|
|excludedApps|[excludedApps](../resources/intune-apps-excludedapps.md)|La propiedad para representar las aplicaciones que se excluirán del producto seleccionado de Office365 Id.|
|useSharedComputerActivation|Booleano|La propiedad para representar si se usa la activación del equipo compartido no para el conjunto de aplicaciones de Office365 app.|
|updateChannel|[officeUpdateChannel](../resources/intune-apps-officeupdatechannel.md)|La propiedad para representar el canal de actualización de Office365. Los valores posibles son: `none`, `current`, `deferred`, `firstReleaseCurrent` y `firstReleaseDeferred`.|
|officePlatformArchitecture|[windowsArchitecture](../resources/intune-apps-windowsarchitecture.md)|La propiedad para representar la versión de conjunto de programas de aplicación de Office365. Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.|
|localesToInstall|Colección String|La propiedad para representar las configuraciones regionales que se instalan cuando se instala las aplicaciones de Office365. Se utiliza 6033 de RFC estándar. Ref:https://technet.microsoft.com/en-us/library/cc179219(v=office.16).aspx|
|installProgressDisplayLevel|[officeSuiteInstallProgressDisplayLevel](../resources/intune-apps-officesuiteinstallprogressdisplaylevel.md)|Para especificar el nivel de presentación para la interfaz de usuario de instalación progreso del programa de instalación en el dispositivo. Los valores posibles son: `none` y `full`.|
|shouldUninstallOlderVersionsOfOffice|Booleano|La propiedad para determinar si debe desinstalar MSI de Office existente si se implementa un conjunto de aplicaciones de la aplicación Office365 en el dispositivo o no.|
|targetVersion|Cadena|La propiedad para representar la versión de destino específico para el conjunto de aplicaciones de la aplicación de Office365 que debe se mantuvo implementado en los dispositivos.|
|updateVersion|Cadena|La propiedad para representar la versión de actualización en la que está disponible para el conjunto de aplicaciones de la aplicación Office365 la versión de destino específica.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|installSummary|[mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md)|Resumen de instalación de las aplicaciones para móviles. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|deviceStatuses|colección de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|La lista de los Estados de instalación para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|userStatuses|colección de [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|La lista de los Estados de instalación para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeSuiteApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeSuiteApp",
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
  "autoAcceptEula": true,
  "productIds": [
    "String"
  ],
  "excludedApps": {
    "@odata.type": "microsoft.graph.excludedApps",
    "access": true,
    "excel": true,
    "groove": true,
    "infoPath": true,
    "lync": true,
    "oneDrive": true,
    "oneNote": true,
    "outlook": true,
    "powerPoint": true,
    "publisher": true,
    "sharePointDesigner": true,
    "visio": true,
    "word": true
  },
  "useSharedComputerActivation": true,
  "updateChannel": "String",
  "officePlatformArchitecture": "String",
  "localesToInstall": [
    "String"
  ],
  "installProgressDisplayLevel": "String",
  "shouldUninstallOlderVersionsOfOffice": true,
  "targetVersion": "String",
  "updateVersion": "String"
}
```





