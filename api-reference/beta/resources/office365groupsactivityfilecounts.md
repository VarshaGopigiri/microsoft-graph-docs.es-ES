---
title: tipo de recurso office365GroupsActivityFileCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: eb2d967108d4f75064b91670ae43fb7a2dd7ce7a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084336"
---
# <a name="office365groupsactivityfilecounts-resource-type"></a>tipo de recurso office365GroupsActivityFileCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Descripción                              |
| :---------------- | :----- | ---------------------------------------- |
| reportRefreshDate | Fecha   | La fecha más reciente del contenido.          |
| total             | Int64  | El número total de archivos en la biblioteca de documentos de SharePoint del grupo. |
| activo            | Int64  | El número de archivos que se han visto, editado, compartidos o sincronizado en la biblioteca de documentos de SharePoint del grupo. |
| reportDate        | Fecha   | La fecha en la que estaba activo un número de archivos en el sitio de SharePoint del grupo. |
| reportPeriod      | String | El número de días que cubre el informe.    |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {

  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityFileCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "total": 1024, 
  "active": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
