---
title: tipo de recurso synchronizationProgress
description: Representa el progreso de un synchronizationJob hasta su finalización.
ms.openlocfilehash: 412b7754dac97a36efe082026ab360569c0fe789
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090765"
---
# <a name="synchronizationprogress-resource-type"></a>tipo de recurso synchronizationProgress

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el progreso de un [synchronizationJob](synchronization-synchronizationjob.md) hasta su finalización.

## <a name="properties"></a>Propiedades

| Propiedad                              | Tipo      | Descripción    |
|:--------------------------------------|:----------|:---------------|
|completedUnits|Int32|El numerador de una relación de progreso; el número de unidades de cambios ya procesados.|
|progressObservationDateTime|DateTimeOffset|La hora de una observación de progreso como un desplazamiento en minutos de la hora UTC.|
|totalUnits|Int32|El denominador de una relación de progreso; un número de unidades de los cambios que va a procesar para llevar a cabo la sincronización.|
|unidades|String|Una descripción opcional de las unidades.|

<!-- The troubleshootingUrl property is missing a description -->

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationStatus"
}-->

```json
{
  "completedUnits": 1025,
  "progressObservationDateTime": "2017-10-10T17:00:00Z",
  "totalUnits": 3024,
  "units": "pages"
}

```

<!-- uuid: 15571993-7e2f-4842-84d5-01ceb67cdc05
20185-08-14 22:30:00 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationProcess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
