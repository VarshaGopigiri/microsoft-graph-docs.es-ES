# <a name="worksheetprotection-resource-type"></a>Tipo de recurso WorksheetProtection

Representa la protección de un objeto de hoja.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get WorksheetProtection](../api/worksheetprotection_get.md) | [WorkbookWorksheetProtection](worksheetprotection.md) |Lee las propiedades y relaciones del objeto worksheetProtection.|
|[Protect](../api/worksheetprotection_protect.md)|Ninguno|Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.|
|[Unprotect](../api/worksheetprotection_unprotect.md)|Ninguno|Desprotege una hoja de cálculo.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|options|[WorkbookWorksheetProtectionOptions](worksheetprotectionoptions.md)|Opciones de protección de la hoja. Solo lectura.|
|protected|booleano|Indica si la hoja de cálculo está protegida.  Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookWorksheetProtection"
}-->

```json
{
  "protected": true,
  "options": { "@odata.type": "microsoft.graph.workbookWorksheetProtectionOptions" }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetProtection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->