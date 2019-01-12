---
title: tipo de recurso administrativeUnit
description: Una unidad administrativa proporciona un contenedor conceptual para los objetos de Active directory de usuario y de grupo. Uso de unidades administrativas, un administrador de la compañía ahora puede delegar responsabilidades administrativas para administrar los usuarios y grupos con ámbito a una unidad administrativa a un administrador regional o departamental o contenidos dentro de.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: a4fb81c9a9d605dd155facefb263ff4a310442c3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955320"
---
# <a name="administrativeunit-resource-type"></a>tipo de recurso administrativeUnit

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una unidad administrativa proporciona un contenedor conceptual para los objetos de Active directory de usuario y de grupo. Uso de unidades administrativas, un administrador de la compañía ahora puede delegar responsabilidades administrativas para administrar los usuarios y grupos con ámbito a una unidad administrativa a un administrador regional o departamental o contenidos dentro de.

Veamos un ejemplo. Imagine que Contoso Corp está formado por dos divisiones - una división costa oeste y una división costa este. El ámbito de los roles de Active Directory de Contoso están el inquilino todo. Lee, un administrador de la compañía Contoso, desea delegar responsabilidades administrativas, pero el ámbito de la división de costa oeste o la división de la costa este.  Lee puede crear una *unidad de comprenderán costa oeste* y colocar todos los usuarios de costa oeste en esta unidad administrativa.  De forma similar, Lee puede crear una *unidad de costa este administrativas*.  Ahora puede iniciar Lee, delegar responsabilidades administrativas a otras personas, pero en el **ámbito de** las unidades administrativas nueva que ha creado. Lee coloca a Jennifer en un *Administrador de departamento de soporte técnico* función en el **ámbito** para la *unidad administrativa costa oeste*.  Esto permite Jennifer restablecer la contraseña de cualquier usuario, pero sólo si los usuarios se encuentran en la *unidad administrativa costa oeste*.  De forma similar, Lee coloca a Dave en un *Administrador de la cuenta de usuario* función en el **ámbito** para la *unidad administrativa costa este*.  Esto permite Dave actualizar a los usuarios, asignar licencias y restablecer la contraseña de cualquier usuario, pero sólo si los usuarios están en la *unidad administrativa costa este*. Para un vídeo de introducción, vea [Introducción a las unidades administrativas de Azure Active Directory](https://channel9.msdn.com/Series/Windows-Azure-Active-Directory/Introduction-to-Azure-Active-Directory-Administrative-Units).

Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](/graph/extensibility-overview).

En este tema se ofrece descripciones de las propiedades declaradas y las propiedades de navegación expuestas por la entidad administrativeUnit, así como las operaciones y las funciones que se pueden llamar en el recurso administrativeUnits.


## <a name="methods"></a>Métodos

| Método   | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Crear administrativeUnit](../api/administrativeunit-post-administrativeunits.md) | [administrativeUnit](administrativeunit.md) | Crear una nueva unidad administrativa.|
|[Lista administrativeUnits](../api/administrativeunit-list.md) | colección de [administrativeUnit](administrativeunit.md) |Propiedades de la lista de todos los administrativeUnits.|
|[Obtener administrativeUnit](../api/administrativeunit-get.md) | [administrativeUnit](administrativeunit.md) |Leer las propiedades y relaciones de un objeto administrativeUnit específica.|
|[Actualizar adminstrativeUnit](../api/administrativeunit-update.md) | [administrativeUnit](administrativeunit.md)  |Actualizar el objeto administrativeUnit. |
|[Eliminar adminstrativeUnit](../api/administrativeunit-delete.md) | Ninguno |Eliminar el objeto administrativeUnit. |
|[Agregar un miembro](../api/administrativeunit-post-members.md) |[directoryObject](directoryobject.md)| Adición de un miembro (usuario o grupo).|
|[Enumerar miembros](../api/administrativeunit-list-members.md) |Colección [directoryObject](directoryobject.md)| Obtener la lista de miembros (de usuario y de grupo).|
|[Obtener un miembro](../api/administrativeunit-get-members.md) |[directoryObject](directoryobject.md)| Obtenga a un miembro específico.|
|[Quitar un miembro](../api/administrativeunit-delete-members.md) |[directoryObject](directoryobject.md)| Quitar a un miembro.|
|[Agregar a miembro de la función con ámbito](../api/administrativeunit-post-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| Adición de un miembro de función con ámbito.|
|[Miembros de la función con ámbito de lista](../api/administrativeunit-list-scopedrolemembers.md) |colección de [scopedRoleMembership](scopedrolemembership.md)| Obtener la lista de administradores de la función con ámbito.|
|[Obtener a un miembro de la función con ámbito](../api/administrativeunit-get-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| Obtenga a un miembro de función con ámbito específico.|
|[Quitar a un miembro de la función con ámbito](../api/administrativeunit-delete-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| Quitar a un miembro de la función con ámbito.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|string|Una descripción opcional para la unidad administrativa.|
|displayName|string|Nombre para mostrar para la unidad administrativa.|
|id|string|Identificador único para la unidad administrativa. Solo lectura.|
|visibility|string|Controla si la unidad administrativa y sus miembros están ocultos o público. Se puede establecer en HiddenMembership o público. Si no se establece, comportamiento predeterminado es público. Cuando se establece en HiddenMembership, sólo los miembros de la unidad administrativa pueden enumerar a otros miembros de la unidad administrativa.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensions|Colección de [extensiones](extension.md)|La colección de extensiones de open definidas para esta unidad administrativa. Admite valores NULL.|
|members|Colección [directoryObject](directoryobject.md)|Los usuarios y grupos que son miembros de esta unidad Adminsitrative. Métodos HTTP: Obtener (miembros de la lista), entrada (agregar miembros), eliminar (quitar miembros).|
|scopedRoleMembers|colección de [scopedRoleMembership](scopedrolemembership.md)| Miembros de la función con ámbito de esta unidad administrativa.  Métodos HTTP: Obtener (lista scopedRoleMemberships), entrada (agregar scopedRoleMembership), eliminar (quitar scopedRoleMembership). |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.administrativeUnit"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "visibility": "string"
}

```


## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "administrativeUnit resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
