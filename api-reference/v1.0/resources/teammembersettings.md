# <a name="teammembersettings-resource-type"></a>tipo de recurso teamMemberSettings



Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowCreateUpdateChannels|Booleano|Si se establece a miembros es true, puede agregar y actualizar los canales.|
|allowDeleteChannels|Booleano|Si se establece en true, miembros puede eliminar canales.|
|allowAddRemoveApps|Booleano|Si se establece a miembros es true, puede agregar y quitar aplicaciones.|
|allowCreateUpdateRemoveTabs|Booleano|Si se establece en true, miembros puede agregar, actualizar y quitar las fichas. |
|allowCreateUpdateRemoveConnectors|Booleano|Si se establece en true, miembros puede agregar, actualizar y quitar conectores.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMemberSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowDeleteChannels": true,
  "allowAddRemoveApps": true,
  "allowCreateUpdateRemoveTabs": true,
  "allowCreateUpdateRemoveConnectors": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's memberSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
