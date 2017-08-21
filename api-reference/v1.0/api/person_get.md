# <a name="get-person"></a>Get person

Recupere las propiedades y las relaciones del objeto [person](../resources/person.md).

Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [obtener información relevante sobre los contactos](../../../concepts/people_example.md).

## <a name="prerequisites"></a>Requisitos previos
Los siguientes **permisos** son necesarios para ejecutar partes de esta API: *People.Read*; *People.Read.All*
 
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->

```http
GET /me/people/?$search='{property_value}'
GET /me/people/?$filter={person_property} eq '{property_value}'
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
|Nombre|Valor|Descripción|
|:---------------|:--------|:-------|
|$filter|string|Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.|
|$orderby|string|De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta. Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.|
|$search|string|Se buscan contactos por nombre o alias. Admite coincidencia aproximada.|
|$select|string|Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.|
|$skip|int|Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.|
|$top|int|Número de resultados que se van a devolver.|

## <a name="parameters"></a>Parámetros
| Parámetro |Tipo       |Descripción|
|:----------|:----------|:----------|
|property_value|Cadena     |El valor de la propiedad extendida que debe coincidir. Es necesario cuando aparece en la sección de la **solicitud HTTP**.|
|person_property|String    |La propiedad person que debe coincidir. Es necesario cuando aparece en la sección de la **solicitud HTTP**.|

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [person](../resources/person.md) en el cuerpo de la respuesta. La respuesta puede contener una instancia person o una colección de instancias person. 
## <a name="examples"></a>Ejemplos
### <a name="perform-a-search"></a>Realizar una búsqueda 
La siguiente solicitud realiza una búsqueda de un contacto llamado Irene McGowan. 

<!-- {
  "blockType": "request",
  "name": "get_person"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="Irene McGowan"
```

En el ejemplo siguiente se muestra la respuesta. 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.person"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
       {
           "id": "C0BD1BA1-A84E-4796-9C65-F8A0293741D1",
           "displayName": "Irene McGowan",
           "givenName": "Irene",
           "surname": "McGowan",
           "birthday": "",
           "personNotes": "",
           "isFavorite": false,
           "jobTitle": "Auditor",
           "companyName": null,
           "yomiCompany": "",
           "department": "Finance",
           "officeLocation": "12/1110",
           "profession": "",
           "userPrincipalName": "irenem@contoso.onmicrosoft.com",
           "imAddress": "sip:irenem@contoso.onmicrosoft.com",
           "scoredEmailAddresses": [
               {
                   "address": "irenem@contoso.onmicrosoft.com",
                   "relevanceScore": -16.446060612802224
               }
           ],
           "phones": [
               {
                   "type": "Business",
                   "number": "+1 412 555 0109"
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
### <a name="select-the-fields-to-return-in-a-filtered-response"></a>Seleccionar los campos que se van a devolver en una respuesta filtrada 
Puede combinar los parámetros *$select* y *$filter* para crear una lista personalizada de contactos relevantes para el usuario y obtener solo los campos que la aplicación necesita. 

En el ejemplo siguiente se obtiene el **displayName** y el **scoredEmailAddresses** de los contactos cuyo nombre para mostrar es igual al nombre especificado. En este ejemplo, solo se devuelven los contactos cuyo nombre para mostrar es igual a "Lorrie Frye". 

<!-- {
  "blockType": "request",
  "name": "get_person"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people/?$select=displayName,scoredEmailAddresses&$filter=displayName eq 'Lorrie Frye'
```

En el ejemplo siguiente se muestra la respuesta. 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.person"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "8CE6E1DE-CB84-4BF5-971D-D3ECF452E2B5",
            "displayName": "Lorrie Frye",
            "scoredEmailAddresses": [
                {
                    "address": "Lorrief@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ]
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get person",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
