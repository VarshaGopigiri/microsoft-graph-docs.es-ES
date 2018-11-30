---
title: Tipo de recurso mobileApp
description: Una clase abstracta que contiene las propiedades base para las aplicaciones móviles de Intune.
ms.openlocfilehash: 7de5450ade7c95984107026eb8a6b19e07a2ba82
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031749"
---
# <a name="mobileapp-resource-type"></a>Tipo de recurso mobileApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase abstracta que contiene las propiedades base para las aplicaciones móviles de Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileApps](../api/intune-apps-mobileapp-list.md)|Colección [mobileApp](../resources/intune-apps-mobileapp.md)|Enumere las propiedades y las relaciones de los objetos [mobileApp](../resources/intune-apps-mobileapp.md).|
|[Obtener mobileApp](../api/intune-apps-mobileapp-get.md)|[mobileApp](../resources/intune-apps-mobileapp.md)|Lea las propiedades y las relaciones del objeto [mobileApp](../resources/intune-apps-mobileapp.md).|
|[Acción assign](../api/intune-apps-mobileapp-assign.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|displayName|String|El título de la aplicación importado o proporcionado por el administrador.|
|descripción|String|La descripción de la aplicación.|
|publicador|String|El publicador de la aplicación.|
|largeIcon|[mimeContent](../resources/intune-shared-mimecontent.md)|El icono grande, se muestra en los detalles de la aplicación y se usa para cargar el icono.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la aplicación.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación.|
|isFeatured|Booleano|El valor que indica si el administrador ha marcado la aplicación como destacada.|
|privacyInformationUrl|String|La dirección URL de la declaración de privacidad.|
|informationUrl|String|La dirección URL para obtener más información.|
|propietario|String|Propietario de la aplicación.|
|desarrollador|String|El desarrollador de la aplicación.|
|notas|String|Notas de la aplicación.|
|publishingState|[mobileAppPublishingState](../resources/intune-apps-mobileapppublishingstate.md)|Estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Los valores posibles son: `notPublished`, `processing` y `published`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|La lista de categorías para esta aplicación.|
|asignaciones|Colección [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileApp",
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
  "publishingState": "String"
}
```



