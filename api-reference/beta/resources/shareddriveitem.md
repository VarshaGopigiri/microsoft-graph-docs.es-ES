---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharedDriveItem
localization_priority: Normal
ms.openlocfilehash: d20656351725f23d4fd4c00b65fdc88fe2f449b8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853070"
---
# <a name="shareddriveitem-resource-type"></a>Tipo de recurso SharedDriveItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **sharedDriveItem** se devuelve al usar la API [Shares](../api/shares-get.md) para obtener acceso a un objeto [driveItem](driveitem.md) compartido.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **sharedDriveItem**.

El recurso **sharedDriveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItem",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.sharedDriveItem"
}-->

```json
{
  "id": "string",
  "name": "string",
  "owner": { "@odata.type": "microsoft.graph.identitySet" },

  "driveItem": { "@odata.type": "microsoft.graph.driveItem" },
  "items": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "list": { "@odata.type": "microsoft.graph.list" },
  "listItem": { "@odata.type": "microsoft.graph.listItem" },
  "permission": { "@odata.type": "microsoft.graph.permission" },
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "site": { "@odata.type": "microsoft.graph.site" }
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo                          | Descripción                                                      |
| :------- | :---------------------------- | :--------------------------------------------------------------- |
| id       | String                        | El identificador único del recurso compartido al que se accede.              |
| name     | String                        | El nombre para mostrar del elemento compartido.                             |
| owner    | [IdentitySet](identityset.md) | Información sobre el propietario del elemento compartido al que se hace referencia. |

## <a name="relationships"></a>Relaciones

| Nombre de la relación | Tipo                | Descripción
| ------------------|:--------------------|:-----------------------------------
| **driveItem**     | [**driveItem**][driveItem] | Usado para obtener acceso al recurso **driveItem** subyacente.
| **list**          | [**list**][list]           | Usado para obtener acceso al recurso **list** subyacente.
| **listItem**      | [**listItem**][listItem]   | Usado para obtener acceso al recurso **listItem** subyacente.
| **permission**    | [**permiso**][permission] | Utilizado para tener acceso el **permiso** que representa el vínculo de uso compartido subyacente
| **site**          | [**site**][site]           | Usado para obtener acceso al recurso **site** subyacente.

O bien, para recursos **driveItem** compartidos de cuentas personales de OneDrive, también se pueden usar las siguientes relaciones.

| Nombre de la relación | Tipo                         | Descripción
| ------------------|:-----------------------------|:-----------------------------------
| **items**         | Colección [**driveItem**][driveItem] | Todos los recursos driveItem que se incluyen en la raíz de uso compartido. Esta colección no se puede enumerar.
| **driveItem**     | [**driveItem**][driveItem]            | Usado para obtener acceso al recurso **driveItem** subyacente.

[driveItem]: driveitem.md
[list]: list.md
[listItem]: listitem.md
[permission]: permission.md
[site]: site.md

## <a name="methods"></a>Métodos

| Método                                  | Ruta de acceso a REST                |
| :-------------------------------------- | :----------------------- |
| [Obtener el elemento compartido](../api/shares-get.md) | `GET /shares/{share-id}` |

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "Share resource returns information about a shared item or collection of items.",
  "keywords": "share,shared,sharing root,shared files, shared items",
  "section": "documentation",
  "tocPath": "Resources/Share"
} -->
