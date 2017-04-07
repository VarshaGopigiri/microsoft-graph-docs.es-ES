# <a name="directoryrole-resource-type"></a>Tipo de recurso directoryRole

Representa un rol de directorio de Azure AD. Los roles de directorio de Azure AD también se conocen como *roles de administrador*. Para obtener más información sobre los roles de directorio (administrador), consulte [Asignación de roles de administrador en Azure Active Directory](http://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/). Con Microsoft Graph, puede asignar usuarios a roles de directorio para concederles los permisos del rol de destino. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activa de manera predeterminada el rol de directorio Administradores de la compañía. Para activar otros roles de directorio disponibles, envíe una solicitud POST con el identificador de la [directoryRoleTemplate](directoryroletemplate.md) en la que se basa el rol de directorio. Hereda de [directoryObject](directoryobject.md).



## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener directoryRole](../api/directoryrole_get.md) | [directoryRole](directoryrole.md) | Lea las propiedades y las relaciones del objeto directoryRole. |
|[Crear miembro](../api/directoryrole_post_members.md) |[directoryObject](directoryobject.md)| Agregue un usuario al rol de directorio; para ello, publique en la propiedad de navegación de miembros.|
|[Enumerar miembros](../api/directoryrole_list_members.md) |Colección [directoryObject](directoryobject.md)| Obtenga los usuarios que son miembros del rol de directorio de la propiedad de navegación de miembros.|
|[Activar directoryRole](../api/directoryrole_post_directoryroles.md) |[directoryRole](directoryrole.md) | Active un rol de directorio.|

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|description|String|La descripción del rol de directorio. Solo lectura. |
|displayName|String|El nombre para mostrar del rol de directorio. Solo lectura. |
|id|String|El identificador único del rol de directorio. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL, solo lectura.|
|roleTemplateId|String| El **id** de la [directoryRoleTemplate](directoryroletemplate.md) en que se basa este rol. La propiedad debe especificarse al activar un rol de directorio en un inquilino con una operación POST. Una vez activado el rol de directorio, la propiedad es de solo lectura. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|members|Colección [directoryObject](directoryobject.md)|Usuarios que son miembros de este rol de directorio. Métodos HTTP: GET, POST, DELETE. Solo lectura. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "memberOf",
    "members",
    "ownedObjects",
    "owners"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryRole"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "roleTemplateId": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
