---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Paquete
ms.openlocfilehash: 12ae750a0f4fbe0e951554308d4041928c31a16d
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267545"
---
# <a name="package-resource-type"></a>Tipo de recurso Package

El recurso **Package** indica que un objeto DriveItem es el elemento de nivel superior en un "paquete" o una colección de elementos que deben tratarse como una colección en lugar de elementos individuales.

Un ejemplo de un paquete es un bloc de notas de OneNote. Mientras que el bloc de notas se compone de archivos y carpetas que representan el contenido del bloc de notas, el elemento de nivel superior que representa el bloc de notas tiene una faceta **package** para indicar a los clientes que se trata de una colección de datos que se deberían tratar de forma especial.

Los objetos DriveItem con la faceta **package** no incluyen una faceta **folder** o **file**, pero son similares de forma conceptual a un elemento con una faceta **folder**.

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.package" } -->
```json
{
  "type": "oneNote"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad | Tipo   | Descripción                                                                                                                                                                      |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type          | cadena | Una cadena que indica el tipo de paquete. Mientras que `oneNote` es el único valor definido actualmente, debe esperar que se devuelvan otros tipos de paquetes y debe controlarlos en consecuencia. |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- {
  "type": "#page.annotation",
  "description": "The Package facet indicates that an item is the root of a special collection of items that should be treated as a single unit.",
  "keywords": "package, facet, onenote",
  "section": "documentation",
  "tocPath": "Facets/Package"
} -->
