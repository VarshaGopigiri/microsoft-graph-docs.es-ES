---
title: tipo de recurso office365GroupsActivityFileCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: adff009d9047aa147c8042059fbdab8491288fb7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972561"
---
# <a name="office365groupsactivityfilecounts-resource-type"></a>tipo de recurso office365GroupsActivityFileCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Descripción                              |
| :---------------- | :----- | ---------------------------------------- |
| reportRefreshDate | Fecha   | La fecha más reciente del contenido.          |
| total             | Int64  | El número total de archivos en la biblioteca de documentos de SharePoint del grupo. |
| activo            | Int64  | El número de archivos que se han visto, editado, compartidos o sincronizado en la biblioteca de documentos de SharePoint del grupo. |
| reportDate        | Fecha   | La fecha en la que estaba activo un número de archivos en el sitio de SharePoint del grupo. |
| reportPeriod      | Cadena | El número de días que cubre el informe.    |

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
