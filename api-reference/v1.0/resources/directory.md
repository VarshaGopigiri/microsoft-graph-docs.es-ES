# <a name="directory-resource-type-deleted-items"></a>Tipo de recurso directory (elementos eliminados)

Representa un elemento eliminado en el directorio. Cuando se elimina un elemento, se agrega al "contenedor" de elementos eliminados. Los elementos eliminados seguirán estando disponible para su restauración durante 30 días. Después de 30 días, los elementos se eliminan permanentemente.

Actualmente, la funcionalidad de elementos eliminados solo es compatible con los [grupos](group.md) y [usuarios](users.md) de Office 365.

## <a name="methods"></a>Métodos

| Método         | Tipo de valor devuelto | Descripción |
|:---------------|:------------|:------------|
|[Obtener elemento eliminado](../api/directory_deleteditems_get.md) | [directoryObject](directoryobject.md) | Obtiene las propiedades de un elemento eliminado. |
|[Restaurar elemento eliminado](../api/directory_deleteditems_restore.md) |[directoryObject](directoryobject.md)| Restaura un elemento eliminado recientemente. |
|[Enumerar elementos eliminados](../api/directory_deleteditems_list.md) |Colección de [directoryObject](directoryobject.md)| Obtiene una lista de elementos eliminados recientemente. |
|[Eliminar permanentemente un elemento](../api/directory_deleteditems_delete.md) | Ninguno | Elimina permanentemente un elemento. |
|[Lista de los elementos eliminados que pertenecen a un usuario](../api/directory_deleteditems_user_owned.md) | Colección de [directoryObject](directoryobject.md) | Se enumeran los elementos del directorio que pertenecen a un usuario. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|deleteditems|Colección de [directoryObject](directoryobject.md)| Elementos eliminados recientemente Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
}
```

## <a name="example"></a>Ejemplo

<!--{"blockType": "request"}-->
```http
GET https://graph.microsoft.com/v1.0/directory
```

<!--{"blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.directory"}-->
```json
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directory resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->