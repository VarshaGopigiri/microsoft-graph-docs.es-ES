---
title: tipo de recurso educationSynchronizationError
description: Representa un error durante la validación de perfiles de datos de escuela o sincronización. Se genera un error único para cada entrada que se produce un error al validar y sincronizar con Azure Active Directory (AD Azure).
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: e5cf502c76aca816e75293ec8ac64cc544eeef7b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852398"
---
# <a name="educationsynchronizationerror-resource-type"></a>tipo de recurso educationSynchronizationError

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un error durante la validación de perfiles de datos de escuela o sincronización. Se genera un error único para cada entrada que se produce un error al validar y sincronizar con Azure Active Directory (AD Azure).

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:-|:-|:-|
| [Obtener errores de sincronización](../api/educationsynchronizationerrors-get.md) | colección de **educationSynchronizationError**| Devuelve la lista de errores de sincronización asociado con un perfil. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:-|:-|:-|
| **entryType** | string |  Representa la entidad de sincronización (escuela, sección, estudiantes, profesor).       |
| **errorCode** | string |  Representa el código de error de este error.         |
| **errorMessage** | string |  Contiene una descripción del error.        |
| **joiningValue** | string |  El identificador único para la entrada.         |
| **recordedDateTime** | DateTimeOffset | El momento de la aparición de este error.         |
| **reportableIdentifier** | string | El identificador de entrada de este error.       |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationError"
}-->

```json
{
    "entryType": "String",
    "errorCode": "String",
    "errorMessage": "String",
    "joiningValue": "String",
    "recordedDateTime": "DateTimeOffset",
    "reportableIdentifier": "String"
}
```
