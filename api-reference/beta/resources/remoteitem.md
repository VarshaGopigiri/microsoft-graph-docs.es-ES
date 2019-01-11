---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: RemoteItem
localization_priority: Normal
ms.openlocfilehash: 122e13513db1a59e23a41cadd16e61996e6a6c04
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843193"
---
# <a name="remoteitem-resource-type"></a>Tipo de recurso RemoteItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **remoteItem** indica que un objeto [**driveItem**](driveitem.md) hace referencia a un elemento que existe en otra unidad. Este recurso proporciona los identificadores únicos de la unidad de origen y del elemento de destino.

Los objetos [**DriveItem**](driveitem.md) con una faceta **remoteItem** que no sea null son recursos que se comparten, agregan al OneDrive del usuario o que están en elementos devueltos de colecciones heterogéneas de elementos (como los resultados de la búsqueda).

**Nota:** A diferencia de las carpetas de la misma unidad, puede que a un objeto **driveItem** que se mueva a un elemento remoto se le cambie el valor `id`.

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.remoteItem", 
       "optionalProperties": ["name", "fileSystemInfo", "file", "folder"] } -->

```json
{
  "id": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "file": { "@odata.type": "microsoft.graph.file" },
  "fileSystemInfo": { "@odata.type": "microsoft.graph.fileSystemInfo" },
  "folder": { "@odata.type": "microsoft.graph.folder" },
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "name": "string",
  "package": { "@odata.type": "microsoft.graph.package" },
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "shared": { "@odata.type": "microsoft.graph.shared" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "size": 1024,
  "webDavUrl": "url",
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad        | Tipo                                | Descripción                                                                                                                                                       |
| :------------------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| createdBy            | [IdentitySet](identityset.md)       | Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.                                                                                  |
| createdDateTime      | Timestamp                           | Fecha y hora de creación del elemento. Solo lectura.                                                                                                                        |
| file                 | [File](file.md)                     | Indica que el elemento remoto es un archivo. Solo lectura.                                                                                                              |
| fileSystemInfo       | [FileSystemInfo](filesysteminfo.md) | Información sobre el elemento remoto del sistema de archivos local. Solo lectura.                                                                                          |
| folder               | [Folder](folder.md)                 | Indica que el elemento remoto es una carpeta. Solo lectura.                                                                                                            |
| id                   | String                              | Identificador único del elemento remoto en su unidad. Solo lectura.                                                                                                    |
| lastModifiedBy       | [IdentitySet](identityset.md)       | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.                                                                            |
| lastModifiedDateTime | Timestamp                           | Fecha y hora de la última modificación del elemento. Solo lectura.                                                                                                              |
| name                 | String                              | Opcional. Nombre de archivo del elemento remoto. Solo lectura.                                                                                                                 |
| paquete              | [Package](package.md)               | Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura. |
| parentReference      | [ItemReference](itemreference.md)   | Propiedades del elemento primario del elemento remoto. Solo lectura.                                                                                                           |
| shared               | [shared](shared.md)                 | Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.                                       |
| sharepointIds        | [SharepointIds](sharepointids.md)   | Proporciona interoperabilidad entre elementos de OneDrive para la Empresa y SharePoint con el conjunto completo de identificadores de elementos. Solo lectura.                                          |
| size                 | Int64                               | Tamaño del elemento remoto. Solo lectura.                                                                                                                               |
| webDavUrl            | Url                                 | Dirección URL compatible con DAV del elemento.                                                                                                                                  |
| webUrl               | Url                                 | Dirección URL que muestra el recurso en el explorador. Solo lectura.                                                                                                         |

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de un objeto **driveItem**, consulte [driveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "tocPath": "Facets/RemoteItem"
} -->
