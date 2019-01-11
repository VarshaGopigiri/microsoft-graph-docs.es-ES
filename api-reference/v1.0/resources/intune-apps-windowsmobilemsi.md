---
title: Tipo de recurso windowsMobileMSI
description: Contiene las propiedades y las propiedades heredadas de la aplicación del conjunto de aplicaciones de línea de negocio de MSI para Windows Mobile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 123b449e2dd94582bbd2c485a121a81f91f58e94
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888343"
---
# <a name="windowsmobilemsi-resource-type"></a>Tipo de recurso windowsMobileMSI

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades y las propiedades heredadas de la aplicación del conjunto de aplicaciones de línea de negocio de MSI para Windows Mobile.

Hereda de [mobileLobApp](../resources/intune-apps-mobilelobapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsMobileMSIs](../api/intune-apps-windowsmobilemsi-list.md)|Colección [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md)|Enumere las propiedades y las relaciones de los objetos [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).|
|[Obtener windowsMobileMSI](../api/intune-apps-windowsmobilemsi-get.md)|[windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md)|Lea las propiedades y las relaciones del objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).|
|[Crear windowsMobileMSI](../api/intune-apps-windowsmobilemsi-create.md)|[windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md)|Cree un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).|
|[Eliminar windowsMobileMSI](../api/intune-apps-windowsmobilemsi-delete.md)|Ninguna|Elimina un [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).|
|[Actualizar windowsMobileMSI](../api/intune-apps-windowsmobilemsi-update.md)|[windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md)|Actualice las propiedades de un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).|

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
|publishingState|[mobileAppPublishingState](../resources/intune-apps-mobileapppublishingstate.md)|Estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|committedContentVersion|Cadena|Versión interna del contenido confirmado. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).|
|fileName|Cadena|Nombre del archivo de la aplicación de LOB principal. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).|
|size|Int64|Tamaño total, incluidos todos los archivos cargados. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).|
|commandLine|Cadena|Línea de comandos.|
|productCode|Cadena|Código del producto.|
|productVersion|Cadena|Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.|
|ignoreVersionDetection|Booleano|Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo. Se establece en true para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md)|
|contentVersions|Colección [mobileAppContent](../resources/intune-apps-mobileappcontent.md)|La lista de versiones de contenido de esta aplicación. Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsMobileMSI"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
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
  "publishingState": "String",
  "committedContentVersion": "String",
  "fileName": "String",
  "size": 1024,
  "commandLine": "String",
  "productCode": "String",
  "productVersion": "String",
  "ignoreVersionDetection": true
}
```



