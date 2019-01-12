---
title: Tipo de recurso WorksheetProtection
description: Representa la protección de un objeto de hoja.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 5b9faed56e545698cb731728b2c95fd31682b252
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916995"
---
# <a name="worksheetprotection-resource-type"></a>Tipo de recurso WorksheetProtection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la protección de un objeto de hoja.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get WorksheetProtection](../api/worksheetprotection-get.md) | [WorksheetProtection](worksheetprotection.md) |Lee las propiedades y relaciones del objeto worksheetProtection.|
|[Protect](../api/worksheetprotection-protect.md)|Ninguno|Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.|
|[Unprotect](../api/worksheetprotection-unprotect.md)|None|Desprotege una hoja de cálculo.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|protected|boolean|Indica si la hoja de cálculo está protegida.  Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|opciones|[WorksheetProtectionOptions](worksheetprotectionoptions.md)|Opciones de protección de la hoja. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.worksheetProtection"
}-->

```json
{
  "protected": true
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
