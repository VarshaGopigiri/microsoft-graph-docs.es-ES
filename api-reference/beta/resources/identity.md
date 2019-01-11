---
author: rgregg
ms.author: rgregg
ms.date: 09/14/2017
title: Identidad
localization_priority: Normal
ms.openlocfilehash: c1cd28f4c2932e4196605c408470948e5b570894
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847589"
---
# <a name="identity-resource-type"></a>tipo de recurso de identidad

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **Identity** representa una identidad de un _actor_. Por ejemplo, un actor puede ser un usuario, un dispositivo o una aplicación.

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.identity", "optionalProperties": ["displayName", "tenantId", "thumbnails"], "openType": true } -->

```json
{
  "displayName": "string",
  "id": "string",
  "tenantId": "string",
  "thumbnails": { "@odata.type": "microsoft.graph.thumbnailSet" }
}
```

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo   | Descripción                                                                                                                                                                                                                                                                                                           |
|:--------------------|:-------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| displayName         | String | El nombre para mostrar de la identidad. Tenga en cuenta que puede que no esté siempre disponible o actualizado. Por ejemplo, si un usuario cambia su nombre para mostrar, la API puede mostrar el nuevo valor en una respuesta futura, pero los elementos asociados con el usuario no estarán modificados al usar [delta](../api/driveitem-delta.md).  |
| id                  | String | Identificador único de la identidad.                                                                                                                                                                                                                                                                                   |
| tenantId            | Cadena | Identidad única del inquilino (opcional).                                                                                                                                                                                                                                                                             |

## <a name="remarks"></a>Comentarios

En algunas circunstancias, puede que el identificador único del actor no esté disponible. En este caso, se devuelve la propiedad **displayName** de la identidad, pero faltará la propiedad **id** del recurso.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity contains information about an app, user, or group.",
  "keywords": "identity,owner,modifier,app,user,group",
  "section": "documentation",
  "tocPath": "Resources/Identity"
} -->
