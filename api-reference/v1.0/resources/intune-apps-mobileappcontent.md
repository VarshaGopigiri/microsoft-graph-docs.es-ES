---
title: Tipo de recurso mobileAppContent
description: Contiene las propiedades del contenido de una versión de aplicación específica. Cada mobileAppContent puede tener varios mobileAppContentFile.
ms.openlocfilehash: 75d00e0b59fe3ca0848c5ad1bcdade76a9430ec1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031484"
---
# <a name="mobileappcontent-resource-type"></a>Tipo de recurso mobileAppContent

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del contenido de una versión de aplicación específica. Cada mobileAppContent puede tener varios mobileAppContentFile.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileAppContents](../api/intune-apps-mobileappcontent-list.md)|Colección [mobileAppContent](../resources/intune-apps-mobileappcontent.md)|Enumere las propiedades y las relaciones de los objetos [mobileAppContent](../resources/intune-apps-mobileappcontent.md).|
|[Obtener mobileAppContent](../api/intune-apps-mobileappcontent-get.md)|[mobileAppContent](../resources/intune-apps-mobileappcontent.md)|Lea las propiedades y las relaciones del objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).|
|[Crear mobileAppContent](../api/intune-apps-mobileappcontent-create.md)|[mobileAppContent](../resources/intune-apps-mobileappcontent.md)|Cree un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).|
|[Eliminar mobileAppContent](../api/intune-apps-mobileappcontent-delete.md)|Ninguna|Elimina un [mobileAppContent](../resources/intune-apps-mobileappcontent.md)|
|[Actualizar mobileAppContent](../api/intune-apps-mobileappcontent-update.md)|[mobileAppContent](../resources/intune-apps-mobileappcontent.md)|Actualice las propiedades de un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La versión de contenido de la aplicación.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|archivos|Colección [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)|La lista de archivos de esta versión de contenido de la aplicación.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppContent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "String (identifier)"
}
```



