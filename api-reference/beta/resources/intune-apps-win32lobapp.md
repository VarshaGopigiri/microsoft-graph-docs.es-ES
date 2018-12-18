---
title: tipo de recurso win32LobApp
description: Contiene propiedades y propiedades heredadas para las aplicaciones de Win32.
author: tfitzmac
ms.openlocfilehash: c0941db87aeb5f2414d7e1c06729461de3483bc9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323096"
---
# <a name="win32lobapp-resource-type"></a>tipo de recurso win32LobApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades y propiedades heredadas para las aplicaciones de Win32.

Hereda de [mobileLobApp](../resources/intune-apps-mobilelobapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista win32LobApps](../api/intune-apps-win32lobapp-list.md)|colección de [win32LobApp](../resources/intune-apps-win32lobapp.md)|Propiedades de la lista y relaciones de los objetos [win32LobApp](../resources/intune-apps-win32lobapp.md) .|
|[Obtener win32LobApp](../api/intune-apps-win32lobapp-get.md)|[win32LobApp](../resources/intune-apps-win32lobapp.md)|Leer las propiedades y las relaciones del objeto [win32LobApp](../resources/intune-apps-win32lobapp.md) .|
|[Crear win32LobApp](../api/intune-apps-win32lobapp-create.md)|[win32LobApp](../resources/intune-apps-win32lobapp.md)|Crear un nuevo objeto [win32LobApp](../resources/intune-apps-win32lobapp.md) .|
|[Eliminar win32LobApp](../api/intune-apps-win32lobapp-delete.md)|Ninguno|Elimina un [win32LobApp](../resources/intune-apps-win32lobapp.md).|
|[Actualizar win32LobApp](../api/intune-apps-win32lobapp-update.md)|[win32LobApp](../resources/intune-apps-win32lobapp.md)|Actualizar las propiedades de un objeto [win32LobApp](../resources/intune-apps-win32lobapp.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|displayName|String|Título de la aplicación importado o proporcionado por el administrador. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|descripción|String|Descripción de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|publicador|String|Publicador de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|largeIcon|[mimeContent](../resources/intune-shared-mimecontent.md)|Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|isFeatured|Boolean|Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|privacyInformationUrl|String|La dirección URL de la declaración de privacidad. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|informationUrl|String|La dirección URL para obtener más información. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|owner|String|Propietario de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|developer|String|Desarrollador de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|notas|String|Notas de la aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|uploadState|Int32|El estado de carga. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|publishingState|[mobileAppPublishingState](../resources/intune-apps-mobileapppublishingstate.md)|Estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|committedContentVersion|String|Versión interna del contenido confirmado. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).|
|fileName|String|Nombre del archivo de la aplicación de LOB principal. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).|
|size|Int64|Tamaño total, incluidos todos los archivos cargados. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).|
|installCommandLine|String|La línea de comandos para instalar esta aplicación|
|uninstallCommandLine|String|La línea de comandos para desinstalar esta aplicación|
|applicableArchitectures|[windowsArchitecture](../resources/intune-apps-windowsarchitecture.md)|Arquitecturas de Windows en las que se puede ejecutar esta aplicación. Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.|
|minimumSupportedOperatingSystem|[windowsMinimumOperatingSystem](../resources/intune-apps-windowsminimumoperatingsystem.md)|Valor del sistema operativo mínimo aplicable.|
|minimumFreeDiskSpaceInMB|Int32|El valor para el espacio libre en disco mínimo que se requiere para instalar esta aplicación.|
|minimumMemoryInMB|Int32|El valor de la memoria física mínimo que se requiere para instalar esta aplicación.|
|minimumNumberOfProcessors|Int32|El valor para el número mínimo de procesadores que se requiere para instalar esta aplicación.|
|minimumCpuSpeedInMHz|Int32|El valor de la velocidad de CPU mínimo que se requiere para instalar esta aplicación.|
|detectionRules|colección de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)|Las reglas de detección para detectar la aplicación de línea de negocio (LoB) de Win32.|
|installExperience|[win32LobAppInstallExperience](../resources/intune-apps-win32lobappinstallexperience.md)|La experiencia de instalación para esta aplicación.|
|returnCodes|colección de [win32LobAppReturnCode](../resources/intune-apps-win32lobappreturncode.md)|Los códigos de retorno para registrar el comportamiento de la instalación.|
|msiInformation|[win32LobAppMsiInformation](../resources/intune-apps-win32lobappmsiinformation.md)|Los detalles MSI si esta aplicación Win32 es una aplicación MSI.|
|setupFilePath|String|La ruta de acceso relativa del archivo del programa de instalación en el paquete de Win32LobApp cifrado.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|installSummary|[mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md)|Resumen de instalación de las aplicaciones para móviles. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|deviceStatuses|colección de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|La lista de los Estados de instalación para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).|
|userStatuses|colección de [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|La lista de los Estados de instalación para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|contentVersions|Colección [mobileAppContent](../resources/intune-apps-mobileappcontent.md)|La lista de versiones de contenido de esta aplicación. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.win32LobApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobApp",
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
  "committedContentVersion": "String",
  "fileName": "String",
  "size": 1024,
  "installCommandLine": "String",
  "uninstallCommandLine": "String",
  "applicableArchitectures": "String",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "minimumFreeDiskSpaceInMB": 1024,
  "minimumMemoryInMB": 1024,
  "minimumNumberOfProcessors": 1024,
  "minimumCpuSpeedInMHz": 1024,
  "detectionRules": [
    {
      "@odata.type": "microsoft.graph.win32LobAppRegistryDetection",
      "check32BitOn64System": true,
      "keyPath": "String",
      "valueName": "String",
      "detectionType": "String",
      "operator": "String",
      "detectionValue": "String"
    }
  ],
  "installExperience": {
    "@odata.type": "microsoft.graph.win32LobAppInstallExperience",
    "runAsAccount": "String"
  },
  "returnCodes": [
    {
      "@odata.type": "microsoft.graph.win32LobAppReturnCode",
      "returnCode": 1024,
      "type": "String"
    }
  ],
  "msiInformation": {
    "@odata.type": "microsoft.graph.win32LobAppMsiInformation",
    "productCode": "String",
    "productVersion": "String",
    "upgradeCode": "String",
    "requiresReboot": true,
    "packageType": "String"
  },
  "setupFilePath": "String"
}
```





