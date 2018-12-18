---
title: Enumerar contactos
description: Recuperar una lista de objetos person ordenados por su relevancia para el usuario, que está determinado por relaciones comerciales y patrones de colaboración y comunicación del usuario.
author: simonhult
ms.openlocfilehash: 64d24111f295fd076024a889d050c8c48c104295
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347659"
---
# <a name="list-people"></a><span data-ttu-id="c9a74-103">Enumerar contactos</span><span class="sxs-lookup"><span data-stu-id="c9a74-103">List people</span></span>

> <span data-ttu-id="c9a74-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c9a74-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c9a74-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c9a74-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c9a74-106">Recuperar una lista de objetos [person](../resources/person.md) ordenados por su relevancia para el [usuario](../resources/user.md), que está determinada por relaciones comerciales y patrones de colaboración y comunicación del usuario.</span><span class="sxs-lookup"><span data-stu-id="c9a74-106">Retrieve a list of [person](../resources/person.md) objects ordered by their relevance to the [user](../resources/user.md), which is determined by the user's communication and collaboration patterns, and business relationships.</span></span>

## <a name="permissions"></a><span data-ttu-id="c9a74-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c9a74-107">Permissions</span></span>

<span data-ttu-id="c9a74-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c9a74-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c9a74-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c9a74-110">Permission type</span></span>      | <span data-ttu-id="c9a74-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c9a74-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c9a74-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c9a74-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c9a74-113">People.Read</span><span class="sxs-lookup"><span data-stu-id="c9a74-113">People.Read</span></span>    |
|<span data-ttu-id="c9a74-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c9a74-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c9a74-115">People.Read</span><span class="sxs-lookup"><span data-stu-id="c9a74-115">People.Read</span></span>    |
|<span data-ttu-id="c9a74-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c9a74-116">Application</span></span> | <span data-ttu-id="c9a74-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c9a74-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c9a74-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c9a74-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/people
GET /users/{id | userPrincipalName}/people
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c9a74-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c9a74-119">Optional query parameters</span></span>

<span data-ttu-id="c9a74-120">Este método admite los siguientes parámetros de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9a74-120">This method supports the following OData query parameters to help customize the response.</span></span>

