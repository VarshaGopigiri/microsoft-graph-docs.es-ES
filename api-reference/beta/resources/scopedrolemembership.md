---
title: tipo de recurso scopedRoleMembership
description: Una pertenencia a una función con ámbito describe la pertenencia de un usuario de un rol de Active directory, que es aún más el ámbito a una unidad administrativa (AU).  Esto proporciona un mecanismo para permitir que un adminsistrator del inquilino de toda la empresa delegar privilegios administrativos a un usuario para administrar usuarios y grupos en un subconjunto de la organización (el subconjunto está definido por un AU).
localization_priority: Normal
ms.openlocfilehash: a83acf82eadd9798a86a1a6456d5b2c4ca60be73
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884801"
---
# <a name="scopedrolemembership-resource-type"></a>tipo de recurso scopedRoleMembership

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una pertenencia a una función con ámbito describe la pertenencia de un usuario de un rol de Active directory, que es aún más el ámbito a una unidad administrativa (AU).  Esto proporciona un mecanismo para permitir que un adminsistrator del inquilino de toda la empresa delegar privilegios administrativos a un usuario para administrar usuarios y grupos en un subconjunto de la organización (el subconjunto está definido por un AU).

## <a name="methods"></a>Métodos
No se admiten las consultas directas a este recurso.  Vea el tema de [unidades administrativas](administrativeunit.md) para ver información acerca de la consulta para las pertenencias a funciones con ámbito, así como agregar y quitar pertenencias de rol con ámbito. 

## <a name="properties"></a>Propiedades
| Propiedad   | Tipo | Description |
|:---------------|:--------|:----------|
|administrativeUnitId|string|Identificador único para la unidad administrativa que el rol de Active directory se limita a|
|id|string| Identificador único para la pertenencia a una función con ámbito. Solo lectura.|
|identificador de función|string| Identificador único para el rol de Active directory que se encuentra en el miembro.|
|roleMemberInfo|[identity](identity.md)| Información de identidad del miembro de función. Representa el usuario que sea miembro de esta función con ámbito.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scopedrolemembership"
}-->

```json
{
  "administrativeUnitId": "string",
  "id": "string (identifier)",
  "roleId": "string",
  "roleMemberInfo": {"@odata.type": "microsoft.graph.identity"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scopedRoleMembership resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
