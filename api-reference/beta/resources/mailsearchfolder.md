---
title: tipo de recurso mailSearchFolder
description: Una mailSearchFolder es una carpeta virtual en el buzón del usuario que contiene todos los elementos de correo electrónico que coincidan con los criterios de búsqueda especificada. mailSearchFolder hereda de mailFolder.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 1ba9ce248071e3d806383b4cd7e7550c1e3aa145
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920915"
---
# <a name="mailsearchfolder-resource-type"></a>tipo de recurso mailSearchFolder

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una mailSearchFolder es una carpeta virtual en el buzón del usuario que contiene todos los elementos de correo electrónico que coincidan con los criterios de búsqueda especificada. mailSearchFolder hereda de [mailFolder](mailfolder.md).

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto  | Descripción |
|:---------------|:--------|:----------|
| [Crear una carpeta de búsqueda](../api/mailsearchfolder-post.md) | [mailSearchFolder](mailsearchfolder.md) | Cree una carpeta de búsqueda en el buzón de este usuario. |
| [Carpetas de búsqueda de lista](../api/mailfolder-list-childfolders.md) | Colección [mailFolder](mailfolder.md) | Lista de todas las carpetas de este buzón de usuario, incluidas las carpetas de búsqueda. |
| [Obtener una carpeta de búsqueda](../api/mailfolder-get.md) | [mailSearchFolder](mailsearchfolder.md) | Obtener la carpeta de búsqueda especificada. |
| [Actualización de una carpeta de búsqueda](../api/mailsearchfolder-update.md) | [mailSearchFolder](mailsearchfolder.md) | Actualice la carpeta de búsqueda especificada. |
| [Eliminar una carpeta de búsqueda](../api/mailfolder-delete.md) | Ninguno | Elimine la carpeta de búsqueda especificada. |
| [Lista de todos los mensajes en una carpeta de búsqueda](../api/mailfolder-list-messages.md) | Colección [message](message.md) | Lista de todos los mensajes en la carpeta de búsqueda especificada. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
| isSupported | Booleano | Indica si una carpeta de búsqueda se puede editar mediante la API de REST. |
| includeNestedFolders | Booleano | Indica cómo se debe pasar por la jerarquía de carpetas de buzón de correo. `true`significa que debe ser una búsqueda en profundidad mientras `false` significa que se debe realizar una búsqueda no exhaustivos en su lugar. |
| sourceFolderIDs | Colección String | Las carpetas de buzón de correo que deben ser extraídas. |
| filterQuery | Cadena | La consulta de OData para filtrar los mensajes. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mailSearchFolder"
}-->

```json
{
  "isSupported": true,
  "includeNestedFolders": true,
  "sourceFolderIDs": ["string"],
  "filterQuery": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2018-01-23 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailSearchFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
