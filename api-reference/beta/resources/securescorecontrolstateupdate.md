---
title: " tipo de recurso secureScoreControlStateUpdate"
description: Este recurso contiene el historial de Estados del control actualizado por usuario (los Estados de control incluyen predeterminado, Ignored, otros, revisada).
localization_priority: Normal
ms.openlocfilehash: 8d8c3122a6263ebc7b10b5edfb823953e2d587fc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888924"
---
 #  <a name="securescorecontrolstateupdate-resource-type"></a>tipo de recurso secureScoreControlStateUpdate
Contiene el historial de los Estados de control actualizado por el usuario (los Estados de control incluyen predeterminado, Ignored, otros, revisada).

|Propiedad |Tipo |Description |
|:--|:--|:--|
|assignedTo | string | Asignar el control para el usuario que llevará a cabo la acción |
|comment | string | Proporciona un comentario opcional sobre el control |
|state | string | Estado del control se puede modificar mediante el comando de revisión (ej: omite otros etcetera) |
|updatedBy | string |Identificador del usuario que se actualizó el estado de inquilinos |
|updatedDateTime | ¿DateTimeOffset? |En el control que se actualizó el estado de tiempo |
 ## <a name="json-representation"></a>Representación JSON
 La siguiente es una representación JSON del recurso
 <!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.secureScoreControlStateUpdate"
}-->
 ```json
{
  "assignedTo": "String",
  "comment": "Double",
  "state": "Double",
  "updatedBy": "Double",
  "updatedDateTime": "Double"
}
 ```
 <!-- {
  "type": "#page.annotation",
  "description": "secureScoreControlStateUpdate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
