---
title: Tipo de recurso educationSchool
description: 'Centro educativo. El recurso **educationSchool** actualmente corresponde a un recurso administrativeUnit y comparte el mismo identificador.  '
ms.openlocfilehash: 6a478428874c7c600f60a6924dc06be5f4e3ba11
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088562"
---
# <a name="educationschool-resource-type"></a>Tipo de recurso educationSchool

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Centro educativo. El recurso **educationSchool** actualmente corresponde a un recurso [administrativeUnit](administrativeunit.md) y comparte el mismo identificador.  

Este recurso es un subtipo de [educationOrganization](educationorganization.md).




## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get](../api/educationschool-get.md) | [educationSchool](educationschool.md) |Lea las propiedades y relaciones de un objeto **educationSchool**.|
|[Agregar clase](../api/educationschool-post-classes.md) |[educationClass](educationclass.md)| Agregue un nuevo **educationClass** en el centro educativo publicando en la propiedad de navegación de clases.|
|[Enumerar clases](../api/educationschool-list-classes.md) |Colección [educationClass](educationclass.md)| Obtenga la colección de objetos **educationClass**.|
|[Quitar clase](../api/educationschool-delete-classes.md) |[educationClass](educationclass.md)| Quite un **educationClass** del centro educativo mediante la propiedad de navegación de clases.|
|[Agregar usuario](../api/educationschool-post-users.md) |[educationUser](educationuser.md)| Agregue un nuevo **educationUser** en el centro educativo publicando en la propiedad de navegación **users**.|
|[Enumerar usuarios](../api/educationschool-list-users.md) |Colección [educationUser](educationuser.md)| Obtenga la colección de objetos **educationUser**.|
|[Quitar usuario](../api/educationschool-delete-users.md) |[educationUser](educationuser.md)| Quite un **educationUser** del centro educativo mediante la propiedad de navegación **users**.|
|[Obtener administrativeUnit](../api/educationschool-get-administrativeunit.md) |[administrativeUnit](administrativeunit.md)| Obtenga el directorio simple **administrativeUnit** correspondiente a este objeto **educationSchool**.|
|[Actualizar](../api/educationschool-update.md) | [educationSchool](educationschool.md) |Actualice un objeto **educationSchool**. |
|[Eliminar](../api/educationschool-delete.md) | Ninguno |Elimine un objeto **educationSchool**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String|GUID de este centro educativo.|
|displayName| String| Nombre para mostrar del centro educativo.| 
|description| String | Descripción del centro educativo.| 
|status| string| Solo lectura. Los valores posibles son: `inactive`, `active`, `expired` y `deleteable`.|
|externalSource| string| Solo lectura.  Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.|
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

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
