---
title: Tipo de recurso page
description: Una página de un bloc de notas de OneNote.
localization_priority: Normal
ms.openlocfilehash: 5928f430fcbfe9f41c6aa83e99d7dfe737e8e1c7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850137"
---
# <a name="page-resource-type"></a>Tipo de recurso page

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una página de un bloc de notas de OneNote.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "parentNotebook",
    "parentSection"
  ],
  "@odata.type": "microsoft.graph.onenotePage"
}-->

```json
{
  "content": "stream",
  "contentUrl": "string",
  "createdByAppId": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "level": 1024,
  "links": {"@odata.type": "microsoft.graph.pageLinks"},
  "order": 1024,
  "self": "string",
  "title": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|content|Secuencia|Contenido HTML de la página.|
|contentUrl|Cadena|Dirección URL del contenido HTML de la página.  Solo lectura.|
|createdByAppId|Cadena|Identificador único de la aplicación que creó la página. Solo lectura.|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|id|Cadena|Identificador único de la página.  Solo lectura.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó la página por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|nivel|Int32|Nivel de sangría de la página. Solo lectura.|
|vínculos|[PageLinks](pagelinks.md)|Vínculos para abrir la página. El vínculo `oneNoteClientURL` abre la página en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebUrl` abre la página en OneNote Online. Solo lectura.|
|order|Int32|El orden de la página dentro de su sección primaria. Solo lectura.|
|self|Cadena|El punto de conexión donde puede obtener información detallada sobre la página. Solo lectura.|
|title|Cadena|Título de la página. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|parentNotebook|[Notebook](notebook.md)|Bloc de notas que contiene la página.  Solo lectura.|
|parentSection|[Section](section.md)|Sección que contiene la página. Solo lectura.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener página](../api/page-get.md) | [Page](page.md) |Leer las propiedades y las relaciones de la página.|
|[Actualizar contenido de la página](../api/page-update.md) | Ninguno |Actualizar el contenido HTML de la página. |
|[Eliminar página](../api/page-delete.md) | Ninguno |Eliminar la página. |
|[copyToSection](../api/page-copytosection.md)| Ninguno |Copia la página en una sección específica.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
