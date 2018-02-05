# <a name="use-the-people-api-in-microsoft-graph-to-get-information-about-the-people-most-relevant-to-you"></a><span data-ttu-id="5b849-101">Usar la API de contactos de Microsoft Graph para obtener información sobre los contactos más relevantes para usted</span><span class="sxs-lookup"><span data-stu-id="5b849-101">Use the People API in Microsoft Graph to get information about the people most relevant to you</span></span>
<span data-ttu-id="5b849-p101">Las aplicaciones de Microsoft Graph usar la API de contactos para recuperar los contactos más relevantes para un usuario. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. Los contactos pueden ser contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype). Además de generar esta información, la API de contactos ofrece también compatibilidad con la búsqueda de coincidencia aproximada y la posibilidad de recuperar la lista de usuarios relevantes para otro usuario de la organización del usuario que ha iniciado sesión. La API de contactos resulta especialmente útil en escenarios de selección de personas, como redactar un mensaje de correo o crear una reunión. Por ejemplo, puede usar la API de contactos en escenarios de redacción de mensajes de correo.</span><span class="sxs-lookup"><span data-stu-id="5b849-p101">Microsoft Graph applications can use the People API to retrieve the people who are most relevant to a user. Relevance is determined by the user’s communication and collaboration patterns and business relationships. People can be local contacts, contacts from social networking or from an organization’s directory, and people from recent communications (such as email and Skype). Along with generating this insight, the People API also provides fuzzy matching search support and the ability to retrieve the list of users relevant to another user in the signed-in user's organization. The People API is particularly useful for people picking scenarios, such as composing an email or creating a meeting. For example, you can use the People API in email compose scenarios.</span></span>
 
## <a name="authorization"></a><span data-ttu-id="5b849-108">Authorization</span><span class="sxs-lookup"><span data-stu-id="5b849-108">Authorization</span></span>
<span data-ttu-id="5b849-109">Para llamar a la API de contactos de Microsoft Graph, la aplicación necesitará los permisos adecuados:</span><span class="sxs-lookup"><span data-stu-id="5b849-109">To call the People API in Microsoft Graph, your app will need the appropriate permissions:</span></span> 

