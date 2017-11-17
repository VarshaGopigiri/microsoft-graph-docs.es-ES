# <a name="licenseunitsdetail-resource-type"></a>Tipo de recurso licenseUnitsDetail

La propiedad **prepaidUnits** de la entidad [subscribedSku](subscribedsku.md) es de tipo **licenseUnitsDetail**.

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:-------------|:-----|:----------|
|enabled|Int32| El número de unidades habilitadas. |
|suspended|Int32| El número de unidades suspendidas. |
|warning|Int32| El número de unidades que se encuentran en estado de advertencia. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseUnitsDetail"
}-->

```json
{
  "enabled": 1024,
  "suspended": 1024,
  "warning": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseUnitsDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
