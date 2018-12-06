---
title: 'Paginación de los datos de Microsoft Graph en la aplicación '
description: 'La propiedad odata.nextLink` en la respuesta que contiene una dirección URL a la siguiente página de resultados. '
ms.openlocfilehash: 9a9224a6dc710fa70ebec2448bf2eef2238968ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092911"
---
# <a name="paging-microsoft-graph-data-in-your-app"></a>Paginación de los datos de Microsoft Graph en la aplicación 

Algunas consultas realizadas en Microsoft Graph devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro `$top` para limitar específicamente el tamaño de página en una solicitud. Cuando un conjunto de resultados abarca varias páginas, Microsoft Graph devuelve una propiedad `@odata.nextLink` en la respuesta que contiene una dirección URL a la siguiente página de resultados. 

Por ejemplo, la dirección URL siguiente solicita todos los usuarios de una organización con un tamaño de página de 5 especificado con el parámetro de consulta `$top`:

```html
https://graph.microsoft.com/v1.0/users?$top=5
```

Si el resultado contiene más de cinco usuarios, Microsoft Graph devolverá una propiedad `@odata:nextLink` similar a la siguiente junto con la primera página de usuarios.

```json
"@odata.nextLink": "https://graph.microsoft.com/v1.0/users?$top=5&$skiptoken=X%274453707 ... 6633B900000000000000000000%27"
```

Para recuperar la siguiente página de resultados, se envía el valor de dirección URL de la propiedad `@odata:nextLink` a Microsoft Graph. 

```html
https://graph.microsoft.com/v1.0/users?$top=5&$skiptoken=X%274453707 ... 6633B900000000000000000000%27
```

Microsoft Graph continuará devolviendo una referencia a la siguiente página de datos en la propiedad `@odata:nextLink` con cada respuesta, hasta que se hayan leído todas las páginas del resultado.

>**Importante:** Debe incluir la dirección URL completa en la propiedad `@odata:nextLink` de la solicitud de la siguiente página de resultados. Según la API en la que se realice la consulta, el valor de dirección URL `@odata:nextLink` contendrá un `$skiptoken` o un parámetro de consulta `$skip`. La dirección URL contiene también todos los demás parámetros de consulta presentes en la solicitud original. No intente extraer `$skiptoken` ni el valor `$skip` y usarlo en una solicitud diferente. 

El comportamiento de paginación varía entre las distintas API de Microsoft Graph. Al trabajar con datos paginados tenga en cuenta lo siguiente:

- Las distintas API pueden tener tamaños de página predeterminados y máximos diferentes.
- Las distintas API pueden comportarse de forma diferente si se especifica un tamaño de página (a través del parámetro de consulta `$top`) que supera el tamaño máximo de página para la API. Según la API, se puede omitir el tamaño de página solicitado, se puede usar el tamaño de página máximo predeterminado para la API o Microsoft Graph puede devolver un error. 
- No todos los recursos o relaciones admiten la paginación. Por ejemplo, las consultas a [directoryRoles](/graph/api/resources/directoryrole?view=graph-rest-1.0) no admiten la paginación. Esto incluye los objetos de rol de lectura así como los miembros de rol.
