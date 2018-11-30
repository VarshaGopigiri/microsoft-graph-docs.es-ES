---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingLink
ms.openlocfilehash: 7639dab9f63a948b3e9a849d8d320de60f5a0954
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029328"
---
# <a name="sharinglink-resource-type"></a>Tipo de recurso SharingLink

El recurso **SharingLink** agrupa en una sola estructura los elementos de datos relacionados con vínculos.

Si un recurso [**Permission**](permission.md) tiene una faceta **sharingLink** que no es NULL, el permiso representa un vínculo para compartir (a diferencia de los permisos concedidos a una persona o un grupo).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "application", "scope" ],
  "@odata.type": "microsoft.graph.sharingLink"
}-->

```json
{
  "application": { "@odata.type": "microsoft.graph.identity" },
  "type": "view | edit | embed",
  "scope": "anonymous | organization",
  "webHtml": "string",
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo          | Descripción
|:------------|:--------------|:-------------------------------------
| application | [identity][]  | La aplicación con la que está asociada el vínculo.
| type        | String        | El tipo del vínculo creado.
| scope       | String        | El ámbito del vínculo representado por este permiso. El valor `anonymous` indica que cualquier usuario puede usar el vínculo, `organization` indica que solo pueden usar el vínculo los usuarios que han iniciado sesión en el mismo inquilino.
| webHtml     | Cadena        | Para los vínculos `embed`, esta propiedad contiene el código HTML para un elemento `<iframe>` que insertará el elemento en una página web.
| webUrl      | String        | Una dirección URL que abre el elemento en el explorador en el sitio web de OneDrive.

[Identity]: identity.md

## <a name="type-options"></a>Opciones de tipo

Esta tabla define los valores posibles de la propiedad **type**:

| Valor   | Rol    | Descripción
|:--------|:--------|:---------------------------------------------------------
| `view`  | `read`  | Un vínculo para compartir de solo vista, que permite el acceso de solo lectura.
| `edit`  | `write` | Un vínculo para compartir de edición, que permite el acceso de lectura y escritura.
| `embed` | `read`  | Un vínculo para compartir de solo vista que puede usarse para insertar contenido en una página web de host. La opción de inserción de vínculos no está disponible en OneDrive para la Empresa o SharePoint.

## <a name="scope-options"></a>Opciones de ámbito

| Valor          | Descripción
|:---------------|:------------------------------------------------------------
| `anonymous`    | Cualquier usuario con el vínculo tiene acceso, sin necesidad de iniciar sesión. Esto puede incluir personas fuera de la organización.
| `organization` | Cualquier usuario que ha iniciado sesión en su organización (inquilino) puede usar el vínculo para obtener acceso. Sólo está disponible en OneDrive para profesionales y SharePoint.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The sharing link facet provides information about how a file is shared.",
  "keywords": "sharing,sharing link, sharing url, webUrl",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/sharinglink.md:
      Found potential enums in resource example that weren't defined in a table:(view,edit,embed) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/sharinglink.md:
      Found potential enums in resource example that weren't defined in a table:(anonymous,organization) are in resource, but () are in table"
  ],
  "tocPath": "Facets/SharingLink"
} -->
