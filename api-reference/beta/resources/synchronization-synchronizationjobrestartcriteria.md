---
title: tipo de recurso synchronizationJobRestartCriteria
description: 'Define el ámbito de la [synchronizationJob: reinicie](../api/synchronization_synchronizationjob_restart.md) acción.'
localization_priority: Normal
ms.openlocfilehash: e26bae2e418da22a2b56e3acb973e4111066df23
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867882"
---
# <a name="synchronizationjobrestartcriteria-resource-type"></a>tipo de recurso synchronizationJobRestartCriteria

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define el ámbito de la [synchronizationJob: reinicie](../api/synchronization_synchronizationjob_restart.md) acción.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|resetScope|Cadena| Combinación de separados por comas de los valores siguientes: `Full`, `QuarantineState`, `Watermark`, `Escrows`, `ConnectorDataStore`. Uso `Full` si desea que todas las opciones.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationJobRestartCriteria"
}-->

```json
{
  "resetScope": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationJobRestartCriteria resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
