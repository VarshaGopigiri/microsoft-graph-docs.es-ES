---
title: " tipo de recurso complianceInformation"
description: Este recurso contiene cumplimiento seguro de los datos asociados con el control de puntuación.
ms.openlocfilehash: a32670c6d11d391834358b769ae938a67b3d8aad
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380962"
---
#  <a name="complianceinformation-resource-type"></a>tipo de recurso complianceInformation

Contiene el cumplimiento seguro de los datos asociados con el control de puntuación.

|Propiedad |Tipo |Descripción |
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
