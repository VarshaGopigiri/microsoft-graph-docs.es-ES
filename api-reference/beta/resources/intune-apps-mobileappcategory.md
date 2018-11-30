---
title: Tipo de recurso mobileAppCategory
description: Contiene las propiedades de una categoría de aplicación de Intune.
ms.openlocfilehash: 83982563e49696e1542fb89f01e906fb80f85c5a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087953"
---
# <a name="mobileappcategory-resource-type"></a>Tipo de recurso mobileAppCategory

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de una categoría de aplicación de Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileAppCategories](../api/intune-apps-mobileappcategory-list.md)|Colección [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|Enumere las propiedades y las relaciones de los objetos [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).|
|[Obtener mobileAppCategory](../api/intune-apps-mobileappcategory-get.md)|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|Lea las propiedades y las relaciones del objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).|
|[Crear mobileAppCategory](../api/intune-apps-mobileappcategory-create.md)|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|Cree un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).|
|[Eliminar mobileAppCategory](../api/intune-apps-mobileappcategory-delete.md)|Ninguna|Elimina un [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|
|[Actualizar mobileAppCategory](../api/intune-apps-mobileappcategory-update.md)|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|Actualice las propiedades de un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave de la entidad.|
|displayName|String|El nombre de la categoría de aplicación.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de mobileAppCategory.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)"
}
```





