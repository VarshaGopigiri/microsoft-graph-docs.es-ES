---
title: tipo de recurso office365ActivationsUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 90d9d2d8616f166eb9d8b87967898daa0468db54
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089740"
---
# <a name="office365activationsusercounts-resource-type"></a>tipo de recurso office365ActivationsUserCounts

## <a name="properties"></a>Propiedades

| Propiedad                 | Tipo   | Descripción                              |
| :----------------------- | :----- | ---------------------------------------- |
| reportRefreshDate        | Fecha   | La fecha más reciente del contenido.          |
| ProductType ofrece              | String | El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365". |
| asignado                 | Int64  | El número de usuarios se han asignado para la licencia del producto. |
| activado                | Int64  | El número de usuarios que ha activado el producto. |
| sharedComputerActivation | Int64  | El número de usuarios que han usado el producto en un equipo compartido. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActivationsUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "productType": "String", 
  "assigned": 1024, 
  "activated": 1024,
  "sharedComputerActivation": 1024
}
```
