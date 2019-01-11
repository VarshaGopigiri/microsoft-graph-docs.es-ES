---
title: tipo de recurso userActivationCounts
description: La siguiente es una representación JSON del recurso
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: cae194545f13d312ee78b572659017752e43a6a6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845293"
---
# <a name="useractivationcounts-resource-type"></a>tipo de recurso userActivationCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Description                              |
| :---------------- | :----- | ---------------------------------------- |
| ProductType ofrece       | Cadena | El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365". |
| lastActivatedDate | Fecha   | La fecha de la última activación.       |
| Windows           | Int64  | El número de activación en Windows. Este número incluye cada activación en cualquier equipo de Windows. |
| mac               | Int64  | El número de activación en Mac OS.          |
| windows10Mobile   | Int64  | La activación contar en 10 de Windows mobile. |
| IOS               | Int64  | El número de activación en iOS.             |
| Android           | Int64  | El número de activación en un dispositivo Android.  |
| activatedOnSharedComputer   | Booleano | True si el usuario utiliza el producto en un equipo compartido antes. |

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
