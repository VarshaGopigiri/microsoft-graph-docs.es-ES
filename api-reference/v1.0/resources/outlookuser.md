---
title: Tipo de recurso outlookUser
description: Representa los servicios de Outlook disponibles para un usuario.
author: angelgolfer-ms
ms.openlocfilehash: 3a65206c74d16f7943d986e38b520ef388803c22
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314745"
---
# <a name="outlookuser-resource-type"></a>Tipo de recurso outlookUser


Representa los servicios de Outlook disponibles para un usuario.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear categoría](../api/outlookuser-post-mastercategories.md) | [outlookCategory](outlookcategory.md) |Crear un objeto **outlookCategory** en la lista principal de categorías del usuario.|
|[Enumerar categorías](../api/outlookuser-list-mastercategories.md) | Colección [outlookCategory](outlookcategory.md) |Obtener todas las categorías que han sido definidas por el usuario.|
|[supportedLanguages](../api/outlookuser-supportedlanguages.md) | Colección [localeInfo](localeinfo.md) | Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario. |
|[supportedTimeZones](../api/outlookuser-supportedtimezones.md) | Colección [timeZoneInformation](timezoneinformation.md) | Obtener una lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario. |


## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|masterCategories|Colección [outlookCategory](../resources/outlookcategory.md)| Lista de categorías definidas para el usuario. | 

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.outlookUser",
  "@odata.annotations": [
    {
      "property": "masterCategories",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    }
  ]
}-->
```json
{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->