---
title: Enumerar contactos
description: Recupera una colección de objetos person ordenados por su relevancia para el user, que viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.
author: simonhult
localization_priority: Priority
ms.openlocfilehash: c1152990e23a931f246c5319e795ef7568aadd76
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881602"
---
# <a name="list-people"></a><span data-ttu-id="5e9f4-103">Enumerar contactos</span><span class="sxs-lookup"><span data-stu-id="5e9f4-103">List people</span></span>

<span data-ttu-id="5e9f4-104">Recupera una colección de objetos [person](../resources/person.md) ordenados por su relevancia para el [user](../resources/user.md), que viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-104">Retrieve a collection of [person](../resources/person.md) objects ordered by their relevance to the [user](../resources/user.md), which is determined by the user's communication and collaboration patterns, and business relationships.</span></span>

<span data-ttu-id="5e9f4-p101">Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [Obtener información relevante sobre los contactos](/graph/people-example).</span><span class="sxs-lookup"><span data-stu-id="5e9f4-p101">You can get this information via the People API. For examples, see the [Examples](#examples) section and the article [Get relevant information about people](/graph/people-example).</span></span>

## <a name="permissions"></a><span data-ttu-id="5e9f4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5e9f4-107">Permissions</span></span>

<span data-ttu-id="5e9f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5e9f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5e9f4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e9f4-110">Permission type</span></span>      | <span data-ttu-id="5e9f4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e9f4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5e9f4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e9f4-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5e9f4-113">People.Read, People.Read.All</span><span class="sxs-lookup"><span data-stu-id="5e9f4-113">People.Read, People.Read.All</span></span>    |
|<span data-ttu-id="5e9f4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e9f4-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5e9f4-115">People.Read</span><span class="sxs-lookup"><span data-stu-id="5e9f4-115">People.Read</span></span>    |
|<span data-ttu-id="5e9f4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e9f4-116">Application</span></span> | <span data-ttu-id="5e9f4-117">People.Read.All</span><span class="sxs-lookup"><span data-stu-id="5e9f4-117">People.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5e9f4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e9f4-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/people
GET /users/{id | userPrincipalName}/people
```

## <a name="optional-query-parameters"></a><span data-ttu-id="5e9f4-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5e9f4-119">Optional query parameters</span></span>

<span data-ttu-id="5e9f4-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) para que le resulte más fácil personalizar la respuesta, como se muestra en los ejemplos del artículo [Obtener información relevante sobre contactos](/graph/people-example).</span><span class="sxs-lookup"><span data-stu-id="5e9f4-120">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response, as shown in the examples in the article [Get relevant information about people](/graph/people-example).</span></span>

|<span data-ttu-id="5e9f4-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e9f4-121">Name</span></span>|<span data-ttu-id="5e9f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5e9f4-122">Value</span></span>|<span data-ttu-id="5e9f4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e9f4-123">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="5e9f4-124">$filter</span><span class="sxs-lookup"><span data-stu-id="5e9f4-124">$filter</span></span>|<span data-ttu-id="5e9f4-125">string</span><span class="sxs-lookup"><span data-stu-id="5e9f4-125">string</span></span>|<span data-ttu-id="5e9f4-126">Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-126">Limits the response to only those people whose record contains the specified criteria.</span></span>|
|<span data-ttu-id="5e9f4-127">$orderby</span><span class="sxs-lookup"><span data-stu-id="5e9f4-127">$orderby</span></span>|<span data-ttu-id="5e9f4-128">cadena</span><span class="sxs-lookup"><span data-stu-id="5e9f4-128">string</span></span>|<span data-ttu-id="5e9f4-129">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-129">By default the people in the response are sorted by their relevance to your query.</span></span> <span data-ttu-id="5e9f4-130">Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-130">You can change the order of the people in the response using the *$orderby* parameter.</span></span>|
|<span data-ttu-id="5e9f4-131">$search</span><span class="sxs-lookup"><span data-stu-id="5e9f4-131">$search</span></span>|<span data-ttu-id="5e9f4-132">string</span><span class="sxs-lookup"><span data-stu-id="5e9f4-132">string</span></span>|<span data-ttu-id="5e9f4-133">Busca contactos por nombre o alias.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-133">Search for people by name or alias.</span></span> <span data-ttu-id="5e9f4-134">Admite la coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-134">Supports Fuzzy matching.</span></span> <span data-ttu-id="5e9f4-135">Parámetro sólo funciona para la búsqueda de personas relevantes del usuario que ha iniciado sesión, no para buscar personas relevantes para otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-135">Parameter only works for searching the signed-in user's relevant people, not for searching people relevant to other users.</span></span> <span data-ttu-id="5e9f4-136">También es compatible con la `topic` palabra clave para buscar personas en función de los temas que se extraen de las conversaciones de correo electrónico con esa persona.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-136">Also supports the `topic` keyword to find people based on topics extracted from e-mail conversations with that person.</span></span> <span data-ttu-id="5e9f4-137">Consulte la sección de *realizar una búsqueda parcial* al [obtener la información relevante acerca de personas](/graph/people-example#perform-a-fuzzy-search) para obtener información y ejemplos.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-137">See the *Perform a fuzzy search* section at [Get relevant information about people](/graph/people-example#perform-a-fuzzy-search) for information and examples.</span></span> |
|<span data-ttu-id="5e9f4-138">$select</span><span class="sxs-lookup"><span data-stu-id="5e9f4-138">$select</span></span>|<span data-ttu-id="5e9f4-139">string</span><span class="sxs-lookup"><span data-stu-id="5e9f4-139">string</span></span>|<span data-ttu-id="5e9f4-p105">Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-p105">Comma-separated list of properties to include in the response. For optimal performance, only select the subset of properties needed.</span></span>|
|<span data-ttu-id="5e9f4-142">$skip</span><span class="sxs-lookup"><span data-stu-id="5e9f4-142">$skip</span></span>|<span data-ttu-id="5e9f4-143">int</span><span class="sxs-lookup"><span data-stu-id="5e9f4-143">int</span></span>|<span data-ttu-id="5e9f4-p106">Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-p106">Skip the first n results, useful for paging. This is not supported when using *$search*.</span></span>|
|<span data-ttu-id="5e9f4-146">$top</span><span class="sxs-lookup"><span data-stu-id="5e9f4-146">$top</span></span>|<span data-ttu-id="5e9f4-147">int</span><span class="sxs-lookup"><span data-stu-id="5e9f4-147">int</span></span>|<span data-ttu-id="5e9f4-148">Número de resultados que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-148">Number of results to be returned.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="5e9f4-149">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e9f4-149">Request headers</span></span>

| <span data-ttu-id="5e9f4-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e9f4-150">Name</span></span>      |<span data-ttu-id="5e9f4-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e9f4-151">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="5e9f4-152">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e9f4-152">Authorization</span></span>  | <span data-ttu-id="5e9f4-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5e9f4-155">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5e9f4-155">Accept</span></span> | <span data-ttu-id="5e9f4-156">application/json</span><span class="sxs-lookup"><span data-stu-id="5e9f4-156">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="5e9f4-157">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e9f4-157">Request body</span></span>

<span data-ttu-id="5e9f4-158">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-158">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5e9f4-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e9f4-159">Response</span></span>

<span data-ttu-id="5e9f4-p108">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [person](../resources/person.md) en el cuerpo de la respuesta. La respuesta puede contener un objeto person o una colección de objetos person.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-p108">If successful, this method returns a `200 OK` response code and a collection of [person](../resources/person.md) objects in the response body. The response can contain one person object or a collection of person objects.</span></span>

## <a name="examples"></a><span data-ttu-id="5e9f4-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5e9f4-162">Examples</span></span>

#### <a name="request"></a><span data-ttu-id="5e9f4-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e9f4-163">Request</span></span>

<span data-ttu-id="5e9f4-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-164">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_person_collection"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people
```

#### <a name="response"></a><span data-ttu-id="5e9f4-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e9f4-165">Response</span></span>

<span data-ttu-id="5e9f4-166">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e9f4-166">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "name": "get_person_collection",
  "truncated": true,
  "@odata.type": "microsoft.graph.person",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1370

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
            "jobTitle": null,
            "companyName": null,
            "yomiCompany": "",
            "department": null,
            "officeLocation": null,
            "profession": "",
            "userPrincipalName": "",
            "imAddress": null,
            "scoredEmailAddresses": [
                {
                    "address": "Marketing@contoso.com",
                    "relevanceScore": 30.0
                }
            ],
            "phones": [],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Group",
                "subclass": "UnifiedGroup"
            }
        },
        {
            "id": "e3d0513b-449e-4198-ba6f-bd97ae7cae85",
            "displayName": "Isaiah Langer",
            "givenName": "Isaiah",
            "surname": "Langer",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Web Marketing Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/1101",
            "profession": "",
            "userPrincipalName": "IsaiahL@contoso.com",
            "imAddress": "sip:isaiahl@contoso.com",
            "scoredEmailAddresses": [
                {
                    "address": "IsaiahL@contoso.com",
                    "relevanceScore": 20.0
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
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        }
    ]
}
```

<span data-ttu-id="5e9f4-167">Para obtener ejemplos, vea el artículo [Obtener información relevante sobre los contactos](/graph/people-example).</span><span class="sxs-lookup"><span data-stu-id="5e9f4-167">For more examples, see the article [Get relevant information about people](/graph/people-example).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List people",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
