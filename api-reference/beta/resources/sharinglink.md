---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingLink
ms.openlocfilehash: 094de0cbdb77fe427ba70b9418ced5cc6e9cc731
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084801"
---
# <a name="sharinglink-resource-type"></a>tipo de recurso sharingLink

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **sharingLink** agrupa los elementos de datos relacionados con el vínculo en una única estructura.

Si un recurso de [**permiso**](permission.md) tiene una faceta distintos de null **sharingLink** , el permiso representa un vínculo de uso compartido (a diferencia de los permisos concedidos a una persona o un grupo).

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
  "preventsDownload": false,
  "type": "view | edit | embed",
  "scope": "anonymous | organization",
  "webHtml": "string",
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo          | Descripción
|:---------------|:--------------|:-------------------------------------
| application    | [identity][]  | La aplicación con la que está asociada el vínculo.
| type           | String        | El tipo del vínculo creado.
| scope          | String        | El ámbito del vínculo representado por este permiso. El valor `anonymous` indica que cualquier usuario puede usar el vínculo, `organization` indica que solo pueden usar el vínculo los usuarios que han iniciado sesión en el mismo inquilino.
| preventsDownload | Booleano       | Si es true, a continuación, el usuario sólo puede usar este vínculo para ver el elemento en la web y no puede usar para descargar el contenido del elemento. Sólo para OneDrive para profesionales y SharePoint.
| webHtml        | String        | Para los vínculos `embed`, esta propiedad contiene el código HTML para un elemento `<iframe>` que insertará el elemento en una página web.
| webUrl         | String        | Una dirección URL que abre el elemento en el explorador en el sitio web de OneDrive.

[Identity]: identity.md

### <a name="type-options"></a>Opciones de tipo

En la tabla siguiente define los valores posibles para la propiedad **type** .

| Valor    | Rol     | Descripción
|:---------|:---------|:---------------------------------------------------------
| `view`   | `read`   | Un vínculo para compartir de solo vista, que permite el acceso de solo lectura.
| `edit`   | `write`  | Un vínculo para compartir de edición, que permite el acceso de lectura y escritura.
| `embed`  | `read`   | Un vínculo para compartir de solo vista que puede usarse para insertar contenido en una página web de host. La opción de inserción de vínculos no está disponible en OneDrive para la Empresa o SharePoint.

### <a name="scope-options"></a>Opciones de ámbito

En la tabla siguiente define los valores posibles para la propiedad de **ámbito** .

| Valor            | Descripción
|:-----------------|:------------------------------------------------------------
| `anonymous`      | Cualquier usuario con el vínculo tiene acceso, sin necesidad de iniciar sesión. Esto puede incluir personas fuera de la organización.
| `organization`   | Cualquier usuario que ha iniciado sesión en su organización (inquilino) puede usar el vínculo para obtener acceso. Sólo está disponible en OneDrive para profesionales y SharePoint.
| `existingAccess` | Sólo los usuarios que ya se hayan concedido el acceso al elemento a través de otros medios pueden obtener acceso al elemento con este vínculo. Sólo está disponible en OneDrive para profesionales y SharePoint.
| `users`          | El vínculo concede acceso sólo a una lista específica de personas. Sólo está disponible en OneDrive para profesionales y SharePoint.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The sharing link facet provides information about how a file is shared.",
  "keywords": "sharing,sharing link, sharing url, webUrl",
  "section": "documentation",
  "tocPath": ""
}-->
