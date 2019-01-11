---
title: Tipo de recurso sectionGroup
description: Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.
localization_priority: Normal
ms.openlocfilehash: 9e955d91fa49642100694da66421665a0d67b3da
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855429"
---
# <a name="sectiongroup-resource-type"></a>Tipo de recurso sectionGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "parentNotebook",
    "parentSectionGroup",
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.sectiongroup"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "string",
  "sectionGroupsUrl": "string",
  "sectionsUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|id|Cadena|El identificador único del grupo de secciones. Solo lectura.|
|lastModifiedBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|displayName|Cadena|El nombre del grupo de secciones.|
|sectionGroupsUrl|Cadena|La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del grupo de secciones. Solo lectura.|
|sectionsUrl|Cadena|La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del grupo de secciones. Solo lectura.|
|self|Cadena|El punto de conexión donde puede obtener información detallada sobre el grupo de secciones. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|parentNotebook|[Notebook](notebook.md)|Bloc de notas que contiene el grupo de secciones. Solo lectura.|
|parentSectionGroup|[SectionGroup](sectiongroup.md)|Grupo de secciones que contiene el grupo de secciones. Solo lectura.|
|sectionGroups|Colección [SectionGroup](sectiongroup.md)|Grupos de secciones de la sección. Solo lectura. Admite valores NULL.|
|sections|Colección [Section](section.md)|Secciones del grupo de secciones. Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener grupo de secciones](../api/sectiongroup-get.md) | [SectionGroup](sectiongroup.md) |Leer las propiedades y las relaciones del grupo de secciones.|
|[Crear grupo de secciones](../api/sectiongroup-post-sectiongroups.md) |[SectionGroup](sectiongroup.md)| Crear un grupo de secciones publicándolo en el grupo de secciones especificado de la colección sectionGroups.|
|[Enumerar grupos de secciones](../api/sectiongroup-list-sectiongroups.md) |Colección [SectionGroup](sectiongroup.md)| Obtener una colección de grupos de secciones en el grupo de secciones especificado.|
|[Crear sección](../api/sectiongroup-post-sections.md) |[Section](section.md)| Crear una sección publicándola en el grupo de secciones especificado de la colección de secciones.|
|[Enumerar secciones](../api/sectiongroup-list-sections.md) |Colección [Section](section.md)| Obtener una colección de secciones en el grupo de secciones especificado.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
