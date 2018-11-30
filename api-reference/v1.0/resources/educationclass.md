---
title: Tipo de recurso educationClass
description: 'Representa una clase en un centro educativo. El recurso **educationClass** corresponde al grupo de Office 365 y comparte el mismo identificador. Los alumnos son miembros normales de la clase y los profesores son propietarios y tienen los derechos adecuados. Para que las experiencias de Office funcionen correctamente, los profesores deben ser miembros de las colecciones de profesores y de miembros.  '
ms.openlocfilehash: 4d61ca209b61b8b2b65fbe92b7ba16854e11fb37
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031255"
---
# <a name="educationclass-resource-type"></a>Tipo de recurso educationClass

Representa una clase en un centro educativo. El recurso **educationClass** corresponde al grupo de Office 365 y comparte el mismo identificador. Los alumnos son miembros normales de la clase y los profesores son propietarios y tienen los derechos adecuados. Para que las experiencias de Office funcionen correctamente, los profesores deben ser miembros de las colecciones de profesores y de miembros.  


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener educationClass](../api/educationclass-get.md) | [educationClass](educationclass.md) |Lea las propiedades y relaciones de un objeto **educationClass**.|
|[Agregar miembro](../api/educationclass-post-members.md) |[educationUser](educationuser.md)| Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de miembros.|
|[Enumerar miembros](../api/educationclass-list-members.md) |Colección [educationUser](educationuser.md)| Obtenga una colección de objetos **educationUser**.|
|[Quitar alumnos](../api/educationclass-delete-members.md) |[educationUser](educationuser.md)| Quite un **educationUser** de la clase mediante la propiedad de navegación de miembros.|
|[Enumerar centros educativos](../api/educationclass-list-schools.md) |Colección [educationSchool](educationschool.md)| Obtenga una colección de objetos **educationSchool**.|
|[Agregar profesor](../api/educationclass-post-teachers.md) |[educationUser](educationuser.md)| Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de profesores.|
|[Enumerar profesores](../api/educationclass-list-teachers.md) |Colección [educationUser](educationuser.md)| Obtenga una lista de los profesores de la clase.|
|[Quitar profesor](../api/educationclass-delete-teachers.md) |[educationUser](educationuser.md)| Quite un **educationUser** de la clase mediante la propiedad de navegación de profesores.|
|[Obtener grupo](../api/educationclass-get-group.md) |[group](group.md)| Obtenga el **group** de Office 365 correspondiente a este objeto **educationClass**.|
|[Actualizar](../api/educationclass-update.md) | [educationClass](educationclass.md)    |Actualice un objeto **educationClass**. |
|[Eliminar](../api/educationclass-delete.md) | Ninguno |Elimine un objeto **educationClass**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id| String| Identificador único de la clase|
|description|String| Descripción de la clase|
|displayName|String| Nombre de la clase.|
|mailNickname|String| Nombre de correo para enviar correo electrónico a todos los miembros, si esta opción está habilitada. |
|createdBy|[identitySet](identityset.md)| Entidad que ha creado la clase. |
|classCode|String| Código de clase que usa el centro educativo para identificar la clase.|
|externalId|String| Identificador de la clase en el sistema de sincronización. |
|externalName|String|Nombre de la clase en el sistema de sincronización.|
|externalSource|educationExternalSource| Forma en que se ha creado la clase. Los valores posibles son: `sis`, `manual`, `unknownFutureValue`.|
|term|[educationTerm](educationterm.md)|Período de la clase.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|members|Colección [educationUser](../resources/educationuser.md)| Todos los usuarios de la clase. Admite valores NULL.|
|schools|Colección [educationSchool](../resources/educationschool.md)| Todos los centros educativos a los que está asociada la clase. Admite valores NULL.|
|teachers|Colección [educationUser](../resources/educationuser.md)|  Todos los profesores de la clase. Admite valores NULL.|
|grupo|[group](../resources/group.md)| El grupo de Active directory correspondiente a esta clase.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.educationClass"
}-->

```json
{
  "id": "String",
  "description": "String",
  "classCode": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "displayName": "String",
  "externalId": "String",
  "externalName": "String",
  "externalSource": "string",
  "mailNickname": "String",
  "term": {"@odata.type": "microsoft.graph.educationTerm"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationClass resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
