---
title: tipo de recurso office365ActivationCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 4787672df6462e8d1f343e4dace43ede7c79ff37
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991184"
---
# <a name="office365activationcounts-resource-type"></a>tipo de recurso office365ActivationCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Descripción                              |
| :---------------- | :----- | ---------------------------------------- |
| reportRefreshDate | Fecha   | La fecha más reciente del contenido.          |
| ProductType ofrece       | Cadena | El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365". |
| Windows           | Int64  | El número de activación en Windows. Este número incluye cada activación en cualquier equipo de Windows. |
| mac               | Int64  | El número de activación en Mac OS.          |
| Android           | Int64  | El número de activación en un dispositivo Android.  |
| IOS               | Int64  | El número de activación en iOS.             |
| windows10Mobile   | Int64  | La activación contar en 10 de Windows mobile. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActivationCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "productType": "String", 
  "windows": 1024, 
  "mac": 1024, 
  "android": 1024, 
  "ios": 1024, 
  "windows10Mobile": 1024
}
```
