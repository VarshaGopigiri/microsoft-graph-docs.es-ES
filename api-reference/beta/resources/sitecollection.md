# <a name="sitecollection-resource"></a>Recurso SiteCollection

El recurso **SiteCollection** proporciona más información acerca de una colección de sitios.

Si un recurso [**site**](site.md) tiene una propiedad **siteCollection** que no es NULL, site es un sitio raíz de una colección de sitios.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.siteCollection"
}-->

```json
{
  "hostname": "contoso.sharepoint.com"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad | Tipo    | Descripción                                                                                                                  |
|:--------------|:--------|:---------------------------------------------------
| **hostname**  | string  | Nombre de host de la colección de sitios. Solo lectura.


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
