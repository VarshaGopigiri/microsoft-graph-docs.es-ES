---
title: tipo de recurso userActivationCounts
description: La siguiente es una representación JSON del recurso
author: dkershaw10
ms.openlocfilehash: 396f6182d000df6d701e8c0cbad3dd02a258c4c0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322921"
---
# <a name="useractivationcounts-resource-type"></a>tipo de recurso userActivationCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Descripción                              |
| :---------------- | :----- | ---------------------------------------- |
| ProductType ofrece       | String | El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365". |
| lastActivatedDate | Date   | La fecha de la última activación.       |
| Windows           | Int64  | El número de activación en Windows. Este número incluye cada activación en cualquier equipo de Windows. |
| mac               | Int64  | El número de activación en Mac OS.          |
| windows10Mobile   | Int64  | La activación contar en 10 de Windows mobile. |
| IOS               | Int64  | El número de activación en iOS.             |
| Android           | Int64  | El número de activación en un dispositivo Android.  |
| activatedOnSharedComputer   | Boolean | True si el usuario utiliza el producto en un equipo compartido antes. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.userActivationCounts"
} -->

```json
{
  "productType": "String", 
  "lastActivatedDate": "Date", 
  "windows": 1024, 
  "mac": 1024, 
  "windows10Mobile": 1024, 
  "ios": 1024, 
  "android": 1024,
  "activatedOnSharedComputer": true 
}
```
