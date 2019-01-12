---
title: tipo de recurso office365GroupsActivityGroupCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: d3c1272f9bd99c3e7ee0f29a4c303e1c8ca95525
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975886"
---
# <a name="office365groupsactivitygroupcounts-resource-type"></a>tipo de recurso office365GroupsActivityGroupCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Descripción                              |
| :---------------- | :----- | ---------------------------------------- |
| reportRefreshDate | Fecha   | La fecha más reciente del contenido.          |
| total             | Int64  | El número total de grupos.              |
| activo            | Int64  | El número de grupos de active. Un grupo se considera activo si se ha producido cualquiera de los siguientes: grupo de correo electrónico del buzón de correo recibido; usuario ve, edita, compartidos o sincronizados los archivos de biblioteca de documentos de SharePoint; usuario ve las páginas de SharePoint; usuario registrado, lea o había gustado los mensajes en grupos de Yammer. |
| reportDate        | Fecha   | La fecha en la que estaba activo un número de grupos. |
| reportPeriod      | Cadena | El número de días que cubre el informe.    |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityGroupCounts"
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
