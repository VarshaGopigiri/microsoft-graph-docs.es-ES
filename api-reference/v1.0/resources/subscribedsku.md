# <a name="subscribedsku-resource-type"></a>Tipo de recurso subscribedSku

Contiene información acerca de una SKU de servicio a la que la empresa está suscrita.

Solo la operación de lectura es compatible con los SKU suscritos; crear, actualizar y eliminar no son compatibles. No se admiten expresiones de filtro de consulta.

Se hereda de [DirectoryObject](directoryobject.md).


## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get subscribedSku](../api/subscribedsku_get.md) | [subscribedSku](subscribedsku.md) |Lea las propiedades del objeto subscribedSku.|

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|capabilityStatus|Cadena|Por ejemplo, "Enabled", "LockedOut" y "Suspended".|
|consumedUnits|Int32|El número de licencias asignadas.|
|id|String|El identificador único del recurso del objeto sku suscrito. Clave. Solo lectura.|
|prepaidUnits|[licenseUnitsDetail](licenseunitsdetail.md)|Información sobre el número y el estado de las licencias prepagadas.|
|servicePlans|Colección [servicePlanInfo](serviceplaninfo.md)|Información acerca de los planes de servicio que están disponibles con el SKU.|
|skuId|Guid|El identificador único (GUID) para el SKU de servicio.|
|skuPartNumber|String|La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC".|
|appliesTo|Cadena|Por ejemplo, "usuario" o "empresa".|

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.subscribedSku"
}-->

```json
{
  "appliesTo": "string",
  "capabilityStatus": "string",
  "consumedUnits": 1024,
  "id": "string (identifier)",
  "prepaidUnits": {"@odata.type": "microsoft.graph.licenseUnitsDetail"},
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "guid",
  "skuPartNumber": "string"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscribedSku resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
