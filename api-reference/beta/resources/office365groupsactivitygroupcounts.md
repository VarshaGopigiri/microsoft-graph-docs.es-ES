---
title: tipo de recurso office365GroupsActivityGroupCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: ed5386083b11fb6fe7f063a4890744532feeb081
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832623"
---
# <a name="office365groupsactivitygroupcounts-resource-type"></a>tipo de recurso office365GroupsActivityGroupCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Description                              |
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
