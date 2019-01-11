---
title: Tipo de recurso Location
description: Representa información de ubicación de un evento.
localization_priority: Normal
ms.openlocfilehash: 650876596e2cf9336054957cfd4c95bf4dad16b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879404"
---
# <a name="location-resource-type"></a>Tipo de recurso Location

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa información de ubicación de un [event](event.md).

Hay varias maneras de crear eventos de calendario, por ejemplo, a través de una aplicación con la API de REST [crear evento](../api/user-post-events.md) o manualmente con la interfaz de usuario de Outlook. Al crear un evento con la interfaz de usuario, puede especificar la ubicación como texto sin formato (por ejemplo, "bar de Harry") o elegirla en la lista de salas proporcionada por Outlook, [Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/) o [Búsqueda local de Bing](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/). 

Según cómo se cree el evento, se espera que Outlook establezca la propiedad **locationType** de solo lectura de manera distinta. 

| Cómo se creó el evento  | Propiedad   | Valor esperado |
|:----------|:-------|:--------------------------------|
| API de REST [crear evento](../api/user-post-events.md) | **locationType** | `default` |
| Interfaz de usuario de Outlook | **locationType** | Uno de los siguientes: <ul><li>`default` en el caso de una ubicación especificada como texto sin formato.</li><li>`conferenceRoom` en el caso de una sala proporcionada por la lista de salas de Outlook.</li><li>O, cualquiera de esta lista (`homeAddress`, `businessAddress`, `geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness` o `postalAddress`) en el caso de una ubicación de Bing Autosuggest o de Búsqueda local de Bing.</li></ul> |




## <a name="properties"></a>Propiedades
| Propiedad  | Tipo   | Descripción                                                     |
|:----------|:-------|:----------------------------------------------------------------|
| address | [physicalAddress](physicaladdress.md) |Dirección postal de la ubicación. |
| coordinates | [outlookGeoCoordinates](outlookgeocoordinates.md) | Coordenadas geográficas y elevación de la ubicación. |
| displayName  | String | Nombre asociado a la ubicación.                       |
| locationEmailAddress | Cadena | Dirección de correo electrónico opcional de la ubicación |
| locationUri | String | URI opcional que representa la ubicación. |
| locationType | String | Tipo de ubicación. Los valores posibles son: `conferenceRoom`, `homeAddress`, `businessAddress`, `geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `default`, `localBusiness` y `postalAddress`. Solo lectura.|
| uniqueId | String | Solo para uso interno.|
| uniqueIdType | String | Solo para uso interno. |


## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.location"
}-->
```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "coordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "displayName": "string",
  "locationEmailAddress": "string",
  "locationUri": "string",
  "locationType": "string",
  "uniqueId": "string",
  "uniqueIdType": "string"
}

```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "location resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
