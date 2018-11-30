---
title: Enumerar contactos
description: Recuperar una lista de objetos person ordenados por su relevancia para el usuario, que está determinado por relaciones comerciales y patrones de colaboración y comunicación del usuario.
ms.openlocfilehash: fc39f983251f668b4e1aa43ccb8be9cee5d23791
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085412"
---
# <a name="list-people"></a>Enumerar contactos

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recuperar una lista de objetos [person](../resources/person.md) ordenados por su relevancia para el [usuario](../resources/user.md), que está determinada por relaciones comerciales y patrones de colaboración y comunicación del usuario.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | People.Read    |
|Delegado (cuenta personal de Microsoft) | People.Read    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /me/people
GET /users/{id | userPrincipalName}/people
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los siguientes parámetros de consulta de OData para ayudar a personalizar la respuesta.

|Nombre|Valor|Descripción|
|:---------------|:--------|:-------|
|$filter|string|Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.|
|$orderby|cadena|De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta. Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.|
|$search|string|Busca contactos por nombre o alias. Admite la coincidencia aproximada. Parámetro sólo funciona para la búsqueda de personas relevantes del usuario que ha iniciado sesión, no para buscar personas relevantes para otros usuarios. También es compatible con la `topic` palabra clave para buscar personas en función de los temas que se extraen de las conversaciones de correo electrónico con esa persona. Consulte la sección de *realizar una búsqueda parcial* al [obtener la información relevante acerca de personas](/graph/people-example#perform-a-fuzzy-search) para obtener información y ejemplos.|
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

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de la [persona](../resources/person.md) en el cuerpo de la respuesta.

## <a name="examples"></a>Ejemplos

### <a name="browse"></a>Examinar

Las solicitudes de esta sección obtener las personas más relevantes para el usuario ha iniciado sesión (`/me`), en función de comunicación, la colaboración y las relaciones de negocios.

De forma predeterminada, cada respuesta devuelve 10 registros, pero usted puedecambiar esto utilizando el *parámetro* $top. Estas solicitudes requieren el permiso People.Read.

#### <a name="request"></a>Solicitud

El siguiente es un ejemplo de la solicitud de forma predeterminada.
<!-- {
  "blockType": "request",
  "name": "get_person_collection_beta"
}-->

```http
GET https://graph.microsoft.com/beta/me/people
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

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

#### <a name="requesting-a-subsequent-page-of-people"></a>Solicitando una página posterior de personas

Si la primera respuesta no contiene la lista completa de contactos relevantes, puede realizar una segunda solicitud mediante *$top* y *$skip* para solicitar páginas adicionales de información. Si la anterior solicitud tiene información adicional, la siguiente solicitud obtiene la siguiente página de contactos del servidor.

```http
GET https://graph.microsoft.com/beta/me/people/?$top=10&$skip=10
```

#### <a name="sort-the-response"></a>Ordenar la respuesta

De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta. Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*. Esta consulta selecciona a las personas más relevantes para usted, las ordena por su nombre para mostrar, y luego devuelve las 10 primeras personas de la lista ordenada.

```http
GET https://graph.microsoft.com/beta/me/people/?$orderby=DisplayName
```

#### <a name="changing-the-number-of-people-returned-and-the-fields-returned"></a>Cambiar el número de personas devueltas y los campos devueltos

Puede cambiar el número de contactos devueltos en la respuesta estableciendo el parámetro *$top*.

En el ejemplo siguiente se solicita el 1.000 personas más relevantes para `/me`. La solicitud también limita la cantidad de datos enviados desde el servidor al solicitar sólo el nombre para mostrar de la persona.

```http
GET https://graph.microsoft.com/beta/me/people/?$top=1000&$select=DisplayName
```

#### <a name="selecting-the-fields-to-return"></a>Seleccionando los campos a devolver

Puede limitar la cantidad de datos devueltos desde el servidor mediante el parámetro *$select* para elegir uno o más campos. El campo *@odata.id*siempre se devuelve.

El ejemplo siguiente limita la respuesta a la *DisplayName* y *EmailAddress* de las 10 personas más relevantes.

```http
GET https://graph.microsoft.com/beta/me/people/?$select=DisplayName,EmailAddresses
```

#### <a name="using-a-filter-to-limit-the-response"></a>Usando un filtro para limitar la respuesta

Puede usar el parámetro *$filter* para limitar la respuesta a solo los contactos cuyo registro contiene los criterios especificados.

La siguiente consulta limita la respuesta a las personas con el origen de "Directorio".

```http
GET https://graph.microsoft.com/beta/me/people/?$filter=Sources/Any (source: source/Type  eq 'Directory')
```

#### <a name="selecting-the-fields-to-return-in-a-filtered-response"></a>Selección de los campos para devolver una respuesta filtrada

Puede combinar los parámetros *$select* y *$filter* para crear una lista personalizada de contactos relevantes para el usuario y obtener solo los campos que la aplicación necesita.

En el ejemplo siguiente se obtiene el *DisplayName* y *EmailAddress* de personas cuyo nombre para mostrar es el nombre especificado. En este ejemplo, solo se devuelven las personas cuyo nombre para mostrar es igual a "Nestor Kellum".

```http
+GET https://graph.microsoft.com/beta/me/people/?$select=DisplayName,EmailAddresses&$filter=DisplayName eq 'Nestor Kellum'
```

### <a name="search-people"></a>Buscar contactos

Las solicitudes de esta sección también obtener las personas más relevantes para el usuario ha iniciado sesión (`/me`). Las solicitudes de búsqueda requieren el permiso People.Read.

#### <a name="using-search-to-select-people"></a>Uso de búsqueda para seleccionar personas

Use el parámetro *$search* para seleccionar contactos que reúnan un conjunto de criterios concreto.

La siguiente consulta de búsqueda devuelve relevantes para las personas `/me` cuyo GivenName o apellido comienza con la letra "j".

```http
GET https://graph.microsoft.com/beta/me/people/?$search=j
```

#### <a name="using-search-to-specify-a-relevant-topic"></a>Usar la búsqueda para especificar un tema relevante

La siguiente solicitud devuelve relevantes para las personas `/me` cuyo nombre contiene "ma" y que tienen una asociación con "Planear la característica".

```http
GET https://graph.microsoft.com/beta/me/people/?$search="ma topic: feature planning"
```

#### <a name="performing-a-fuzzy-search"></a>Realizando una búsqueda aproximada

La siguiente solicitud realiza una búsqueda de una persona denominada "Hermaini García". Debido a que hay una persona denominada "Herminia Hull" relevantes para el usuario ha iniciado sesión, se devuelve la información de "Casco Herminia".

```http
GET https://graph.microsoft.com/beta/me/people/?$search="hermaini hall"
```

### <a name="related-people"></a>Personas relacionadas

La siguiente solicitud obtiene las personas más relevantes a otra persona en la organización del usuario. Esta solicitud requiere la User.ReadBasic.All de permiso People.Read.All. En este ejemplo, se muestran las personas relevantes del Nestor Kellum.

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
