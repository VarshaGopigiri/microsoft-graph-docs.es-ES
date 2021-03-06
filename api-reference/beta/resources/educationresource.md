---
title: tipo de recurso educationResource
description: Una superclase para todos los objetos de recursos en el sistema. Un recurso está asociado a una **asignación** o **envío**, que representa el objeto de aprendizaje que se va a
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 9ac84fd9d661f31186ea65e95c680456cdabe221
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982123"
---
# <a name="educationresource-resource-type"></a>tipo de recurso educationResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una superclase para todos los objetos de recursos en el sistema. Un recurso está asociado a una **asignación** o **envío**, que representa el objeto de aprendizaje que se va a entregar o de la presentación. No se puede crear una instancia un recurso directamente; debe realizar una subclase que representa el tipo de recurso que se va a utilizar.

Este recurso almacena las propiedades comunes en todos los tipos de recursos.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|Quién creó el recurso.|
|createdDateTime|Momento en el tiempo cuando se creó el recurso.  DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|displayName|Cadena|Nombre para mostrar del recurso.|
|lastModifiedBy|[identitySet](identityset.md)|¿Quién fue el último usuario para modificar el recurso.|
|lastModifiedDateTime|DateTimeOffset|Momento en el tiempo cuando se modificó por última vez el recurso.  El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationResource"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "displayName": "String",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
