---
title: List contacts
description: Obtenga los contactos en el buzón del usuario.
localization_priority: Normal
ms.openlocfilehash: b78009d44fd442bab31b9911056023256a1d5102
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886621"
---
# <a name="list-contacts"></a><span data-ttu-id="1ce96-103">List contacts</span><span class="sxs-lookup"><span data-stu-id="1ce96-103">List contacts</span></span>

> <span data-ttu-id="1ce96-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1ce96-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1ce96-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1ce96-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1ce96-106">Obtenga los contactos en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="1ce96-106">Get contacts in the user's mailbox.</span></span>

<span data-ttu-id="1ce96-107">Hay dos escenarios donde una aplicación puede obtener los contactos en la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="1ce96-107">There are two scenarios where an app can get contacts in another user's contact folder:</span></span>

* <span data-ttu-id="1ce96-108">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="1ce96-108">If the app has application permissions, or,</span></span>
* <span data-ttu-id="1ce96-109">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="1ce96-109">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="1ce96-110">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-contacts-folders).</span><span class="sxs-lookup"><span data-stu-id="1ce96-110">See [details and an example](/graph/outlook-get-shared-contacts-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="1ce96-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="1ce96-111">Permissions</span></span>
<span data-ttu-id="1ce96-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1ce96-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1ce96-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ce96-114">Permission type</span></span>      | <span data-ttu-id="1ce96-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ce96-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1ce96-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ce96-116">Delegated (work or school account)</span></span> | <span data-ttu-id="1ce96-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ce96-117">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="1ce96-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ce96-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1ce96-119">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ce96-119">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="1ce96-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ce96-120">Application</span></span> | <span data-ttu-id="1ce96-121">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ce96-121">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="1ce96-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ce96-122">HTTP request</span></span>

<span data-ttu-id="1ce96-123">Para obtener todos los contactos del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="1ce96-123">To get all the contacts in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

<span data-ttu-id="1ce96-124">Para obtener los contactos de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="1ce96-124">To get contacts in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1ce96-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1ce96-125">Optional query parameters</span></span>
<span data-ttu-id="1ce96-126">Puede usar el `$filter` parámetro de consulta para filtrar contactos según sus direcciones de correo electrónico:</span><span class="sxs-lookup"><span data-stu-id="1ce96-126">You can use the `$filter` query parameter to filter contacts based on their email addresses:</span></span>

<!-- { "blockType": "ignored" } -->
``` http
GET https://graph.microsoft.com/beta/me/contacts?$filter=emailAddresses/any(a:a/address eq 'garth@contoso.com')
```

<span data-ttu-id="1ce96-127">Tenga en cuenta que puede usar `$filter`, `any`y el `eq` operador en sólo la propiedad subcaracterística de **dirección** de instancias de una colección de **emailAddresses** .</span><span class="sxs-lookup"><span data-stu-id="1ce96-127">Note that you can use `$filter`, `any`, and the `eq` operator on only the **address** sub-property of instances in an **emailAddresses** collection.</span></span> <span data-ttu-id="1ce96-128">Es decir, no se puede filtrar en el **nombre** o cualquier otra propiedad subcaracterística de una instancia de **emailAddresses**, ni tampoco puede aplicar cualquier otro operador o funcionar con `filter`, tales como `ne`, `le`, y `startswith()`.</span><span class="sxs-lookup"><span data-stu-id="1ce96-128">That is, you cannot filter on the **name** or any other sub-property of an instance of **emailAddresses**, nor can you apply any other operator or function with `filter`, such as `ne`, `le`, and `startswith()`.</span></span>

<span data-ttu-id="1ce96-129">Para obtener información general sobre la `$filter` parámetro de consulta, vea [parámetros de consulta de OData](/graph/query-parameters).</span><span class="sxs-lookup"><span data-stu-id="1ce96-129">For general information on the `$filter` query parameter, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="1ce96-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ce96-130">Request headers</span></span>
| <span data-ttu-id="1ce96-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ce96-131">Header</span></span>       | <span data-ttu-id="1ce96-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1ce96-132">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1ce96-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="1ce96-133">Authorization</span></span>  | <span data-ttu-id="1ce96-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ce96-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1ce96-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ce96-136">Request body</span></span>
<span data-ttu-id="1ce96-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1ce96-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1ce96-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ce96-138">Response</span></span>

<span data-ttu-id="1ce96-139">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos [de contacto](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ce96-139">If successful, this method returns a `200 OK` response code and collection of [contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1ce96-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ce96-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1ce96-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ce96-141">Request</span></span>
<span data-ttu-id="1ce96-142">En el ejemplo siguiente se obtiene las propiedades **displayName** y **emailAddresses** de contactos del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="1ce96-142">The following example gets the **displayName** and **emailAddresses** properties of the signed-in user's contacts.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/beta/me/contacts?$select=displayName,emailAddresses
```


##### <a name="response"></a><span data-ttu-id="1ce96-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ce96-143">Response</span></span>
<span data-ttu-id="1ce96-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ce96-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('c3e1fcd2-db78-42a8-aec5-1f2cd59abb5c')/contacts(displayName,emailAddresses)",
    "value":[
        {
            "@odata.etag":"W/\"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7f6\"",
            "id":"AAMkADh6v5AAAvgTCFAAA=",
            "displayName":"Elvis Blank",
            "emailAddresses":[
                {
                    "type":"personal",
                    "name":"Elvis Blank",
                    "address":"elvisb@relecloud.onmicrosoft.com"
                },
                {
                    "type":"other",
                    "otherLabel":"Volunteer work",
                    "name":"Elvis Blank",
                    "address":"elvisb@fabrikam.onmicrosoft.com"
                }
            ]
        },
        {
            "@odata.etag":"W/\"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7fn\"",
            "id":"AAMkADh6v5AAAvgTCEAAA=",
            "displayName":"Pavel Bansky",
            "emailAddresses":[
                {
                    "type":"personal",
                    "name":"Pavel Bansky",
                    "address":"pavelb@contoso.onmicrosoft.com"
                },
                {
                    "type":"other",
                    "otherLabel":"Volunteer work",
                    "name":"Pavel Bansky",
                    "address":"pavelb@fabrikam.onmicrosoft.com"
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
  "description": "List contacts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
