# <a name="educationclass-resource-type"></a>Tipo de recurso educationClass

Representa una clase en un centro educativo. El recurso **educationClass** corresponde al grupo de Office 365 y comparte el mismo identificador. Los alumnos son miembros normales de la clase y los profesores son propietarios y tienen los derechos adecuados. Para que las experiencias de Office funcionen correctamente, los profesores deben ser miembros de las colecciones de profesores y de miembros.  


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener educationClass](../api/educationclass_get.md) | [educationClass](educationclass.md) |Lea las propiedades y relaciones de un objeto **educationClass**.|
|[Agregar miembro](../api/educationclass_post_members.md) |[educationUser](educationuser.md)| Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de miembros.|
|[Enumerar miembros](../api/educationclass_list_members.md) |Colección [educationUser](educationuser.md)| Obtenga una colección de objetos **educationUser**.|
|[Quitar alumnos](../api/educationclass_delete_members.md) |[educationUser](educationuser.md)| Quite un **educationUser** de la clase mediante la propiedad de navegación de miembros.|
|[Enumerar centros educativos](../api/educationclass_list_schools.md) |Colección [educationSchool](educationschool.md)| Obtenga una colección de objetos **educationSchool**.|
|[Agregar profesor](../api/educationclass_post_teachers.md) |[educationUser](educationuser.md)| Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de profesores.|
|[Enumerar profesores](../api/educationclass_list_teachers.md) |Colección [educationUser](educationuser.md)| Obtenga una lista de los profesores de la clase.|
|[Quitar profesor](../api/educationclass_delete_teachers.md) |[educationUser](educationuser.md)| Quite un **educationUser** de la clase mediante la propiedad de navegación de profesores.|
|[Obtener grupo](../api/educationclass_get_group.md) |[group](group.md)| Obtenga el **group** de Office 365 correspondiente a este objeto **educationClass**.|
|[Actualizar](../api/educationclass_update.md) | [educationClass](educationclass.md)    |Actualice un objeto **educationClass**. |
|[Eliminar](../api/educationclass_delete.md) | Ninguno |Elimine un objeto **educationClass**. |

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
|externalSource|string| Forma en que se ha creado la clase. Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.|
|term|[educationTerm](educationterm.md)|Período de la clase.|


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|members|Colección [educationUser](../resources/educationuser.md)| Todos los usuarios de la clase. Admite valores NULL.|
|schools|Colección [educationSchool](../resources/educationschool.md)| Todos los centros educativos a los que está asociada la clase. Admite valores NULL.|
|teachers|Colección [educationUser](../resources/educationuser.md)|  Todos los profesores de la clase. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
  "term": {"@odata.type": "microsoft.graph.education.term"}
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
