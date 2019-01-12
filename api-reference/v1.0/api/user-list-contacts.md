---
title: List contacts
description: Obtener una colección de contacto desde la carpeta Contactos predeterminada del usuario que ha iniciado sesión.
author: dkershaw10
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 3f0f7fd86987e3d2923d8ea81a8ca7fbf87900b1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984139"
---
# <a name="list-contacts"></a><span data-ttu-id="e8af1-103">List contacts</span><span class="sxs-lookup"><span data-stu-id="e8af1-103">List contacts</span></span>

<span data-ttu-id="e8af1-104">Obtener una colección de contacto desde la carpeta Contactos predeterminada del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="e8af1-104">Get a contact collection from the default contacts folder of the signed-in user.</span></span>

<span data-ttu-id="e8af1-105">Hay dos escenarios donde una aplicación puede obtener los contactos en la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="e8af1-105">There are two scenarios where an app can get contacts in another user's contact folder:</span></span>

* <span data-ttu-id="e8af1-106">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="e8af1-106">If the app has application permissions, or,</span></span>
* <span data-ttu-id="e8af1-107">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="e8af1-107">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="e8af1-108">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-contacts-folders).</span><span class="sxs-lookup"><span data-stu-id="e8af1-108">See [details and an example](/graph/outlook-get-shared-contacts-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="e8af1-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="e8af1-109">Permissions</span></span>
<span data-ttu-id="e8af1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8af1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8af1-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8af1-112">Permission type</span></span>      | <span data-ttu-id="e8af1-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8af1-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e8af1-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8af1-114">Delegated (work or school account)</span></span> | <span data-ttu-id="e8af1-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8af1-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="e8af1-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8af1-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e8af1-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8af1-117">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="e8af1-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8af1-118">Application</span></span> | <span data-ttu-id="e8af1-119">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8af1-119">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e8af1-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8af1-120">HTTP request</span></span>

<span data-ttu-id="e8af1-121">Para obtener todos los contactos del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="e8af1-121">To get all the contacts in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

<span data-ttu-id="e8af1-122">Para obtener los contactos de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="e8af1-122">To get contacts in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e8af1-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e8af1-123">Optional query parameters</span></span>
<span data-ttu-id="e8af1-124">Puede usar el `$filter` parámetro de consulta para filtrar contactos según sus direcciones de correo electrónico:</span><span class="sxs-lookup"><span data-stu-id="e8af1-124">You can use the `$filter` query parameter to filter contacts based on their email addresses:</span></span>

<!-- { "blockType": "ignored" } -->
``` http
GET https://graph.microsoft.com/v1.0/me/contacts?$filter=emailAddresses/any(a:a/address eq 'garth@contoso.com')
```

<span data-ttu-id="e8af1-125">Tenga en cuenta que puede usar `$filter`, `any`y el `eq` operador en sólo la propiedad subcaracterística de **dirección** de instancias de una colección de **emailAddresses** .</span><span class="sxs-lookup"><span data-stu-id="e8af1-125">Note that you can use `$filter`, `any`, and the `eq` operator on only the **address** sub-property of instances in an **emailAddresses** collection.</span></span> <span data-ttu-id="e8af1-126">Es decir, no se puede filtrar en el **nombre** o cualquier otra propiedad subcaracterística de una instancia de **emailAddresses**, ni tampoco puede aplicar cualquier otro operador o funcionar con `filter`, tales como `ne`, `le`, y `startswith()`.</span><span class="sxs-lookup"><span data-stu-id="e8af1-126">That is, you cannot filter on the **name** or any other sub-property of an instance of **emailAddresses**, nor can you apply any other operator or function with `filter`, such as `ne`, `le`, and `startswith()`.</span></span>

<span data-ttu-id="e8af1-127">Para obtener información general sobre la `$filter` parámetro de consulta, vea [parámetros de consulta de OData](/graph/query-parameters).</span><span class="sxs-lookup"><span data-stu-id="e8af1-127">For general information on the `$filter` query parameter, see [OData query parameters](/graph/query-parameters).</span></span>



## <a name="request-headers"></a><span data-ttu-id="e8af1-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8af1-128">Request headers</span></span>
| <span data-ttu-id="e8af1-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8af1-129">Header</span></span>       | <span data-ttu-id="e8af1-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e8af1-130">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e8af1-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="e8af1-131">Authorization</span></span>  | <span data-ttu-id="e8af1-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e8af1-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e8af1-134">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e8af1-134">Content-Type</span></span>   | <span data-ttu-id="e8af1-135">application/json</span><span class="sxs-lookup"><span data-stu-id="e8af1-135">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e8af1-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8af1-136">Request body</span></span>
<span data-ttu-id="e8af1-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e8af1-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e8af1-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8af1-138">Response</span></span>

<span data-ttu-id="e8af1-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8af1-139">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e8af1-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8af1-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e8af1-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8af1-141">Request</span></span>
<span data-ttu-id="e8af1-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8af1-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts
```


##### <a name="response"></a><span data-ttu-id="e8af1-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8af1-143">Response</span></span>
<span data-ttu-id="e8af1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e8af1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 263

{
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "birthday": "datetime-value",
      "fileAs": "fileAs-value",
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "initials": "initials-value"
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
