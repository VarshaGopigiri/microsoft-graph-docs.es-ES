---
title: tipo de recurso androidPermissionAction
description: Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.
ms.openlocfilehash: e65f9b28169e231e34b5a7a46316821f77639233
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085175"
---
# <a name="androidpermissionaction-resource-type"></a>tipo de recurso androidPermissionAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|permiso|String|Cadena de permiso Android, definida en la documentación oficial de Android.  Ejemplo 'android.permission.READ_CONTACTS'.|
|action|[androidPermissionActionType](../resources/intune-apps-androidpermissionactiontype.md)|Tipo de acción de permiso Android. Los valores posibles son: `prompt`, `autoGrant` y `autoDeny`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidPermissionAction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidPermissionAction",
  "permission": "String",
  "action": "String"
}
```





