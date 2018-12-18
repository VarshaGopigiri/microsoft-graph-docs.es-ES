---
title: tipo de recurso roleScopeTag
description: Etiqueta de ámbito de rol
author: tfitzmac
ms.openlocfilehash: 49059ceddcd043f39f51c563c85ba8986b6fc61b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354771"
---
# <a name="rolescopetag-resource-type"></a>tipo de recurso roleScopeTag

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Etiqueta de ámbito de rol
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista roleScopeTags](../api/intune-rbac-rolescopetag-list.md)|colección de [roleScopeTag](../resources/intune-rbac-rolescopetag.md)|Propiedades de la lista y relaciones de los objetos [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .|
|[Obtener roleScopeTag](../api/intune-rbac-rolescopetag-get.md)|[roleScopeTag](../resources/intune-rbac-rolescopetag.md)|Leer las propiedades y las relaciones del objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .|
|[Crear roleScopeTag](../api/intune-rbac-rolescopetag-create.md)|[roleScopeTag](../resources/intune-rbac-rolescopetag.md)|Crear un nuevo objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .|
|[Eliminar roleScopeTag](../api/intune-rbac-rolescopetag-delete.md)|Ninguno|Elimina un [roleScopeTag](../resources/intune-rbac-rolescopetag.md).|
|[Actualizar roleScopeTag](../api/intune-rbac-rolescopetag-update.md)|[roleScopeTag](../resources/intune-rbac-rolescopetag.md)|Actualizar las propiedades de un objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Es de solo lectura y generada automáticamente.|
|displayName|String|El para mostrar o el nombre descriptivo de la etiqueta de ámbito de función.|
|descripción|String|Descripción de la etiqueta de ámbito de función.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.roleScopeTag"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.roleScopeTag",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```





