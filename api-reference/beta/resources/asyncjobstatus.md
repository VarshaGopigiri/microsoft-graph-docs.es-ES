---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: AsyncJobStatus
localization_priority: Normal
ms.openlocfilehash: 8c442ad8ff3b23d20e8377a224a3f67b00163f5f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820968"
---
# <a name="asyncjobstatus-resource"></a>Recurso AsyncJobStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Este recurso proporciona información sobre el estado del progreso de un trabajo asincrónico.

La API siguiente llama a los recursos **AsyncJobStatus** de devolución:

* [Copiar elemento](../api/driveitem-copy.md)

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@type": "microsoft.graph.asyncJobStatus", "@type.aka": "oneDrive.asyncOperationStatus" } -->

```json
{
  "percentageComplete": 100.0,
  "status": "notStarted | inProgress | completed | updating | failed | deletePending | deleteFailed | waiting"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad          | Tipo   | Descripción                                                                                |
|:-----------------------|:-------|:-------------------------------------------------------------------------------------------|
| **percentageComplete** | Double | Un valor entre 0 y 100 que indica el porcentaje completado.                          |
| **status**             | String | Un valor de cadena que se asigna a una enumeración de posibles valores sobre el estado del trabajo. |

<!-- {
  "type": "#page.annotation",
  "description": "AsyncJobResource provides details about how to poll for an async completion.",
  "keywords": "async,job status,async status,copy,upload from url",
  "section": "documentation"
} -->
