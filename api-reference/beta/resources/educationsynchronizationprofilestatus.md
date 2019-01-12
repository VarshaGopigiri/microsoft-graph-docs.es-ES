---
title: tipo de recurso educationSynchronizationProfileStatus
description: 'Representa el estado de sincronización de un perfil de sincronización de datos de school. '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: d16619b0cf1e2c09358cf585b896b0c7c7d4f318
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928930"
---
# <a name="educationsynchronizationprofilestatus-resource-type"></a>tipo de recurso educationSynchronizationProfileStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el estado de sincronización del school datos [perfil de sincronización](educationsynchronizationprofile.md). 

> **Nota:** Se pueden retrasar las actualizaciones de la **educationSynchronizationProfileStatus** debido a la naturaleza asincrónica de procesamiento de sincronización en segundo plano.

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:-|:-|:-|
| [Obtener el estado de una sincronización](../api/educationsynchronizationprofilestatus-get.md) | **educationSynchronizationProfileStatus** | Devolver el estado de un perfil de sincronización específica. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **status** | string | El estado de una sincronización. Los valores posibles son: `paused`, `inProgress`, `success`, `error`, `quarantined`, `validationError`. |
| **lastSynchronizationDateTime** | DateTimeOffset | Representa el tiempo cuando se han observado cambios más recientes en el directorio.  |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationProfileStatus"
}-->

```json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/synchronizationProfiles('{id}')/profileStatus/$entity",
    "status": {"@odata.type":"microsoft.graph.educationSynchronizationStatus"},
    "lastSynchronizationDateTime": "DateTimeOffset"
}
```
