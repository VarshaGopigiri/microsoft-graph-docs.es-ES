---
title: 'Paginación de los datos de Microsoft Graph en la aplicación '
description: 'La propiedad odata.nextLink` en la respuesta que contiene una dirección URL a la siguiente página de resultados. '
author: piotrci
localization_priority: Priority
ms.openlocfilehash: 6a19d1873057f5a6f6ea1749a6941389b9be8eb5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830663"
---
# <a name="paging-microsoft-graph-data-in-your-app"></a><span data-ttu-id="7e811-103">Paginación de los datos de Microsoft Graph en la aplicación</span><span class="sxs-lookup"><span data-stu-id="7e811-103">Paging Microsoft Graph data in your app</span></span> 

<span data-ttu-id="7e811-p101">Algunas consultas realizadas en Microsoft Graph devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro `$top` para limitar específicamente el tamaño de página en una solicitud. Cuando un conjunto de resultados abarca varias páginas, Microsoft Graph devuelve una propiedad `@odata.nextLink` en la respuesta que contiene una dirección URL a la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="7e811-p101">Some queries against Microsoft Graph return multiple pages of data either due to server-side paging or due to the use of the `$top` query parameter to specifically limit the page size in a request. When a result set spans multiple pages, Microsoft Graph returns an `@odata.nextLink` property in the response that contains a URL to the next page of results.</span></span> 

<span data-ttu-id="7e811-106">Por ejemplo, la dirección URL siguiente solicita todos los usuarios de una organización con un tamaño de página de 5 especificado con el parámetro de consulta `$top`:</span><span class="sxs-lookup"><span data-stu-id="7e811-106">For example, the following URL requests all the users in an organization with a page size of 5, specified with the `$top` query parameter:</span></span>

```html
https://graph.microsoft.com/v1.0/users?$top=5
```

<span data-ttu-id="7e811-107">Si el resultado contiene más de cinco usuarios, Microsoft Graph devolverá una propiedad `@odata:nextLink` similar a la siguiente junto con la primera página de usuarios.</span><span class="sxs-lookup"><span data-stu-id="7e811-107">If the result contains more than five users, Microsoft Graph will return an `@odata:nextLink` property similar to the following along with the first page of users.</span></span>

```json
"@odata.nextLink": "https://graph.microsoft.com/v1.0/users?$top=5&$skiptoken=X%274453707 ... 6633B900000000000000000000%27"
```

<span data-ttu-id="7e811-108">Para recuperar la siguiente página de resultados, se envía el valor de dirección URL de la propiedad `@odata:nextLink` a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="7e811-108">You can retrieve the next page of results by sending the URL value of the `@odata:nextLink` property to Microsoft Graph.</span></span> 

```html
https://graph.microsoft.com/v1.0/users?$top=5&$skiptoken=X%274453707 ... 6633B900000000000000000000%27
```

<span data-ttu-id="7e811-109">Microsoft Graph continuará devolviendo una referencia a la siguiente página de datos en la propiedad `@odata:nextLink` con cada respuesta, hasta que se hayan leído todas las páginas del resultado.</span><span class="sxs-lookup"><span data-stu-id="7e811-109">Microsoft Graph will continue to return a reference to the next page of data in the `@odata:nextLink` property with each response until all pages of the result have been read.</span></span>

><span data-ttu-id="7e811-110">**Importante:** Debe incluir la dirección URL completa en la propiedad `@odata:nextLink` de la solicitud de la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="7e811-110">**Important:** You should include the entire URL in the `@odata:nextLink` property in your request for the next page of results.</span></span> <span data-ttu-id="7e811-111">Según la API en la que se realice la consulta, el valor de dirección URL `@odata:nextLink` contendrá un `$skiptoken` o un parámetro de consulta `$skip`.</span><span class="sxs-lookup"><span data-stu-id="7e811-111">Depending on the API that the query is being performed against, the `@odata:nextLink` URL value will contain either a `$skiptoken` or a `$skip` query parameter.</span></span> <span data-ttu-id="7e811-112">La dirección URL contiene también todos los demás parámetros de consulta presentes en la solicitud original.</span><span class="sxs-lookup"><span data-stu-id="7e811-112">The URL also contains all the other query parameters present in the original request.</span></span> <span data-ttu-id="7e811-113">No intente extraer `$skiptoken` ni el valor `$skip` y usarlo en una solicitud diferente.</span><span class="sxs-lookup"><span data-stu-id="7e811-113">Do not try to extract the `$skiptoken` or `$skip` value and use it in a different request.</span></span> 

<span data-ttu-id="7e811-114">El comportamiento de paginación varía entre las distintas API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="7e811-114">Paging behavior varies across different Microsoft Graph APIs.</span></span> <span data-ttu-id="7e811-115">Al trabajar con datos paginados tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7e811-115">Consider the following when working with paged data:</span></span>

- <span data-ttu-id="7e811-116">Las distintas API pueden tener tamaños de página predeterminados y máximos diferentes.</span><span class="sxs-lookup"><span data-stu-id="7e811-116">Different APIs might have different default and maximum page sizes.</span></span>
- <span data-ttu-id="7e811-117">Las distintas API pueden comportarse de forma diferente si se especifica un tamaño de página (a través del parámetro de consulta `$top`) que supera el tamaño máximo de página para la API.</span><span class="sxs-lookup"><span data-stu-id="7e811-117">Different APIs might behave differently if you specify a page size (via the `$top` query parameter) that exceeds the maximum page size for that API.</span></span> <span data-ttu-id="7e811-118">Según la API, se puede omitir el tamaño de página solicitado, se puede usar el tamaño de página máximo predeterminado para la API o Microsoft Graph puede devolver un error.</span><span class="sxs-lookup"><span data-stu-id="7e811-118">Depending on the API, the requested page size might be ignored, it might default to the maximum page size for that API, or Microsoft Graph might return an error.</span></span> 
- <span data-ttu-id="7e811-p105">No todos los recursos o relaciones admiten la paginación. Por ejemplo, las consultas a [directoryRoles](/graph/api/resources/directoryrole?view=graph-rest-1.0) no admiten la paginación. Esto incluye los objetos de rol de lectura así como los miembros de rol.</span><span class="sxs-lookup"><span data-stu-id="7e811-p105">Not all resources or relationships support paging. For example, queries against [directoryRoles](/graph/api/resources/directoryrole?view=graph-rest-1.0) do not support paging. This includes reading role objects themselves as well as role members.</span></span>
