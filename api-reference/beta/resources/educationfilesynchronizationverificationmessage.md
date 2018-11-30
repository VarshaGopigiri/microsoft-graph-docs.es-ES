---
title: tipo de recurso educationFileSynchronizationVerificationMessage
description: Representa un error devuelto al cliente en respuesta a una solicitud para iniciar la sincronización de perfiles de datos de school basada en CSV. El recurso va a contener errores derivados de la comprobación. Los usuarios deben corregir los datos de origen antes de reiniciar la solicitud para sincronizar con Azure Active Directory (AD Azure).
ms.openlocfilehash: cf685e0619c5600340df68ba86ecaef11a8a435d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083529"
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