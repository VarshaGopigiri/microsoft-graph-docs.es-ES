# <a name="provisionedplan-resource-type"></a>Tipo de recurso provisionedPlan

La propiedad **provisionedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|capabilityStatus|String|Por ejemplo, "Habilitado".|
|provisioningStatus|String|Por ejemplo, "Correcto".|
|service|String|Nombre del servicio; por ejemplo, "AccessControlS2S".|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.provisionedplan"
}-->

```json
{
  "capabilityStatus": "string",
  "provisioningStatus": "string",
  "service": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "provisionedPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->