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
# <a name="list-people"></a>Enumerar contactos

Recupera una colección de objetos [person](../resources/person.md) ordenados por su relevancia para el [user](../resources/user.md), que viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.

Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [Obtener información relevante sobre los contactos](/graph/people-example).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | People.Read, People.Read.All    |
|Delegado (cuenta personal de Microsoft) | People.Read    |
|Aplicación | People.Read.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /me/people
GET /users/{id | userPrincipalName}/people
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta de OData](/graph/query-parameters) para que le resulte más fácil personalizar la respuesta, como se muestra en los ejemplos del artículo [Obtener información relevante sobre contactos](/graph/people-example).

|Nombre|Valor|Descripción|
|:---------------|:--------|:-------|
|$filter|string|Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.|
|$orderby|cadena|De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta. Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.|
|$search|string|Busca contactos por nombre o alias. Admite la coincidencia aproximada. Parámetro sólo funciona para la búsqueda de personas relevantes del usuario que ha iniciado sesión, no para buscar personas relevantes para otros usuarios. También es compatible con la `topic` palabra clave para buscar personas en función de los temas que se extraen de las conversaciones de correo electrónico con esa persona. Consulte la sección de *realizar una búsqueda parcial* al [obtener la información relevante acerca de personas](/graph/people-example#perform-a-fuzzy-search) para obtener información y ejemplos. |
|$select|string|Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.|
|$skip|int|Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.|
|$top|int|Número de resultados que se van a devolver.|

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Aceptar | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [person](../resources/person.md) en el cuerpo de la respuesta. La respuesta puede contener un objeto person o una colección de objetos person.

## <a name="examples"></a>Ejemplos

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "get_person_collection"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

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

Para obtener ejemplos, vea el artículo [Obtener información relevante sobre los contactos](/graph/people-example).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List people",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
