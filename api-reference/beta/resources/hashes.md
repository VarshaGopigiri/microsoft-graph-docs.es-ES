---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Hashes
ms.openlocfilehash: 2387af83450f667aa4732cc46d7d3cf2111579f0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083441"
---
# <a name="hashes-resource-type"></a>Tipo de recurso Hashes

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