|<span data-ttu-id="c9a74-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9a74-121">Name</span></span>|<span data-ttu-id="c9a74-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c9a74-122">Value</span></span>|<span data-ttu-id="c9a74-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9a74-123">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="c9a74-124">$filter</span><span class="sxs-lookup"><span data-stu-id="c9a74-124">$filter</span></span>|<span data-ttu-id="c9a74-125">string</span><span class="sxs-lookup"><span data-stu-id="c9a74-125">string</span></span>|<span data-ttu-id="c9a74-126">Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="c9a74-126">Limits the response to only those people whose record contains the specified criteria.</span></span>|
|<span data-ttu-id="c9a74-127">$orderby</span><span class="sxs-lookup"><span data-stu-id="c9a74-127">$orderby</span></span>|<span data-ttu-id="c9a74-128">cadena</span><span class="sxs-lookup"><span data-stu-id="c9a74-128">string</span></span>|<span data-ttu-id="c9a74-129">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta.</span><span class="sxs-lookup"><span data-stu-id="c9a74-129">By default the people in the response are sorted by their relevance to your query.</span></span> <span data-ttu-id="c9a74-130">Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="c9a74-130">You can change the order of the people in the response using the *$orderby* parameter.</span></span>|
|<span data-ttu-id="c9a74-131">$search</span><span class="sxs-lookup"><span data-stu-id="c9a74-131">$search</span></span>|<span data-ttu-id="c9a74-132">string</span><span class="sxs-lookup"><span data-stu-id="c9a74-132">string</span></span>|<span data-ttu-id="c9a74-133">Busca contactos por nombre o alias.</span><span class="sxs-lookup"><span data-stu-id="c9a74-133">Search for people by name or alias.</span></span> <span data-ttu-id="c9a74-134">Admite la coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="c9a74-134">Supports Fuzzy matching.</span></span> <span data-ttu-id="c9a74-135">Parámetro sólo funciona para la búsqueda de personas relevantes del usuario que ha iniciado sesión, no para buscar personas relevantes para otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="c9a74-135">Parameter only works for searching the signed-in user's relevant people, not for searching people relevant to other users.</span></span> <span data-ttu-id="c9a74-136">También es compatible con la `topic` palabra clave para buscar personas en función de los temas que se extraen de las conversaciones de correo electrónico con esa persona.</span><span class="sxs-lookup"><span data-stu-id="c9a74-136">Also supports the `topic` keyword to find people based on topics extracted from e-mail conversations with that person.</span></span> <span data-ttu-id="c9a74-137">Consulte la sección de *realizar una búsqueda parcial* al [obtener la información relevante acerca de personas](/graph/people-example#perform-a-fuzzy-search) para obtener información y ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c9a74-137">See the *Perform a fuzzy search* section at [Get relevant information about people](/graph/people-example#perform-a-fuzzy-search) for information and examples.</span></span>|
|<span data-ttu-id="c9a74-138">$select</span><span class="sxs-lookup"><span data-stu-id="c9a74-138">$select</span></span>|<span data-ttu-id="c9a74-139">string</span><span class="sxs-lookup"><span data-stu-id="c9a74-139">string</span></span>|<span data-ttu-id="c9a74-p105">Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.</span><span class="sxs-lookup"><span data-stu-id="c9a74-p105">Comma-separated list of properties to include in the response. For optimal performance, only select the subset of properties needed.</span></span>|
|<span data-ttu-id="c9a74-142">$skip</span><span class="sxs-lookup"><span data-stu-id="c9a74-142">$skip</span></span>|<span data-ttu-id="c9a74-143">int</span><span class="sxs-lookup"><span data-stu-id="c9a74-143">int</span></span>|<span data-ttu-id="c9a74-p106">Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.</span><span class="sxs-lookup"><span data-stu-id="c9a74-p106">Skip the first n results, useful for paging. This is not supported when using *$search*.</span></span>|
|<span data-ttu-id="c9a74-146">$top</span><span class="sxs-lookup"><span data-stu-id="c9a74-146">$top</span></span>|<span data-ttu-id="c9a74-147">int</span><span class="sxs-lookup"><span data-stu-id="c9a74-147">int</span></span>|<span data-ttu-id="c9a74-148">Número de resultados que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="c9a74-148">Number of results to be returned.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="c9a74-149">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c9a74-149">Request headers</span></span>

| <span data-ttu-id="c9a74-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9a74-150">Name</span></span>      |<span data-ttu-id="c9a74-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9a74-151">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c9a74-152">Authorization</span><span class="sxs-lookup"><span data-stu-id="c9a74-152">Authorization</span></span>  | <span data-ttu-id="c9a74-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9a74-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c9a74-155">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c9a74-155">Accept</span></span> | <span data-ttu-id="c9a74-156">application/json</span><span class="sxs-lookup"><span data-stu-id="c9a74-156">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="c9a74-157">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c9a74-157">Request body</span></span>

<span data-ttu-id="c9a74-158">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c9a74-158">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c9a74-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9a74-159">Response</span></span>

<span data-ttu-id="c9a74-160">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de la [persona](../resources/person.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9a74-160">If successful, this method returns a `200 OK` response code and a collection of [person](../resources/person.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="c9a74-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c9a74-161">Examples</span></span>

### <a name="browse"></a><span data-ttu-id="c9a74-162">Examinar</span><span class="sxs-lookup"><span data-stu-id="c9a74-162">Browse</span></span>

<span data-ttu-id="c9a74-163">Las solicitudes de esta sección obtener las personas más relevantes para el usuario ha iniciado sesión (`/me`), en función de comunicación, la colaboración y las relaciones de negocios.</span><span class="sxs-lookup"><span data-stu-id="c9a74-163">The requests in this section get the people most relevant to the signed-in user (`/me`), based on communication, collaboration, and business relationships.</span></span>

<span data-ttu-id="c9a74-164">De forma predeterminada, cada respuesta devuelve 10 registros, pero usted puedecambiar esto utilizando el *parámetro* $top.</span><span class="sxs-lookup"><span data-stu-id="c9a74-164">By default, each response returns 10 records, but you can change this using the *$top* parameter.</span></span> <span data-ttu-id="c9a74-165">Estas solicitudes requieren el permiso People.Read.</span><span class="sxs-lookup"><span data-stu-id="c9a74-165">These requests require the People.Read permission.</span></span>

#### <a name="request"></a><span data-ttu-id="c9a74-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c9a74-166">Request</span></span>

<span data-ttu-id="c9a74-167">El siguiente es un ejemplo de la solicitud de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c9a74-167">The following is an example of the default request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_person_collection_beta"
}-->

