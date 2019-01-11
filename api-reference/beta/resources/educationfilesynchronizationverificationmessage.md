---
title: tipo de recurso educationFileSynchronizationVerificationMessage
description: Representa un error devuelto al cliente en respuesta a una solicitud para iniciar la sincronización de perfiles de datos de school basada en CSV. El recurso va a contener errores derivados de la comprobación. Los usuarios deben corregir los datos de origen antes de reiniciar la solicitud para sincronizar con Azure Active Directory (AD Azure).
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: ae09ec3f208adfee64a6392db9732841fc7a0808
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845517"
---
# <a name="educationfilesynchronizationverificationmessage-resource-type"></a>tipo de recurso educationFileSynchronizationVerificationMessage

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un error devuelto al cliente en respuesta a una solicitud para [iniciar la sincronización](../api/educationsynchronizationprofile-start.md) para los perfiles de datos basada en CSV school. El recurso va a contener errores derivados de la comprobación. Los usuarios deben corregir los datos de origen antes de reiniciar la solicitud para sincronizar con Azure Active Directory (AD Azure).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **type** | string | Tipo de mensaje. Los valores posibles son: `error`, `warning` y `information`. | 
| **nombre de archivo** | string | Archivo de origen que contiene el error. |
| **description** | string | Obtener información detallada sobre el tipo de mensaje. |

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFileSynchronizationVerificationMessage"
}-->

```json
{
    "type": "String",
    "fileName": "String",
    "description": "String"
}
```
