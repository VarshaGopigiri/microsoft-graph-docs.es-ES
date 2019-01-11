---
title: tipo de recurso deviceDetail
description: Indica los detalles del dispositivo asociados con un dispositivo utilizado para iniciar sesión. Incluye información como el explorador del dispositivo y la información del sistema operativo, si el dispositivo es Azure AD administrado.
localization_priority: Normal
ms.openlocfilehash: ca4679a8c484b6dc5b36ef39d3d6d039537cbdbb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884843"
---
# <a name="devicedetail-resource-type"></a>tipo de recurso deviceDetail
Indica los detalles del dispositivo asociados con un dispositivo utilizado para iniciar sesión. Incluye información como el explorador del dispositivo y la información del sistema operativo, si el dispositivo es Azure AD administrado.



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|Explorador|Cadena|Indica la información del explorador del que se usa para iniciar sesión.|
|deviceId|Cadena|Hace referencia a la UniqueID del dispositivo usado para iniciar sesión.|
|displayName|Cadena|Hace referencia al nombre del dispositivo usado para iniciar sesión.|
|isCompliant|Boolean|Indica si el dispositivo es compatible con o no.|
|isManaged|Boolean|Indica si el dispositivo se administra o no.|
|operatingSystem|Cadena|Indica el nombre del sistema operativo y versión que usa para iniciar sesión.|
|trustType|String|Indica información de si el dispositivo que ha iniciado sesión está unido a dominio de área de trabajo se unió a, se unió a AzureAD. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.deviceDetail"
}-->

```json
{
  "browser": "String",
  "deviceId": "String",
  "displayName": "String",
  "isCompliant": true,
  "isManaged": true,
  "operatingSystem": "String",
  "trustType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "deviceDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