```http
GET https://graph.microsoft.com/beta/me/people
```

#### <a name="response"></a><span data-ttu-id="c9a74-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9a74-168">Response</span></span>

<span data-ttu-id="c9a74-169">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9a74-169">The following is an example of the response.</span></span>
><span data-ttu-id="c9a74-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c9a74-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "name": "get_person_collection_beta",
  "truncated": true,
  "@odata.type": "microsoft.graph.person",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1326

{
    "value": [
        {
            "id": "33b43a5b-87d6-41ec-91f8-a2610048105f",
            "displayName": "Marketing",
            "givenName": null,
            "surname": null,
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "title": null,
            "companyName": null,
            "yomiCompany": "",
            "department": null,
            "officeLocation": null,
            "profession": "",
            "mailboxType": "GroupMailbox",
            "personType": "ModernGroup",
            "userPrincipalName": "",
            "emailAddresses": [
                {
                    "address": "Marketing@contoso.com",
                    "rank": 30
                }
            ],
            "phones": [],
            "postalAddresses": [],
            "websites": [],
            "sources": [
                {
                    "type": "Directory"
                }
            ]
        },
        {
            "id": "e3d0513b-449e-4198-ba6f-bd97ae7cae85",
            "displayName": "Isaiah Langer",
            "givenName": "Isaiah",
            "surname": "Langer",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "title": "Web Marketing Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/1101",
            "profession": "",
            "mailboxType": "Mailbox",
            "personType": "Person",
            "userPrincipalName": "IsaiahL@contoso.com",
            "emailAddresses": [
                {
                    "address": "IsaiahL@contoso.com",
                    "rank": 20
                }
            ],
            "phones": [
                {
                    "type": "business",
                    "number": "+1 918 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "sources": [
                {
                    "type": "Directory"
                }
            ]
        }
    ]
}
```

#### <a name="requesting-a-subsequent-page-of-people"></a><span data-ttu-id="c9a74-172">Solicitando una página posterior de personas</span><span class="sxs-lookup"><span data-stu-id="c9a74-172">Requesting a subsequent page of people</span></span>

<span data-ttu-id="c9a74-p110">Si la primera respuesta no contiene la lista completa de contactos relevantes, puede realizar una segunda solicitud mediante *$top* y *$skip* para solicitar páginas adicionales de información. Si la anterior solicitud tiene información adicional, la siguiente solicitud obtiene la siguiente página de contactos del servidor.</span><span class="sxs-lookup"><span data-stu-id="c9a74-p110">If the first response does not contain the complete list of relevant people, you can make a second request using *$top* and *$skip* to request additional pages of information. If the previous request has additional information, the following request gets the next page of people from the server.</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$top=10&$skip=10
```

#### <a name="sort-the-response"></a><span data-ttu-id="c9a74-175">Ordenar la respuesta</span><span class="sxs-lookup"><span data-stu-id="c9a74-175">Sort the response</span></span>

<span data-ttu-id="c9a74-176">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta.</span><span class="sxs-lookup"><span data-stu-id="c9a74-176">By default the people in the response are sorted by their relevance to your query.</span></span> <span data-ttu-id="c9a74-177">Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="c9a74-177">You can change the order of the people in the response using the *$orderby* parameter.</span></span> <span data-ttu-id="c9a74-178">Esta consulta selecciona a las personas más relevantes para usted, las ordena por su nombre para mostrar, y luego devuelve las 10 primeras personas de la lista ordenada.</span><span class="sxs-lookup"><span data-stu-id="c9a74-178">This query selects the people most relevant to you, sorts them by their display name, and then returns the first 10 people on the sorted list.</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$orderby=DisplayName
```

#### <a name="changing-the-number-of-people-returned-and-the-fields-returned"></a><span data-ttu-id="c9a74-179">Cambiar el número de personas devueltas y los campos devueltos</span><span class="sxs-lookup"><span data-stu-id="c9a74-179">Changing the number of people returned and the fields returned</span></span>

<span data-ttu-id="c9a74-180">Puede cambiar el número de contactos devueltos en la respuesta estableciendo el parámetro *$top*.</span><span class="sxs-lookup"><span data-stu-id="c9a74-180">You can change the number of people returned in the response by setting the *$top* parameter.</span></span>

<span data-ttu-id="c9a74-181">En el ejemplo siguiente se solicita el 1.000 personas más relevantes para `/me`.</span><span class="sxs-lookup"><span data-stu-id="c9a74-181">The following example requests the 1,000 people most relevant to `/me`.</span></span> <span data-ttu-id="c9a74-182">La solicitud también limita la cantidad de datos enviados desde el servidor al solicitar sólo el nombre para mostrar de la persona.</span><span class="sxs-lookup"><span data-stu-id="c9a74-182">The request also limits the amount of data sent back from the server by requesting only the display name of the person.</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$top=1000&$select=DisplayName
```

#### <a name="selecting-the-fields-to-return"></a><span data-ttu-id="c9a74-183">Seleccionando los campos a devolver</span><span class="sxs-lookup"><span data-stu-id="c9a74-183">Selecting the fields to return</span></span>

<span data-ttu-id="c9a74-184">Puede limitar la cantidad de datos devueltos desde el servidor mediante el parámetro *$select* para elegir uno o más campos.</span><span class="sxs-lookup"><span data-stu-id="c9a74-184">You can limit the amount of data returned from the server by using the *$select* parameter to choose one or more fields.</span></span> <span data-ttu-id="c9a74-185">El campo *@odata.id*siempre se devuelve.</span><span class="sxs-lookup"><span data-stu-id="c9a74-185">The *@odata.id* field is always returned.</span></span>

<span data-ttu-id="c9a74-186">El ejemplo siguiente limita la respuesta a la *DisplayName* y *EmailAddress* de las 10 personas más relevantes.</span><span class="sxs-lookup"><span data-stu-id="c9a74-186">The following example limits the response to the *DisplayName* and *EmailAddress* of the 10 most relevant people.</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$select=DisplayName,EmailAddresses
```

#### <a name="using-a-filter-to-limit-the-response"></a><span data-ttu-id="c9a74-187">Usando un filtro para limitar la respuesta</span><span class="sxs-lookup"><span data-stu-id="c9a74-187">Using a filter to limit the response</span></span>

<span data-ttu-id="c9a74-188">Puede usar el parámetro *$filter* para limitar la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="c9a74-188">You can use the *$filter* parameter to limit the response to only those people whose record contains the specified criteria.</span></span>

<span data-ttu-id="c9a74-189">La siguiente consulta limita la respuesta a las personas con el origen de "Directorio".</span><span class="sxs-lookup"><span data-stu-id="c9a74-189">The following query limits the response to people with the source "Directory."</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$filter=Sources/Any (source: source/Type  eq 'Directory')
```

#### <a name="selecting-the-fields-to-return-in-a-filtered-response"></a><span data-ttu-id="c9a74-190">Selección de los campos para devolver una respuesta filtrada</span><span class="sxs-lookup"><span data-stu-id="c9a74-190">Selecting the fields to return in a filtered response</span></span>

<span data-ttu-id="c9a74-191">Puede combinar los parámetros *$select* y *$filter* para crear una lista personalizada de contactos relevantes para el usuario y obtener solo los campos que la aplicación necesita.</span><span class="sxs-lookup"><span data-stu-id="c9a74-191">You can combine the *$select* and *$filter* parameters to create a custom list of people relevant to the user and get only the fields that your application needs.</span></span>

<span data-ttu-id="c9a74-192">En el ejemplo siguiente se obtiene el *DisplayName* y *EmailAddress* de personas cuyo nombre para mostrar es el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="c9a74-192">The following example gets the *DisplayName* and *EmailAddress* of people whose display name equals the specified name.</span></span> <span data-ttu-id="c9a74-193">En este ejemplo, solo se devuelven las personas cuyo nombre para mostrar es igual a "Nestor Kellum".</span><span class="sxs-lookup"><span data-stu-id="c9a74-193">In this example, only people whose display name equals "Nestor Kellum" are returned.</span></span>

```http
+GET https://graph.microsoft.com/beta/me/people/?$select=DisplayName,EmailAddresses&$filter=DisplayName eq 'Nestor Kellum'
```

### <a name="search-people"></a><span data-ttu-id="c9a74-194">Buscar contactos</span><span class="sxs-lookup"><span data-stu-id="c9a74-194">Search people</span></span>

<span data-ttu-id="c9a74-195">Las solicitudes de esta sección también obtener las personas más relevantes para el usuario ha iniciado sesión (`/me`).</span><span class="sxs-lookup"><span data-stu-id="c9a74-195">The requests in this section also get the people most relevant to the signed-in user (`/me`).</span></span> <span data-ttu-id="c9a74-196">Las solicitudes de búsqueda requieren el permiso People.Read.</span><span class="sxs-lookup"><span data-stu-id="c9a74-196">Search requests require the People.Read permission.</span></span>

#### <a name="using-search-to-select-people"></a><span data-ttu-id="c9a74-197">Uso de búsqueda para seleccionar personas</span><span class="sxs-lookup"><span data-stu-id="c9a74-197">Using search to select people</span></span>

<span data-ttu-id="c9a74-198">Use el parámetro *$search* para seleccionar contactos que reúnan un conjunto de criterios concreto.</span><span class="sxs-lookup"><span data-stu-id="c9a74-198">Use the *$search* parameter to select people who meet a particular set of criteria.</span></span>

<span data-ttu-id="c9a74-199">La siguiente consulta de búsqueda devuelve relevantes para las personas `/me` cuyo GivenName o apellido comienza con la letra "j".</span><span class="sxs-lookup"><span data-stu-id="c9a74-199">The following search query returns people relevant to `/me` whose GivenName or Surname begins with the letter "j".</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$search=j
```

#### <a name="using-search-to-specify-a-relevant-topic"></a><span data-ttu-id="c9a74-200">Usar la búsqueda para especificar un tema relevante</span><span class="sxs-lookup"><span data-stu-id="c9a74-200">Using search to specify a relevant topic</span></span>

<span data-ttu-id="c9a74-201">La siguiente solicitud devuelve relevantes para las personas `/me` cuyo nombre contiene "ma" y que tienen una asociación con "Planear la característica".</span><span class="sxs-lookup"><span data-stu-id="c9a74-201">The following request returns people relevant to `/me` whose name contains "ma" and who have an association with "feature planning."</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$search="ma topic: feature planning"
```

#### <a name="performing-a-fuzzy-search"></a><span data-ttu-id="c9a74-202">Realizando una búsqueda aproximada</span><span class="sxs-lookup"><span data-stu-id="c9a74-202">Performing a fuzzy search</span></span>

<span data-ttu-id="c9a74-203">La siguiente solicitud realiza una búsqueda de una persona denominada "Hermaini García".</span><span class="sxs-lookup"><span data-stu-id="c9a74-203">The following request does a search for a person named "Hermaini Hall."</span></span> <span data-ttu-id="c9a74-204">Debido a que hay una persona denominada "Herminia Hull" relevantes para el usuario ha iniciado sesión, se devuelve la información de "Casco Herminia".</span><span class="sxs-lookup"><span data-stu-id="c9a74-204">Because there is a person named "Herminia Hull" relevant to the signed-in user, the information for "Herminia Hull" is returned.</span></span>

```http
GET https://graph.microsoft.com/beta/me/people/?$search="hermaini hall"
```

### <a name="related-people"></a><span data-ttu-id="c9a74-205">Personas relacionadas</span><span class="sxs-lookup"><span data-stu-id="c9a74-205">Related people</span></span>

<span data-ttu-id="c9a74-206">La siguiente solicitud obtiene las personas más relevantes a otra persona en la organización del usuario.</span><span class="sxs-lookup"><span data-stu-id="c9a74-206">The following request gets the people most relevant to another person in the user's organization.</span></span> <span data-ttu-id="c9a74-207">Esta solicitud requiere la User.ReadBasic.All de permiso People.Read.All.</span><span class="sxs-lookup"><span data-stu-id="c9a74-207">This request requires the User.ReadBasic.All for People.Read.All permission.</span></span> <span data-ttu-id="c9a74-208">En este ejemplo, se muestran las personas relevantes del Nestor Kellum.</span><span class="sxs-lookup"><span data-stu-id="c9a74-208">In this example, Nestor Kellum's relevant people are displayed.</span></span>

```http
GET https://graph.microsoft.com/beta/users('nestork@contoso.com')/people/
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List people",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
