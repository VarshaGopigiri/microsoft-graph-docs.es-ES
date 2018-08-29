# <a name="directoryobject-resource-type"></a>Tipo de recurso directoryObject

Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get directoryObject](../api/directoryobject_get.md) | [directoryObject](directoryobject.md) |Lee las propiedades de un objeto directory.|
|[Delete directoryObject](../api/directoryobject_delete.md) | Ninguno |Elimina un objeto directory. |
|[checkMemberGroups](../api/directoryobject_checkmembergroups.md)|Colección string|Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.|
|[getMemberGroups](../api/directoryobject_getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.|
|[getMemberObjects](../api/directoryobject_getmemberobjects.md)|Colección string| Devuelve todos los grupos y roles de directorio de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva. |
|[getByIds](../api/directoryobject_getbyids.md) | Colección [directoryObject](directoryobject.md) | Obtenga un conjunto de objetos de directorio basados en un conjunto de identificadores proporcionados. |

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|id|Cadena|Guid que es el identificador único para el objeto; por ejemplo, 12345678-9abc-def0-1234-56789abcde. Clave. No admite valores NULL. Solo lectura.|

## <a name="relationships"></a>Relaciones

Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directoryObject",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
