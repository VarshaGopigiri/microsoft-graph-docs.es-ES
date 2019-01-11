---
title: tipo de recurso office365ActivationCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 30386b3833b8140d4c602e27cb3a78f3a68670dc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824993"
---
# <a name="office365activationcounts-resource-type"></a>tipo de recurso office365ActivationCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Description                              |
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
