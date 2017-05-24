# <a name="licensedetails-resource-type"></a>Tipo de recurso licenseDetails

Contiene información sobre una licencia asignada a un usuario.

### <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar licenseDetails](../api/user_list_licensedetails.md) | Colección licenseDetails |Recupere una lista de objetos licenseDetails para un usuario.|

<!--|[Get licenseDetails](../api/licensedetails_get.md) | licenseDetails |Read properties and relationships of a licenseDetails object.|-->

### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Identificador único del objeto licenseDetails. Solo lectura, no admite valores NULL. |
|servicePlans|Colección [servicePlanInfo](serviceplaninfo.md)| Información sobre los planes de servicio asignados a la licencia. Solo lectura, no admite valores NULL. |
|skuId|Guid| Identificador único (GUID) del SKU de servicio. Es igual a la propiedad skuId en el objeto [SubscribedSku](subscribedsku.md) relacionado. Solo lectura |
|skuPartNumber|Cadena| Nombre para mostrar de SKU único. Es igual al skuPartNumber en el objeto [SubscribedSku](subscribedsku.md) relacionado; por ejemplo: "AAD_Premium". Solo lectura |

### <a name="relationships"></a>Relaciones
Ninguno

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseDetails"
}-->

```json
{
  "id": "String (identifier)",
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "Guid",
  "skuPartNumber": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->