* <span data-ttu-id="5b849-p102">People.Read: se usa para realizar llamadas generales a la API de contactos; por ejemplo, https://graph.microsoft.com/v1.0/me/people/. People.Read requiere el consentimiento del usuario final.</span><span class="sxs-lookup"><span data-stu-id="5b849-p102">People.Read - Use to make general People API calls; for example, https://graph.microsoft.com/v1.0/me/people/. People.Read requires end user consent.</span></span>
* <span data-ttu-id="5b849-p103">People.Read.All: se requiere para recuperar los contactos más relevantes para llamadas de un usuario concreto de la organización del usuario que ha iniciado sesión (https://graph.microsoft.com/v1.0/users('{id}')/people). People.Read.All requiere el consentimiento del administrador.</span><span class="sxs-lookup"><span data-stu-id="5b849-p103">People.Read.All - Required to retrieve the people most relevant to a specified user in the signed-in user’s organization (https://graph.microsoft.com/v1.0/users('{id}')/people) calls. People.Read.All requires admin consent.</span></span>
## <a name="browse-people"></a><span data-ttu-id="5b849-114">Examinar personas</span><span class="sxs-lookup"><span data-stu-id="5b849-114">Browse people</span></span>
<span data-ttu-id="5b849-p104">Las solicitudes de esta sección obtienen los contactos más relevantes para el usuario que ha iniciado sesión (`/me`). Estas solicitudes requieren el permiso People.Read. De manera predeterminada, cada respuesta devuelve 10 registros, pero esto se puede cambiar mediante el parámetro de consulta *$top*.</span><span class="sxs-lookup"><span data-stu-id="5b849-p104">The requests in this section get the people most relevant to the signed-in user (`/me`). These requests require the People.Read permission. By default, each response returns 10 records, but you can change this by using the *$top* query parameter.</span></span> 
### <a name="get-a-collection-of-relevant-people"></a><span data-ttu-id="5b849-118">Obtener una colección de contactos relevantes</span><span class="sxs-lookup"><span data-stu-id="5b849-118">Get a collection of relevant people</span></span> 
<span data-ttu-id="5b849-119">La siguiente solicitud obtiene los contactos más relevantes para el usuario que ha iniciado sesión (`/me`), en función de las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="5b849-119">The following request gets the people most relevant to the signed-in user (`/me`), based on communication and collaboration patterns and business relationships.</span></span> 

```http
GET https://graph.microsoft.com/v1.0/me/people/
```

<span data-ttu-id="5b849-p105">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro de consulta *$top*. En este ejemplo se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="5b849-p105">The following example shows the response. By default, each response returns 10 records. You can change this by using the *$top* query parameter. This example uses *$top* to limit the response to three records.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "8CE6E1DE-CB84-4BF5-971D-D3ECF452E2B5",
            "displayName": "Lorrie Frye",
            "givenName": "Lorrie",
            "surname": "Frye",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Paralegal",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "20/1109",
            "profession": "",
            "userPrincipalName": "Lorrief@contoso.onmicrosoft.com",
            "imAddress": "sip:Lorrief@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Lorrief@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 980 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "5767393D-42BA-4E5C-BEE4-52BB25639CF4",
            "displayName": "Maynard Denman",
            "givenName": "Maynard",
            "surname": "Denman",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Web Marketing Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/1101",
            "profession": "",
            "userPrincipalName": "Maynardd@contoso.onmicrosoft.com",
            "imAddress": "sip:Maynardd@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Maynardd@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 918 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "914B5191-11FA-4C0B-A354-0FA8C8EFD585",
            "displayName": "Darrel Halsey",
            "givenName": "Darrel",
            "surname": "Halsey",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Attorney",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "14/1102",
            "profession": "",
            "userPrincipalName": "Darrelh@contoso.onmicrosoft.com",
            "imAddress": "sip:Darrelh@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Darrelh@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 205 555 0103"
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
### <a name="request-a-subsequent-page-of-people"></a><span data-ttu-id="5b849-124">Solicitar una página posterior de contactos</span><span class="sxs-lookup"><span data-stu-id="5b849-124">Request a subsequent page of people</span></span>
<span data-ttu-id="5b849-p106">Si la primera respuesta no contiene la lista completa de contactos relevantes, puede realizar una segunda solicitud mediante *$top* y *$skip* para solicitar páginas adicionales de información. Si la anterior solicitud tiene información adicional, la siguiente solicitud obtiene la siguiente página de contactos del servidor.</span><span class="sxs-lookup"><span data-stu-id="5b849-p106">If the first response does not contain the complete list of relevant people, you can make a second request using *$top* and *$skip* to request additional pages of information. If the previous request has additional information, the following request gets the next page of people from the server.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$top=3&$skip=10
```

<span data-ttu-id="5b849-p107">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro de consulta *$top*. En este ejemplo se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="5b849-p107">The following example shows the response. By default, each response returns 10 records. You can change this by using the *$top* query parameter. This example uses *$top* to limit the response to three records.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "1F28616D-BDFE-4080-8F06-03366A851688",
            "displayName": "Felix Coppola",
            "givenName": "Felix",
            "surname": "Coppola",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "CVP Legal",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "19/2109",
            "profession": "",
            "userPrincipalName": "Felixc@contoso.onmicrosoft.com",
            "imAddress": "sip:Felixc@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Felixc@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 309 555 0104"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "8A3FC021-6DBB-44AC-8884-B7B500CC260A",
            "displayName": "Lenora Rowland",
            "givenName": "Lenora",
            "surname": "Rowland",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Marketing Assistant",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "18/1106",
            "profession": "",
            "userPrincipalName": "Lenorar@contoso.onmicrosoft.com",
            "imAddress": "sip:Lenorar@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Lenorar@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 954 555 0118"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "032C9919-4DF9-4715-8C46-4D0FAE7B3EB2",
            "displayName": "Manuel Collette",
            "givenName": "Manuel",
            "surname": "Collette",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Accountant II",
            "companyName": null,
            "yomiCompany": "",
            "department": "Finance",
            "officeLocation": "98/2202",
            "profession": "",
            "userPrincipalName": "Manuelc@contoso.onmicrosoft.com",
            "imAddress": "sip:Manuelc@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Manuelc@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+20 255501070"
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
### <a name="sort-the-response"></a><span data-ttu-id="5b849-131">Ordenar la respuesta</span><span class="sxs-lookup"><span data-stu-id="5b849-131">Sort the response</span></span> 
<span data-ttu-id="5b849-p108">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta. Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*. Esta consulta selecciona los contactos más relevantes para usted, los ordena por su **displayName** y luego devuelve los 10 primeros contactos en la lista ordenada.</span><span class="sxs-lookup"><span data-stu-id="5b849-p108">By default, the people in the response are sorted by their relevance to your query. You can change the order of the people in the response by using the *$orderby* parameter. This query selects the people most relevant to you, sorts them by their **displayName**, and then returns the first 10 people on the sorted list.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$orderby=displayName
```

<span data-ttu-id="5b849-p109">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro *$top*. En el ejemplo siguiente se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="5b849-p109">The following example shows the response. By default, each response returns 10 records. You can change this by using the *$top* parameter. The following example uses *$top* to limit the response to three records.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "818E29A1-E6BB-4EDA-AB20-8230B4B1E290",
            "displayName": "Adriana Ramos",
            "givenName": "Adriana",
            "surname": "Ramos",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Product Marketing Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "18/2111",
            "profession": "",
            "userPrincipalName": "Adrianar@contoso.onmicrosoft.com",
            "imAddress": "sip:Adrianar@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Adrianar@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 425 555 0109"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "62633BAA-1CB9-4FA2-9B8F-55AB1840B69D",
            "displayName": "Alyce Cooley",
            "givenName": "Alyce",
            "surname": "Cooley",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Marketing Assistant",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "131/1104",
            "profession": "",
            "userPrincipalName": "Alycec@contoso.onmicrosoft.com",
            "imAddress": "sip:Alycec@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Alycec@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 858 555 0110"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "6BB54D2C-EF20-48DA-ADD9-AE757DD30C4E",
            "displayName": "Alyssa Clarke",
            "givenName": "Alyssa",
            "surname": "Clarke",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Corporate Security Officer",
            "companyName": null,
            "yomiCompany": "",
            "department": "Operations",
            "officeLocation": "24/1106",
            "profession": "",
            "userPrincipalName": "Alyssac@contoso.onmicrosoft.com",
            "imAddress": "sip:Alyssac@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Alyssac@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 262 555 0106"
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
### <a name="change-the-number-of-people-and-fields-returned"></a><span data-ttu-id="5b849-139">Cambiar el número de contactos y campos devueltos</span><span class="sxs-lookup"><span data-stu-id="5b849-139">Change the number of people and fields returned</span></span> 
<span data-ttu-id="5b849-140">Puede cambiar el número de contactos devueltos en la respuesta estableciendo el parámetro *$top*.</span><span class="sxs-lookup"><span data-stu-id="5b849-140">You can change the number of people returned in the response by setting the *$top* parameter.</span></span> 

<span data-ttu-id="5b849-p110">En el siguiente ejemplo se solicitan los 1000 contactos más relevantes para `/me`. La solicitud limita también la cantidad de datos que se devuelven del servidor solicitando solo el **displayName** del contacto.</span><span class="sxs-lookup"><span data-stu-id="5b849-p110">The following example requests the 1,000 people most relevant to `/me`. The request also limits the amount of data sent back from the server by requesting only the **displayName** of the person.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$top=1000&$Select=displayName
```

<span data-ttu-id="5b849-143">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b849-143">The following example shows the response.</span></span> 

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "8CE6E1DE-CB84-4BF5-971D-D3ECF452E2B5",
            "displayName": "Lorrie Frye"
        },
        {
            "id": "5767393D-42BA-4E5C-BEE4-52BB25639CF4",
            "displayName": "Maynard Denman"
        },
        {
            "id": "914B5191-11FA-4C0B-A354-0FA8C8EFD585",
            "displayName": "Darrel Halsey"
        },
        {
            "id": "E3C5B235-DE15-4566-B7B1-7A8E32426540",
            "displayName": "Roscoe Seidel"
        },
        {
            "id": "6BB54D2C-EF20-48DA-ADD9-AE757DD30C4E",
            "displayName": "Alyssa Clarke"
        },
        {
            "id": "818E29A1-E6BB-4EDA-AB20-8230B4B1E290",
            "displayName": "Adriana Ramos"
        },
        {
            "id": "62633BAA-1CB9-4FA2-9B8F-55AB1840B69D",
            "displayName": "Alyce Cooley"
        },
        {
            "id": "6BB9CC1F-418D-4DDF-AB0C-6A1C4ABCDBF4",
            "displayName": "Wayne Leeper"
        },
        {
            "id": "E7D40AC5-0078-4575-B1F3-F738124C4BC9",
            "displayName": "Jan Travis"
        },
        {
            "id": "6F99D1CC-4FCC-49E4-9160-E8AB01BF3E83",
            "displayName": "Charlotte Delacruz"
        },
        {
            "id": "1F28616D-BDFE-4080-8F06-03366A851688",
            "displayName": "Felix Coppola"
        },
        {
            "id": "8A3FC021-6DBB-44AC-8884-B7B500CC260A",
            "displayName": "Lenora Rowland"
        },
        {
            "id": "032C9919-4DF9-4715-8C46-4D0FAE7B3EB2",
            "displayName": "Manuel Collette"
        },
      ... etc
}
```
### <a name="select-the-fields-to-return"></a><span data-ttu-id="5b849-144">Seleccionar los campos que se van a devolver</span><span class="sxs-lookup"><span data-stu-id="5b849-144">Select the fields to return</span></span>
<span data-ttu-id="5b849-p111">Puede limitar la cantidad de datos devueltos desde el servidor usando el parámetro *$select* para elegir uno o varios campos. El campo `@odata.id` siempre se devuelve.</span><span class="sxs-lookup"><span data-stu-id="5b849-p111">You can limit the amount of data returned from the server by using the *$select* parameter to choose one or more fields. The `@odata.id` field is always returned.</span></span>

<span data-ttu-id="5b849-147">El ejemplo siguiente limita la respuesta al **displayName** y el **scoredEmailAddresses** de los 10 contactos más relevantes.</span><span class="sxs-lookup"><span data-stu-id="5b849-147">The following example limits the response to the **displayName** and **scoredEmailAddresses** of the 10 most relevant people.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$select=displayName,scoredEmailAddresses
```

<span data-ttu-id="5b849-p112">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro *$top*. En este ejemplo se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="5b849-p112">The following example shows the response. By default, each response returns 10 records. You can change this using the *$top* parameter. This example uses *$top* to limit the response to three records.</span></span>

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
        },
        {
            "id": "5767393D-42BA-4E5C-BEE4-52BB25639CF4",
            "displayName": "Maynard Denman",
            "scoredEmailAddresses": [
                {
                    "address": "Maynardd@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ]
        },
        {
            "id": "914B5191-11FA-4C0B-A354-0FA8C8EFD585",
            "displayName": "Darrel Halsey",
            "scoredEmailAddresses": [
                {
                    "address": "Darrelh@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ]
        }
    ]
}
```
### <a name="use-a-filter-to-limit-the-response"></a><span data-ttu-id="5b849-152">Usar un filtro para limitar la respuesta</span><span class="sxs-lookup"><span data-stu-id="5b849-152">Use a filter to limit the response</span></span> 
<span data-ttu-id="5b849-153">Puede usar el parámetro *$filter* para limitar la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="5b849-153">You can use the *$filter* parameter to limit the response to only those people whose record contains the specified criteria.</span></span> 

<span data-ttu-id="5b849-154">La consulta siguiente limita la respuesta a las instancias de **person** que tienen la propiedad **personType** que se asigna a **person** como **class** y **organizationUser** como **subclass**.</span><span class="sxs-lookup"><span data-stu-id="5b849-154">The following query limits the response to **person** instances with the **personType** property being assigned **person** as **class** and **organizationUser** as **subclass**.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$filter=personType/class eq 'Person' and personType/subclass eq 'OrganizationUser'
```

<span data-ttu-id="5b849-p113">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro *$top*. En este ejemplo se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="5b849-p113">The following example shows the response. By default, each response returns 10 records. You can change this using the *$top* parameter. This example uses *$top* to limit the response to three records.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "8CE6E1DE-CB84-4BF5-971D-D3ECF452E2B5",
            "displayName": "Lorrie Frye",
            "givenName": "Lorrie",
            "surname": "Frye",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Paralegal",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "20/1109",
            "profession": "",
            "userPrincipalName": "Lorrief@contoso.onmicrosoft.com",
            "imAddress": "sip:Lorrief@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Lorrief@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 980 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "5767393D-42BA-4E5C-BEE4-52BB25639CF4",
            "displayName": "Maynard Denman",
            "givenName": "Maynard",
            "surname": "Denman",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Web Marketing Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/1101",
            "profession": "",
            "userPrincipalName": "Maynardd@contoso.onmicrosoft.com",
            "imAddress": "sip:Maynardd@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Maynardd@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 918 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "914B5191-11FA-4C0B-A354-0FA8C8EFD585",
            "displayName": "Darrel Halsey",
            "givenName": "Darrel",
            "surname": "Halsey",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Attorney",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "14/1102",
            "profession": "",
            "userPrincipalName": "Darrelh@contoso.onmicrosoft.com",
            "imAddress": "sip:Darrelh@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Darrelh@contoso.onmicrosoft.com",
                    "relevanceScore": 8
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 205 555 0103"
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
### <a name="select-the-fields-to-return-in-a-filtered-response"></a><span data-ttu-id="5b849-159">Seleccionar los campos que se van a devolver en una respuesta filtrada</span><span class="sxs-lookup"><span data-stu-id="5b849-159">Select the fields to return in a filtered response</span></span> 
<span data-ttu-id="5b849-160">Puede combinar los parámetros *$select* y *$filter* para crear una lista personalizada de contactos relevantes para el usuario y obtener solo los campos que la aplicación necesita.</span><span class="sxs-lookup"><span data-stu-id="5b849-160">You can combine the *$select* and *$filter* parameters to create a custom list of people relevant to the user and get only the fields that your application needs.</span></span> 

<span data-ttu-id="5b849-p114">En el ejemplo siguiente se obtiene el **displayName** y el **scoredEmailAddresses** de los contactos cuyo nombre para mostrar es igual al nombre especificado. En este ejemplo, solo se devuelven los contactos cuyo nombre para mostrar es igual a "Lorrie Frye".</span><span class="sxs-lookup"><span data-stu-id="5b849-p114">The following example gets the **displayName** and **scoredEmailAddresses** of people whose display name equals the specified name. In this example, only people whose display name equals "Lorrie Frye" are returned.</span></span> 

```http
GET https://graph.microsoft.com/v1.0/me/people/?$select=displayName,scoredEmailAddresses&$filter=displayName eq 'Lorrie Frye'
```

<span data-ttu-id="5b849-163">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b849-163">The following example shows the response.</span></span> 

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
## <a name="search-people"></a><span data-ttu-id="5b849-164">Buscar contactos</span><span class="sxs-lookup"><span data-stu-id="5b849-164">Search people</span></span>
<span data-ttu-id="5b849-p115">Las solicitudes de esta sección le permiten buscar contactos relevantes para el usuario que ha iniciado sesión (`/me`) y otros usuarios de la organización del usuario que ha iniciado sesión. Estas solicitudes requieren el permiso People.Read, salvo que se busquen contactos relevantes para otros usuarios, que requiere People.Read.All. De manera predeterminada, cada respuesta devuelve 10 registros, pero esto se puede cambiar mediante el parámetro *$top*.</span><span class="sxs-lookup"><span data-stu-id="5b849-p115">The requests in this section allow you to search for people relevant to the signed-in user (`/me`) and other users in the signed-in user’s organization. These requests require the People.Read permission, with the exception of searching other users’ relevant people, which requires People.Read.All. By default, each response returns 10 records, but you can change this by using the *$top* parameter.</span></span> 
### <a name="use-search-to-select-people"></a><span data-ttu-id="5b849-168">Usar la búsqueda para seleccionar contactos</span><span class="sxs-lookup"><span data-stu-id="5b849-168">Use search to select people</span></span> 
<span data-ttu-id="5b849-169">Use el parámetro *$search* para seleccionar contactos que reúnan un conjunto de criterios concreto.</span><span class="sxs-lookup"><span data-stu-id="5b849-169">Use the *$search* parameter to select people who meet a particular set of criteria.</span></span> 

<span data-ttu-id="5b849-170">La siguiente consulta de búsqueda devuelve contactos relevantes para `/me` cuyo **displayName** o \*emailAddress" incluya una palabra que comience con la letra "j".</span><span class="sxs-lookup"><span data-stu-id="5b849-170">The following search query returns people relevant to `/me` whose **displayName** has a word that begins with the letter "j".</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search=j
```

<span data-ttu-id="5b849-p116">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro *$top*. En este ejemplo se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="5b849-p116">The following example shows the response. By default, each response returns 10 records. You can change this using the *$top* parameter. This example uses *$top* to limit the response to three records.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "E3C5B235-DE15-4566-B7B1-7A8E32426540",
            "displayName": "Jan Travis",
            "givenName": "Jan",
            "surname": "Travis",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "VP Sales",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "19/3123",
            "profession": "",
            "userPrincipalName": "jant@contoso.onmicrosoft.com",
            "imAddress": "sip:jant@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "jant@contoso.onmicrosoft.com",
                    "relevanceScore": -12.297347783416837
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 732 555 0102"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "C43BF05E-5B6B-4DCF-B2FC-0837B09E0FA9",
            "displayName": "Jacob Cazares (TAILSPIN)",
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
                    "address": "jacobc@tailspintoys.com",
                    "relevanceScore": -12.298154282019846
                }
            ],
            "phones": [],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "PersonalContact"
            }
        },
        {
            "id": "6BB9CC1F-418D-4DDF-AB0C-6A1C4ABCDBF4",
            "displayName": "Jewell Montgomery",
            "givenName": "Jewell",
            "surname": "Montgomery",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": null,
            "companyName": null,
            "yomiCompany": "",
            "department": null,
            "officeLocation": null,
            "profession": "",
            "userPrincipalName": "jewellm@contoso.onmicrosoft.com",
            "imAddress": null,
            "scoredEmailAddresses": [
                {
                    "address": "jewellm@contoso.onmicrosoft.com",
                    "relevanceScore": -12.531408487977451
                }
            ],
            "phones": [],
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
### <a name="perform-a-fuzzy-search"></a><span data-ttu-id="5b849-175">Realizar una búsqueda aproximada</span><span class="sxs-lookup"><span data-stu-id="5b849-175">Perform a fuzzy search</span></span> 

<span data-ttu-id="5b849-176">Las búsquedas implementan un algoritmo de coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="5b849-176">Searches implement a fuzzy matching algorithm.</span></span> <span data-ttu-id="5b849-177">Se devolverán resultados basados en una coincidencia exacta y también en inferencias sobre la intención de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5b849-177">They will return results based on an exact match and also on inferences about the intent of the search.</span></span> <span data-ttu-id="5b849-178">Por ejemplo, imagine un usuario con el nombre para mostrar "Tyler Lee" y la dirección de correo tylerle@example.com que se encuentra en la colección de **usuarios** del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="5b849-178">For example, imagine a user with a display name of "Tyler Lee" and an email address of tylerle@example.com who is in the **people** collection of the signed-in user.</span></span> <span data-ttu-id="5b849-179">Todas las búsquedas siguientes devolverán este usuario Tyler como uno de los resultados.</span><span class="sxs-lookup"><span data-stu-id="5b849-179">All of the following searches will return this user Tyler as one of the results.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people?$search=tyler                //matches both Tyler's name and email
GET https://graph.microsoft.com/v1.0/me/people?$search=tylerle              //matches Tyler's email
GET https://graph.microsoft.com/v1.0/me/people?$search="tylerle@example.com"  //matches Tyler's email. Note the quotes to enclose '@'.
GET https://graph.microsoft.com/v1.0/me/people?$search=tiler                //fuzzy match with Tyler's name 
GET https://graph.microsoft.com/v1.0/me/people?$search="tyler lee"          //matches Tyler's name. Note the quotes to enclose the space.
```

<span data-ttu-id="5b849-180">También puede realizar búsquedas de contactos relevantes para el usuario que ha iniciado sesión y hayan expresado interés en comunicarse con ese usuario sobre temas como pizzas, en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5b849-180">You can also perform searches for people who are relevant to the signed-in user and have expressed an interest in communicating with that user over topics such as pizzas in the following example:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="topic:pizza"                
```

<span data-ttu-id="5b849-181">Los temas en este contexto son tan solo palabras que los usuarios han usado más a menudo en conversaciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5b849-181">Topics in this context are just words that have been used most by users in email conversations.</span></span> <span data-ttu-id="5b849-182">Microsoft extrae esas palabras y crea un índice con estos datos para facilitar las búsquedas aproximadas.</span><span class="sxs-lookup"><span data-stu-id="5b849-182">Microsoft extracts such words and creates an index for this data to facilitate fuzzy searches.</span></span> 

<span data-ttu-id="5b849-183">Tenga en cuenta que la frase de búsqueda se incluye entre comillas y los temas de estos datos se extraen sin contexto.</span><span class="sxs-lookup"><span data-stu-id="5b849-183">Note that the search phrase is enclosed in quotes, and topics in this data are extracted free of their contexts.</span></span> <span data-ttu-id="5b849-184">Por ejemplo, la búsqueda de "ventanas" en la consulta siguiente:</span><span class="sxs-lookup"><span data-stu-id="5b849-184">As an example, searching for "windows" in the following query:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="topic:windows" 
```
<span data-ttu-id="5b849-185">es una búsqueda aproximada en el índice de datos de tema y los resultados pueden incluir instancias relacionadas con una abertura en una pared o con otras definiciones.</span><span class="sxs-lookup"><span data-stu-id="5b849-185">is a fuzzy search in the topic data index, and the results can include instances that mean the Windows operating system, an opening in a building wall, or other definitions.</span></span>

<span data-ttu-id="5b849-186">Por último, puede combinar búsquedas de contactos y de temas en la misma solicitud combinando los dos tipos de expresión de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5b849-186">Finally, you can combine both people searches and topic searches in the same request by combining the two types of search expression.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="tyl topic:pizza"                
```

<span data-ttu-id="5b849-187">Esta solicitud realiza básicamente dos búsquedas: una búsqueda parcial en las propiedades **displayName** y **emailAddress** de los contactos pertinentes del usuario que ha iniciado sesión, y una búsqueda de tema para "pizza" en los contactos pertinentes del usuario.</span><span class="sxs-lookup"><span data-stu-id="5b849-187">This request essentially conducts two searches: a fuzzy search against **displayName** and **emailAddress** properties of the signed-in user's relevant people, and a topic search for "pizza" against the user's relevant people.</span></span> <span data-ttu-id="5b849-188">Después, los resultados se clasificarán, se ordenarán y se devolverán.</span><span class="sxs-lookup"><span data-stu-id="5b849-188">The results are then ranked, ordered, and returned.</span></span> <span data-ttu-id="5b849-189">Tenga en cuenta que la búsqueda no es restrictiva; puede obtener resultados que contengan contactos que coincidan con "tyl" de forma aproximada, o que están interesados en "pizza", o ambos.</span><span class="sxs-lookup"><span data-stu-id="5b849-189">Note that the search is not restrictive; you might get results that contain people that fuzzy match "tyl", or that are interested in "pizza", or both.</span></span>

### <a name="search-other-users-relevant-people"></a><span data-ttu-id="5b849-190">Buscar otros contactos relevantes para el usuario</span><span class="sxs-lookup"><span data-stu-id="5b849-190">Search other user’s relevant people</span></span>
<span data-ttu-id="5b849-p121">La siguiente solicitud obtiene los contactos más relevantes para otro contacto de la organización del usuario que ha iniciado sesión. Esta solicitud requiere el permiso People.Read.All. En este ejemplo, se muestran los contactos relevantes de Roscoe Seidel.</span><span class="sxs-lookup"><span data-stu-id="5b849-p121">The following request gets the people most relevant to another person in the signed-in user's organization. This request requires the People.Read.All permission. In this example, Roscoe Seidel's relevant people are displayed.</span></span>

```http
GET https://graph.microsoft.com/v1.0/users('roscoes@contoso.com')/people/
```

<span data-ttu-id="5b849-p122">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro *$top*. En el ejemplo siguiente se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="5b849-p122">The following example shows the response. By default, each response returns 10 records. You can change this using the *$top* parameter. The example below uses *$top* to limit the response to three records.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
     "value": [
        {
            "id": "56155636-703F-47F2-B657-C83F01F49BBC",
            "displayName": "Clifton Clemente",
            "givenName": "Clifton",
            "surname": "Clemente",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Director",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "19/2106",
            "profession": "",
            "userPrincipalName": "Cliftonc@contoso.onmicrosoft.com",
            "imAddress": "sip:Cliftonc@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Cliftonc@contoso.onmicrosoft.com",
                    "relevanceScore": 20
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 309 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "6BF27D5A-AB4F-4C43-BED0-7DAD9EB0C1C4",
            "displayName": "Sheree Mitchell",
            "givenName": "Sheree",
            "surname": "Mitchell",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Product Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/2107",
            "profession": "",
            "userPrincipalName": "Shereem@contoso.onmicrosoft.com",
            "imAddress": "sip:shereem@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Shereem@contoso.onmicrosoft.com",
                    "relevanceScore": 10
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 918 555 0107"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        },
        {
            "id": "B3E5302D-EAF0-4E8B-8C6C-A2AE64B4B163",
            "displayName": "Vincent Matney",
            "givenName": "Vincent",
            "surname": "Matney",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "CVP Engineering",
            "companyName": null,
            "yomiCompany": "",
            "department": "Engineering",
            "officeLocation": "23/2102",
            "profession": "",
            "userPrincipalName": "Vincentm@contoso.onmicrosoft.com",
            "imAddress": "sip:vincentm@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Vincentm@contoso.onmicrosoft.com",
                    "relevanceScore": 10
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 502 555 0102"
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