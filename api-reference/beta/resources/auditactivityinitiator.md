---
title: tipo de recurso auditActivityInitiator
description: El objeto de recurso que inicia la actividad de identidad. El iniciador puede ser un usuario, una aplicación o un sistema (que se considera como una aplicación)
ms.openlocfilehash: 834b39f67a9a3a251c61f15d3b1fa8aa964870e9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087869"
---
# <a name="auditactivityinitiator-resource-type"></a>tipo de recurso auditActivityInitiator
El objeto de recurso que inicia la actividad de identidad. El iniciador puede ser un usuario, una aplicación o un sistema (que se considera como una aplicación)



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|aplicación|[appIdentity](appidentity.md)|Si el recurso de inicio de la actividad es una aplicación, esta propiedad indica todos los de las aplicaciones relacionadas con la información como appId, nombre, servicePrincipalId, nombre.|
|usuario|[IdentidadDeUsuario](useridentity.md)|Si el recurso de inicio de la actividad es un usuario, esta propiedad indica todos los el usuario relacionadas con la información como userId, nombre, UserPrinicpalName.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.auditActivityInitiator"
}-->

```json
{
  "app": {"@odata.type": "microsoft.graph.appIdentity"},
  "user": {"@odata.type": "microsoft.graph.userIdentity"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "auditActivityInitiator resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->