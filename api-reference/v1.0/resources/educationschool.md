---
title: Tipo de recurso educationSchool
description: 'Un recurso que representa una escuela y que se usa para administrar las clases, los profesores y los alumnos de la escuela representada.  '
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 2549d8babd000a36f0ff3ccd38541ef3c1b2e466
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925822"
---
# <a name="educationschool-resource-type"></a>Tipo de recurso educationSchool

Un recurso que representa una escuela y que se usa para administrar las clases, los profesores y los alumnos de la escuela representada.  


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get](../api/educationschool-get.md) | [educationSchool](educationschool.md) |Lea las propiedades y relaciones de un objeto **educationSchool**.|
|[Agregar clase](../api/educationschool-post-classes.md) |[educationClass](educationclass.md)| Agregue un nuevo **educationClass** en el centro educativo publicando en la propiedad de navegación de clases.|
|[Enumerar clases](../api/educationschool-list-classes.md) |Colección [educationClass](educationclass.md)| Obtenga la colección de objetos **educationClass**.|
|[Quitar clase](../api/educationschool-delete-classes.md) |[educationClass](educationclass.md)| Quite un **educationClass** del centro educativo mediante la propiedad de navegación de clases.|
|[Agregar usuario](../api/educationschool-post-users.md) |[educationUser](educationuser.md)| Agregue un nuevo **educationUser** en el centro educativo publicando en la propiedad de navegación **users**.|
|[Enumerar usuarios](../api/educationschool-list-users.md) |Colección [educationUser](educationuser.md)| Obtenga la colección de objetos **educationUser**.|
|[Quitar usuario](../api/educationschool-delete-users.md) |[educationUser](educationuser.md)| Quite un elemento **educationUser** del centro educativo mediante la propiedad de navegación **users**.|
|[Actualizar](../api/educationschool-update.md) | [educationSchool](educationschool.md) |Actualice un objeto **educationSchool**. |
|[Eliminar](../api/educationschool-delete.md) | Ninguno |Elimine un objeto **educationSchool**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String|GUID de este centro educativo.|
|displayName| String| Nombre para mostrar del centro educativo.| 
|description| String | Descripción del centro educativo.| 
|status| string| Solo lectura. Los valores posibles son: `inactive`, `active`, `expired`, `deleteable`.|
|externalSource| educationExternalSource| Solo lectura.  Los valores posibles son: `sis`, `manual`, `unknownFutureValue`.|
|principalEmail| String| Dirección de correo electrónico del director.|
|principalName| String | Nombre del director.|
|externalPrincipalId| String | Identificador del director en el sistema de sincronización. |
|highestGrade|String| Curso más alto que se imparte. |
|lowestGrade|String| Curso más bajo que se imparte. |
|schoolNumber|String| Número del centro educativo|
|externalId|String| Identificador del centro educativo en el sistema de sincronización. |
|phone|String| Número de teléfono del centro educativo. |
|fax|String| Número de fax del centro educativo. |
|address|[physicalAddress](physicaladdress.md)| Dirección del centro educativo.|
|createdBy|[identitySet](identityset.md)|Entidad que ha creado el centro educativo.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classes|Colección [educationClass](educationclass.md)| Clases impartidas en el centro educativo. Admite valores NULL.|
|users|Colección [educationUser](educationuser.md)| Usuarios del centro educativo. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.educationOrganization",
  "@odata.type": "microsoft.graph.educationSchool"
}-->

```json
{
  "id": "String",
  "displayName": "String",
  "description": "String",
  "status": "String",
  "externalSource": "String",
  "principalEmail": "String",
  "principalName": "String",
  "externalPrincipalId": "String",
  "highestGrade": "String",
  "lowestGrade": "String",
  "schoolNumber": "String",
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "externalId": "String",
  "fax": "String",
  "phone": "String",
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSchool resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
