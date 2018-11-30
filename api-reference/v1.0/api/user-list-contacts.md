---
title: List contacts
description: Obtener una colección de contacto desde la carpeta Contactos predeterminada del usuario que ha iniciado sesión.
ms.openlocfilehash: 296844eb4eea93c5bd46e8028f3423fe797142ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030792"
---
# <a name="list-contacts"></a><span data-ttu-id="1d135-103">List contacts</span><span class="sxs-lookup"><span data-stu-id="1d135-103">List contacts</span></span>

<span data-ttu-id="1d135-104">Obtener una colección de contacto desde la carpeta Contactos predeterminada del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="1d135-104">Get a contact collection from the default contacts folder of the signed-in user.</span></span>

<span data-ttu-id="1d135-105">Hay dos escenarios donde una aplicación puede obtener los contactos en la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="1d135-105">There are two scenarios where an app can get contacts in another user's contact folder:</span></span>

* <span data-ttu-id="1d135-106">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="1d135-106">If the app has application permissions, or,</span></span>
* <span data-ttu-id="1d135-107">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="1d135-107">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="1d135-108">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-contacts-folders).</span><span class="sxs-lookup"><span data-stu-id="1d135-108">See [details and an example](/graph/outlook-get-shared-contacts-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="1d135-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d135-109">Permissions</span></span>
<span data-ttu-id="1d135-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d135-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d135-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d135-112">Permission type</span></span>      | <span data-ttu-id="1d135-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d135-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1d135-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d135-114">Delegated (work or school account)</span></span> | <span data-ttu-id="1d135-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d135-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="1d135-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d135-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1d135-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d135-117">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="1d135-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d135-118">Application</span></span> | <span data-ttu-id="1d135-119">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d135-119">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="1d135-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d135-120">HTTP request</span></span>

<span data-ttu-id="1d135-121">Para obtener todos los contactos del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="1d135-121">To get all the contacts in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

<span data-ttu-id="1d135-122">Para obtener los contactos de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="1d135-122">To get contacts in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1d135-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1d135-123">Optional query parameters</span></span>
<span data-ttu-id="1d135-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d135-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="1d135-125">Por ejemplo, puede usar el parámetro de consulta `$filter` para filtrar contactos en función del dominio de sus direcciones de correo:</span><span class="sxs-lookup"><span data-stu-id="1d135-125">For example, you can use the `$filter` query parameter to filter contacts based on the domain of their email addresses:</span></span>

`https://graph.microsoft.com/v1.0/me/contacts?$filter=emailAddresses/any(a:a/address eq '@domain.com')`



## <a name="request-headers"></a><span data-ttu-id="1d135-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d135-126">Request headers</span></span>
| <span data-ttu-id="1d135-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d135-127">Header</span></span>       | <span data-ttu-id="1d135-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1d135-128">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1d135-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d135-129">Authorization</span></span>  | <span data-ttu-id="1d135-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d135-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="1d135-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1d135-132">Content-Type</span></span>   | <span data-ttu-id="1d135-133">application/json</span><span class="sxs-lookup"><span data-stu-id="1d135-133">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1d135-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d135-134">Request body</span></span>
<span data-ttu-id="1d135-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1d135-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1d135-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d135-136">Response</span></span>

<span data-ttu-id="1d135-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d135-137">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1d135-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d135-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1d135-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d135-139">Request</span></span>
<span data-ttu-id="1d135-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d135-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts
```


##### <a name="response"></a><span data-ttu-id="1d135-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d135-141">Response</span></span>
<span data-ttu-id="1d135-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d135-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
