# <a name="onpremisesextensionattributes-resource-type"></a>Tipo de recurso onPremisesExtensionAttributes

La propiedad **onPremisesExtensionAttributes** de la entidad de [user](user.md) contiene quince propiedades de atributo de extensión personalizada. Para un usuario que tenga habilitado **onPremisesSyncEnabled**, este conjunto de propiedades se controla en Active Directory local, se sincroniza con Azure AD y es de solo lectura. Para un usuario de solo nube (para el que **onPremisesSyncEnabled** es falso), estas propiedades se pueden definir durante la creación o la actualización.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensionAttribute1|Cadena| Primer atributo de extensión personalizable. |
|extensionAttribute2|Cadena| Segundo atributo de extensión personalizable. |
|extensionAttribute3|Cadena| Tercer atributo de extensión personalizable. |
|extensionAttribute4|Cadena| Cuarto atributo de extensión personalizable. |
|extensionAttribute5|Cadena| Quinto atributo de extensión personalizable. |
|extensionAttribute6|Cadena| Sexto atributo de extensión personalizable. |
|extensionAttribute7|Cadena| Séptimo atributo de extensión personalizable. |
|extensionAttribute8|Cadena| Octavo atributo de extensión personalizable. |
|extensionAttribute9|Cadena| Noveno atributo de extensión personalizable. |
|extensionAttribute10|Cadena| Décimo atributo de extensión personalizable. |
|extensionAttribute11|Cadena| Undécimo atributo de extensión personalizable. |
|extensionAttribute12|Cadena| Duodécimo atributo de extensión personalizable. |
|extensionAttribute13|Cadena| Decimotercer atributo de extensión personalizable. |
|extensionAttribute14|Cadena| Decimocuarto atributo de extensión personalizable. |
|extensionAttribute15|Cadena| Decimoquinto atributo de extensión personalizable. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesExtensionAttributes"
}-->


```json
{
      "extensionAttribute1": "string",
      "extensionAttribute2": "string",
      "extensionAttribute3": "string",
      "extensionAttribute4": "string",
      "extensionAttribute5": "string",
      "extensionAttribute6": "string",
      "extensionAttribute7": "string",
      "extensionAttribute8": "string",
      "extensionAttribute9": "string",
      "extensionAttribute10": "string",
      "extensionAttribute11": "string",
      "extensionAttribute12": "string",
      "extensionAttribute13": "string",
      "extensionAttribute14": "string",
      "extensionAttribute15": "string"
  }

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesExtensionAttributes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->