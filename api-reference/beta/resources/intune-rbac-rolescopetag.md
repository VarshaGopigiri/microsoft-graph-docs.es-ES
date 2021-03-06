---
title: tipo de recurso roleScopeTag
description: Etiqueta de ámbito de rol
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 609d4202069f6e4258c9824a65b72ab769c365b2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981857"
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
|id|Cadena|Clave de la entidad. Es de solo lectura y generada automáticamente.|
|displayName|Cadena|El para mostrar o el nombre descriptivo de la etiqueta de ámbito de función.|
|descripción|Cadena|Descripción de la etiqueta de ámbito de función.|

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





