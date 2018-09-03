---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharedDriveItem
ms.openlocfilehash: abcf686be46e15a523a1a88170981cb318e71b00
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268203"
---
# <a name="shareddriveitem-resource-type"></a>Tipo de recurso de SharedDriveItem

El recurso **sharedDriveItem** se devuelve al usar la API [Shares](../api/shares_get.md) para obtener acceso a un objeto [driveItem](driveitem.md) compartido.

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
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "site": { "@odata.type": "microsoft.graph.site" }
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo                          | Descripción                                                      |
| :------- | :---------------------------- | :--------------------------------------------------------------- |
| id       | Cadena                        | El identificador único del recurso compartido al que se accede.              |
| name     | Cadena                        | El nombre para mostrar del elemento compartido.                             |
| owner    | [IdentitySet](identityset.md) | Información sobre el propietario del elemento compartido al que se hace referencia. |

## <a name="relationships"></a>Relaciones

| Nombre de la relación | Tipo                | Descripción
| ------------------|:--------------------|:-----------------------------------
| **driveItem**     | [**driveItem**][driveItem]   | Usado para obtener acceso al recurso **driveItem** subyacente.
| **list**          | [**list**][list]        | Usado para obtener acceso al recurso **list** subyacente.
| **listItem**      | [**listItem**][listItem]    | Usado para obtener acceso al recurso **listItem** subyacente.
| **site**          | [**site**][site]        | Usado para obtener acceso al recurso **site** subyacente.

O bien, para recursos **driveItem** compartidos de cuentas personales de OneDrive, también se pueden usar las siguientes relaciones.

| Nombre de la relación | Tipo                         | Descripción
| ------------------|:-----------------------------|:-----------------------------------
| **items**         | Colección [**driveItem**][driveItem] | Todos los recursos driveItem que se incluyen en la raíz de uso compartido. Esta colección no se puede enumerar.
| **root**          | [**driveItem**][driveItem]   | Usado para obtener acceso al recurso **driveItem** subyacente. Obsoleto; use `driveItem` en su lugar.

[driveItem]: driveItem.md
[list]: list.md
[listItem]: listItem.md
[site]: site.md

## <a name="methods"></a>Métodos

| Método                                  | Ruta de acceso a REST                |
| :-------------------------------------- | :----------------------- |
| [Obtener el elemento compartido](../api/shares_get.md) | `GET /shares/{share-id}` |

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "Share resource returns information about a shared item or collection of items.",
  "keywords": "share,shared,sharing root,shared files, shared items",
  "section": "documentation",
  "tocPath": "Resources/Share"
} -->
