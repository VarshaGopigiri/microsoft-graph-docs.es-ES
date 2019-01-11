---
title: tipo de recurso androidPermissionAction
description: Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: daf72bbc5f8d1e32480adeda72c3f759255f54db
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860539"
---
# <a name="androidpermissionaction-resource-type"></a>tipo de recurso androidPermissionAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|permiso|Cadena|Cadena de permiso Android, definida en la documentación oficial de Android.  Ejemplo 'android.permission.READ_CONTACTS'.|
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





