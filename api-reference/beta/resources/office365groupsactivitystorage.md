---
title: tipo de recurso office365GroupsActivityStorage
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 23ff4d112373f52c4c19d6631ac89bac22399b29
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089926"
---
# <a name="office365groupsactivitystorage-resource-type"></a>tipo de recurso office365GroupsActivityStorage

## <a name="properties"></a>Propiedades

| Propiedad                  | Tipo   | Descripción                              |
| :------------------------ | :----- | ---------------------------------------- |
| reportRefreshDate         | Fecha   | La fecha más reciente del contenido.          |
| mailboxStorageUsedInBytes | Int64  | El almacenamiento usado en el buzón de correo de grupo.       |
| siteStorageUsedInBytes    | Int64  | El almacenamiento utilizado en la biblioteca de documentos de SharePoint. |
| reportDate                | Fecha   | La fecha de instantánea para Exchange y SharePoint utiliza almacenamiento de información. |
| reportPeriod              | String | El número de días que cubre el informe.    |

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
