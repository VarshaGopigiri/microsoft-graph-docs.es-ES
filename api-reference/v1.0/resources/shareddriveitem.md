---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharedDriveItem
ms.openlocfilehash: 3b4497c1a15704388dbb4bb4ba181d3985d65a69
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="shareddriveitem-resource-type"></a>Tipo de recurso de SharedDriveItem

El recurso **sharedDriveItem** se devuelve al usar la API [Shares](../api/shares_get.md) para obtener acceso a un objeto [driveItem](driveitem.md) compartido.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **sharedDriveItem**.

El recurso **sharedDriveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.sharedDriveItem"
}-->

```json
{
  "id": "string",
  "name": "string",
  "owner": { "@odata.type": "microsoft.graph.identitySet" },

  "driveItem": [ { "@odata.type": "microsoft.graph.driveItem" }],
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
| id       | String                        | El identificador único del recurso compartido al que se accede.              |
| name     | String                        | El nombre para mostrar del elemento compartido.                             |
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
| **driveItem**     | [**driveItem**][driveItem]            | Usado para obtener acceso al recurso **driveItem** subyacente.

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
