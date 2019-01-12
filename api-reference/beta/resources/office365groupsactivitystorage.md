---
title: tipo de recurso office365GroupsActivityStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 180e60a52b397f969aa10cee5bc27bba934ad1e4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944456"
---
# <a name="office365groupsactivitystorage-resource-type"></a>tipo de recurso office365GroupsActivityStorage

## <a name="properties"></a>Propiedades

| Propiedad                  | Tipo   | Descripción                              |
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
