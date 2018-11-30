---
title: List contacts
description: Obtener todos los contactos en el buzón del usuario que ha iniciado sesión (.../me/contacts), o desde la carpeta de contactos especificada.
ms.openlocfilehash: e15080c9a4d5b0f8e388cc9556ded1ac90ce2823
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084639"
---
# <a name="list-contacts"></a><span data-ttu-id="e4214-103">List contacts</span><span class="sxs-lookup"><span data-stu-id="e4214-103">List contacts</span></span>

> <span data-ttu-id="e4214-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4214-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e4214-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e4214-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e4214-106">Obtener todos los contactos en el buzón del usuario que ha iniciado sesión (.../me/contacts), o desde la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="e4214-106">Get all the contacts in the signed-in user's mailbox (.../me/contacts), or from the specified contact folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="e4214-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4214-107">Permissions</span></span>
<span data-ttu-id="e4214-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4214-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e4214-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4214-110">Permission type</span></span>      | <span data-ttu-id="e4214-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4214-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e4214-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4214-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e4214-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4214-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="e4214-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4214-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4214-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4214-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="e4214-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4214-116">Application</span></span> | <span data-ttu-id="e4214-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4214-117">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e4214-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4214-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts

GET /me/contactFolders/{id}/contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e4214-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e4214-119">Optional query parameters</span></span>
<span data-ttu-id="e4214-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4214-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e4214-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4214-121">Request headers</span></span>
| <span data-ttu-id="e4214-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4214-122">Name</span></span>       | <span data-ttu-id="e4214-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4214-123">Type</span></span> | <span data-ttu-id="e4214-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4214-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e4214-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="e4214-125">Authorization</span></span>  | <span data-ttu-id="e4214-126">string</span><span class="sxs-lookup"><span data-stu-id="e4214-126">string</span></span>  | <span data-ttu-id="e4214-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4214-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e4214-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4214-129">Request body</span></span>
<span data-ttu-id="e4214-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e4214-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e4214-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4214-131">Response</span></span>

<span data-ttu-id="e4214-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4214-132">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e4214-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4214-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e4214-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4214-134">Request</span></span>
<span data-ttu-id="e4214-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4214-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/beta/me/contactFolders/{id}/contacts
```
##### <a name="response"></a><span data-ttu-id="e4214-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4214-136">Response</span></span>
<span data-ttu-id="e4214-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e4214-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "birthday": "2016-10-19T10:37:00Z",
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
