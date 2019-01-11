---
title: tipo de recurso office365GroupsActivityStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 9824d3d172a8578f8a25a049c2d0d3b407bbc47e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862254"
---
# <a name="office365groupsactivitystorage-resource-type"></a>tipo de recurso office365GroupsActivityStorage

## <a name="properties"></a>Propiedades

| Propiedad                  | Tipo   | Description                              |
| :------------------------ | :----- | ---------------------------------------- |
| reportRefreshDate         | Fecha   | La fecha más reciente del contenido.          |
| mailboxStorageUsedInBytes | Int64  | El almacenamiento usado en el buzón de correo de grupo.       |
| siteStorageUsedInBytes    | Int64  | El almacenamiento utilizado en la biblioteca de documentos de SharePoint. |
| reportDate                | Fecha   | La fecha de instantánea para Exchange y SharePoint utiliza almacenamiento de información. |
| reportPeriod              | Cadena | El número de días que cubre el informe.    |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "mailboxStorageUsedInBytes": 1024, 
  "siteStorageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
