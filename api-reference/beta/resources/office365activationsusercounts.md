---
title: tipo de recurso office365ActivationsUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: f57393a538631664be8845fdaeda9f35d07c986f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849311"
---
# <a name="office365activationsusercounts-resource-type"></a>tipo de recurso office365ActivationsUserCounts

## <a name="properties"></a>Propiedades

| Propiedad                 | Tipo   | Description                              |
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
