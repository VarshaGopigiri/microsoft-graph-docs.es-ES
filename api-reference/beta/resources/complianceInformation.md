---
title: " tipo de recurso complianceInformation"
description: Este recurso contiene cumplimiento seguro de los datos asociados con el control de puntuación.
localization_priority: Normal
ms.openlocfilehash: 7a3968e6e043d2019100870061c5e34b03b1b8bd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820604"
---
#  <a name="complianceinformation-resource-type"></a>tipo de recurso complianceInformation

Contiene el cumplimiento seguro de los datos asociados con el control de puntuación.

|Propiedad |Tipo |Description |
|:--|:--|:--|
|certificationName | string | Nombre de certificación de cumplimiento de normas (por ejemplo, ISO 27018:2014, GDPR, FedRAMP, NIST 800-171) |
|certificationControls | colección de [certificationControl](certificationcontrol.md) | Colección de los controles de certificación asociados con la certificación |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.complianceInformation"
}-->

```json
{
  "certificationName": "String",
  "certificationControls": "Collection(microsoft.graph.complianceInformation)"
}

```


<!-- {
  "type": "#page.annotation",
  "description": "complianceInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
