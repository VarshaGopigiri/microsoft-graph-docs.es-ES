---
title: tipo de recurso privilegedRole
description: 'Representa una función de administrador de Azure AD, tales como: **Administrador Global, Administrador de facturación, Administrador de servicio, Administrador de usuarios, Administrador de contraseñas**, etcetera.'
localization_priority: Normal
ms.openlocfilehash: 75763e18731cb969623cc4df6360d50abc018b41
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860861"
---
# <a name="privilegedrole-resource-type"></a>tipo de recurso privilegedRole

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una función de administrador de Azure AD, tales como: **Administrador Global, Administrador de facturación, Administrador de servicio, Administrador de usuarios, Administrador de contraseñas**, etcetera.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Objetos de lista de privilegedRole](../api/privilegedrole-list.md) | colección de [privilegedRole](privilegedrole.md)|Obtener la colección de privilegedRole.|
|[Obtener privilegedRole](../api/privilegedrole-get.md) | [privilegedRole](privilegedrole.md) |Leer las propiedades y las relaciones del objeto privilegedRole.|
|[Asignaciones de listas](../api/privilegedrole-list-assignments.md) |colección de [privilegedRoleAssignment](privilegedroleassignment.md)| Obtener una colección de objetos de asignación para esta función.|
|[selfActivate](../api/privilegedrole-selfactivate.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|Activar el rol asignado.|
|[selfDeactivate](../api/privilegedrole-selfdeactivate.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|Desactivar el rol asignado.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string|El identificador único para el rol de administrador. Es una cadena GUID y tiene el mismo valor que el identificador de plantilla de rol de Azure AD para el rol determinado. Solo lectura.|
|name|string|Nombre de la función.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|asignaciones|colección de [privilegedRoleAssignment](privilegedroleassignment.md)| Las asignaciones de este rol. Solo lectura. Admite valores NULL.|
|settings|[privilegedRoleSettings](privilegedrolesettings.md)| La configuración de este rol. Solo lectura. Admite valores NULL.|
|Resumen|[privilegedRoleSummary](privilegedrolesummary.md)| La información de resumen para este rol. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRole"
}-->

```json
{
  "id": "string (identifier)",
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
