---
title: List contacts
description: Obtenga los contactos en el buzón del usuario.
ms.openlocfilehash: 2554836607705138702e5b04a60cf4a77a8e53f3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083733"
---
# <a name="list-contacts"></a><span data-ttu-id="ab95a-103">List contacts</span><span class="sxs-lookup"><span data-stu-id="ab95a-103">List contacts</span></span>

> <span data-ttu-id="ab95a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab95a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab95a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab95a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ab95a-106">Obtenga los contactos en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ab95a-106">Get contacts in the user's mailbox.</span></span>

<span data-ttu-id="ab95a-107">Hay dos escenarios donde una aplicación puede obtener los contactos en la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="ab95a-107">There are two scenarios where an app can get contacts in another user's contact folder:</span></span>

* <span data-ttu-id="ab95a-108">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="ab95a-108">If the app has application permissions, or,</span></span>
* <span data-ttu-id="ab95a-109">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="ab95a-109">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="ab95a-110">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-contacts-folders).</span><span class="sxs-lookup"><span data-stu-id="ab95a-110">See [details and an example](/graph/outlook-get-shared-contacts-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="ab95a-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="ab95a-111">Permissions</span></span>
<span data-ttu-id="ab95a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab95a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ab95a-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab95a-114">Permission type</span></span>      | <span data-ttu-id="ab95a-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab95a-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ab95a-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab95a-116">Delegated (work or school account)</span></span> | <span data-ttu-id="ab95a-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ab95a-117">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="ab95a-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab95a-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ab95a-119">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ab95a-119">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="ab95a-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab95a-120">Application</span></span> | <span data-ttu-id="ab95a-121">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ab95a-121">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ab95a-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab95a-122">HTTP request</span></span>

<span data-ttu-id="ab95a-123">Para obtener todos los contactos del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="ab95a-123">To get all the contacts in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

<span data-ttu-id="ab95a-124">Para obtener los contactos de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="ab95a-124">To get contacts in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ab95a-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ab95a-125">Optional query parameters</span></span>
<span data-ttu-id="ab95a-126">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab95a-126">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="ab95a-127">Por ejemplo, puede usar el parámetro de consulta `$filter` para filtrar contactos en función del dominio de sus direcciones de correo:</span><span class="sxs-lookup"><span data-stu-id="ab95a-127">For example, you can use the `$filter` query parameter to filter contacts based on the domain of their email addresses:</span></span>

`https://graph.microsoft.com/v1.0/me/contacts?$filter=emailAddresses/any(a:a/address eq '@domain.com')`

## <a name="request-headers"></a><span data-ttu-id="ab95a-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab95a-128">Request headers</span></span>
| <span data-ttu-id="ab95a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab95a-129">Header</span></span>       | <span data-ttu-id="ab95a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ab95a-130">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ab95a-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="ab95a-131">Authorization</span></span>  | <span data-ttu-id="ab95a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab95a-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ab95a-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ab95a-134">Request body</span></span>
<span data-ttu-id="ab95a-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ab95a-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ab95a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab95a-136">Response</span></span>

<span data-ttu-id="ab95a-137">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos [de contacto](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab95a-137">If successful, this method returns a `200 OK` response code and collection of [contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ab95a-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab95a-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ab95a-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab95a-139">Request</span></span>
<span data-ttu-id="ab95a-140">En el ejemplo siguiente se obtiene las propiedades **displayName** y **emailAddresses** de contactos del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="ab95a-140">The following example gets the **displayName** and **emailAddresses** properties of the signed-in user's contacts.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/beta/me/contacts?$select=displayName,emailAddresses
```


##### <a name="response"></a><span data-ttu-id="ab95a-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab95a-141">Response</span></span>
<span data-ttu-id="ab95a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab95a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
