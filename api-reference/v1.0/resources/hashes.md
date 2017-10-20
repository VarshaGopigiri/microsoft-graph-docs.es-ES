---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
ms.openlocfilehash: 9de6923146b915207fc771721d7aeb6767e9f99e
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
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
| **sha1Hash**     | String | Hash SHA1 para el contenido del archivo (si está disponible). Solo lectura. |
| **crc32Hash**    | String | El valor CRC32 del archivo (si está disponible). Solo lectura.            |
| **quickXorHash** | String | Un hash de propietario del archivo que se puede usar para determinar si ha cambiado el contenido del archivo (si está disponible). Solo lectura. |

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
