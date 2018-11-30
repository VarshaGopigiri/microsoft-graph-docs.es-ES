---
title: Tipo de recurso WorksheetProtection
description: Representa la protección de un objeto de hoja.
ms.openlocfilehash: aae92566503ce7bdb4a742c33b1a65c43937662c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030178"
---
# <a name="worksheetprotection-resource-type"></a>Tipo de recurso WorksheetProtection

Representa la protección de un objeto de hoja.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get WorksheetProtection](../api/worksheetprotection-get.md) | [WorkbookWorksheetProtection](worksheetprotection.md) |Lee las propiedades y relaciones del objeto worksheetProtection.|
|[Protect](../api/worksheetprotection-protect.md)|Ninguno|Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.|
|[Unprotect](../api/worksheetprotection-unprotect.md)|None|Desprotege una hoja de cálculo.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|opciones|[WorkbookWorksheetProtectionOptions](worksheetprotectionoptions.md)|Opciones de protección de la hoja. Solo lectura.|
|protected|boolean|Indica si la hoja de cálculo está protegida.  Solo lectura.|

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