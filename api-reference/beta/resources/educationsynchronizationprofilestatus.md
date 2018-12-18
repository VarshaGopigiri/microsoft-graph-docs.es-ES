---
title: tipo de recurso educationSynchronizationProfileStatus
description: 'Representa el estado de sincronización de un perfil de sincronización de datos de school. '
author: mmast-msft
ms.openlocfilehash: c92ba2226b28896f8df89a7aee66602651344154
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326001"
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