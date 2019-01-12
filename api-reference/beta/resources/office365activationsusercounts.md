---
title: tipo de recurso office365ActivationsUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 3dc497e516f95f1e05167703f2b9f8aea6363a64
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917724"
---
# <a name="office365activationsusercounts-resource-type"></a>tipo de recurso office365ActivationsUserCounts

## <a name="properties"></a>Propiedades

| Propiedad                 | Tipo   | Descripción                              |
| :----------------------- | :----- | ---------------------------------------- |
| reportRefreshDate        | Fecha   | La fecha más reciente del contenido.          |
| ProductType ofrece              | Cadena | El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365". |
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
