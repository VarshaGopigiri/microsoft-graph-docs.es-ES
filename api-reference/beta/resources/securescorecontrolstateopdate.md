---
title: " tipo de recurso secureScoreControlStateUpdate"
description: Este recurso contiene el historial de Estados del control actualizado por usuario (los Estados de control incluyen predeterminado, Ignored, otros, revisada).
ms.openlocfilehash: ba98f2fc85f3f8e12355f9acf5d232599a7f29f7
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380969"
---
 #  <a name="securescorecontrolstateupdate-resource-type"></a>tipo de recurso secureScoreControlStateUpdate
Contiene el historial de los Estados de control actualizado por el usuario (los Estados de control incluyen predeterminado, Ignored, otros, revisada).

|Propiedad |Tipo |Descripción |
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
