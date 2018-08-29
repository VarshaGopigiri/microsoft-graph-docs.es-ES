---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
ms.openlocfilehash: 92882910ecf86d19e1f0a8a5767d148f5aa95775
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23264038"
---
# <a name="hashes-resource-type"></a>Tipo de recurso Hashes

El recurso **Hashes** agrupa hashes disponibles en una sola estructura de un elemento.

**Nota:** No todos los servicios proporcionan un valor para todas las propiedades de hash enumeradas.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "sha1Hash", "crc32Hash", "quickXorHash" ],
  "@odata.type": "microsoft.graph.hashes"
}-->

```json
{
  "crc32Hash": "string (hex)",
  "sha1Hash": "string (hex)",
  "quickXorHash": "string (base64)"
}
```

## <a name="properties"></a>Propiedades

| Propiedad         | Tipo   | Descripción                                                       |
|:-----------------|:-------|:------------------------------------------------------------------|
| **sha1Hash**     | Cadena | Hash SHA1 para el contenido del archivo (si está disponible). Solo lectura. |
| **crc32Hash**    | Cadena | El valor de CRC32 del archivo en little endian (si está disponible). Solo lectura.            |
| **quickXorHash** | Cadena | Un hash de propietario del archivo que se puede usar para determinar si ha cambiado el contenido del archivo (si está disponible). Solo lectura. |

**Nota:** En algunos casos, puede que no estén disponibles los valores hash. Si este es el caso, los valores hash de un elemento se actualizarán después de que se descargue el elemento.

## <a name="remarks"></a>Comentarios

En OneDrive para la Empresa y SharePoint Server 2016, **sha1Hash** y **crc32Hash** no están disponibles.

En OneDrive Personal, **quickXorHash** no está disponible.

Para calcular **quickXorHash** para un archivo, haga referencia al [fragmento de código QuickXorHash](https://dev.onedrive.com/snippets/quickxorhash.htm).
Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- {
  "type": "#page.annotation",
  "description": "The hashes facet provides hash identifiers for a file in OneDrive",
  "keywords": "hash,sha1,crc32,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Hashes"
} -->
