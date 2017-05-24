# <a name="sharepointids-resource-type"></a>Tipo de recurso SharePointIds

El recurso **SharePointIds** agrupa en una sola estructura los distintos identificadores de un elemento almacenado en un sitio de SharePoint o en OneDrive para la Empresa.

**Nota:** los elementos devueltos de OneDrive Personal no incluyen una faceta **SharePointIds**.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "listId", "listItemId", "listItemUniqueId", "siteId", "siteUrl", "webId" ],
  "@odata.type": "microsoft.graph.sharepointIds"
}-->

```json
{
    "listId": "string",
    "listItemId": "string",
    "listItemUniqueId": "string",
    "siteId": "string",
    "siteUrl": "url",
    "webId": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad         | Tipo         | Descripción                                                                                  |
| :--------------- | :----------- | :------------------------------------------------------------------------------------------- |
| listId           | cadena       | Identificador único (guid) de la lista del elemento en SharePoint.                              |
| listItemId       | string       | Identificador entero del elemento en la lista que lo contiene.                               |
| listItemUniqueId | cadena       | Identificador único (guid) del elemento contenido en OneDrive para la Empresa o en un sitio de SharePoint. |
| siteId           | cadena       | Identificador único (guid) de la colección de sitios del elemento (SPSite).                        |
| siteUrl          | string (URL) | La URL de SharePoint del sitio que contiene el elemento.                                      |
| webId            | cadena       | Identificador único (guid) del sitio del elemento (SPWeb).                                    |

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sharepointIds resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
