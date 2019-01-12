---
title: Get contact
description: Recuperar las propiedades y las relaciones de objeto de contacto.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 5e7064072ff3adf416f34e1aa4e2b12d0c661a65
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975501"
---
# <a name="get-contact"></a><span data-ttu-id="3841b-103">Get contact</span><span class="sxs-lookup"><span data-stu-id="3841b-103">Get contact</span></span>

> <span data-ttu-id="3841b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3841b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3841b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3841b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3841b-106">Recuperar las propiedades y las relaciones de objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="3841b-106">Retrieve the properties and relationships of contact object.</span></span>

<span data-ttu-id="3841b-107">Hay dos escenarios donde una aplicación puede obtener un contacto en la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="3841b-107">There are two scenarios where an app can get a contact in another user's contact folder:</span></span>

* <span data-ttu-id="3841b-108">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="3841b-108">If the app has application permissions, or,</span></span>
* <span data-ttu-id="3841b-109">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="3841b-109">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="3841b-110">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-contacts-folders).</span><span class="sxs-lookup"><span data-stu-id="3841b-110">See [details and an example](/graph/outlook-get-shared-contacts-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="3841b-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="3841b-111">Permissions</span></span>
<span data-ttu-id="3841b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3841b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3841b-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3841b-114">Permission type</span></span>      | <span data-ttu-id="3841b-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3841b-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3841b-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3841b-116">Delegated (work or school account)</span></span> | <span data-ttu-id="3841b-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3841b-117">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="3841b-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3841b-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3841b-119">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3841b-119">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="3841b-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3841b-120">Application</span></span> | <span data-ttu-id="3841b-121">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3841b-121">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3841b-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3841b-122">HTTP request</span></span>
<span data-ttu-id="3841b-123"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="3841b-123"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) in the user's mailbox.</span></span>
```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="3841b-124">[Póngase en contacto con](../resources/contact.md) desde un nivel superior [contactFolder](../resources/contactfolder.md) del usuario.</span><span class="sxs-lookup"><span data-stu-id="3841b-124">A [contact](../resources/contact.md) from a top level [contactFolder](../resources/contactfolder.md) of the user's.</span></span>
```http
GET /me/contactfolders/{Id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```
<span data-ttu-id="3841b-125">[Póngase en contacto con](../resources/contact.md) contenidos en una carpeta secundaria de un [contactFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="3841b-125">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md).</span></span>  <span data-ttu-id="3841b-126">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="3841b-126">The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3841b-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3841b-127">Optional query parameters</span></span>
|<span data-ttu-id="3841b-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="3841b-128">Name</span></span>|<span data-ttu-id="3841b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3841b-129">Value</span></span>|<span data-ttu-id="3841b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3841b-130">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="3841b-131">$expand</span><span class="sxs-lookup"><span data-stu-id="3841b-131">$expand</span></span>|<span data-ttu-id="3841b-132">string</span><span class="sxs-lookup"><span data-stu-id="3841b-132">string</span></span>|<span data-ttu-id="3841b-133">Lista separada por comas de las relaciones para expandir e incluir en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3841b-133">Comma-separated list of relationships to expand and include in the response.</span></span> <span data-ttu-id="3841b-134">Vea la tabla de relaciones de [ponerse en contacto con](../resources/contact.md) el objeto de nombres admitidos.</span><span class="sxs-lookup"><span data-stu-id="3841b-134">See relationships table of [contact](../resources/contact.md) object for supported names.</span></span> |
|<span data-ttu-id="3841b-135">$select</span><span class="sxs-lookup"><span data-stu-id="3841b-135">$select</span></span>|<span data-ttu-id="3841b-136">string</span><span class="sxs-lookup"><span data-stu-id="3841b-136">string</span></span>|<span data-ttu-id="3841b-137">Lista separada por comas de propiedades para incluir en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3841b-137">Comma-separated list of properties to include in the response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="3841b-138">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3841b-138">Request headers</span></span>
| <span data-ttu-id="3841b-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3841b-139">Header</span></span>       | <span data-ttu-id="3841b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="3841b-140">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3841b-141">Authorization</span><span class="sxs-lookup"><span data-stu-id="3841b-141">Authorization</span></span>  | <span data-ttu-id="3841b-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3841b-p106">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3841b-144">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3841b-144">Request body</span></span>
<span data-ttu-id="3841b-145">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3841b-145">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3841b-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3841b-146">Response</span></span>

<span data-ttu-id="3841b-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3841b-147">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3841b-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3841b-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3841b-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3841b-149">Request</span></span>
<span data-ttu-id="3841b-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3841b-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contact"
}-->
```http
GET https://graph.microsoft.com/beta/me/contacts/AAMkAGI2THk0AAA=
```
##### <a name="response"></a><span data-ttu-id="3841b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3841b-151">Response</span></span>
<span data-ttu-id="3841b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3841b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "AAMkAGI2THk0AAA=",
  "createdDateTime": "2014-10-19T23:08:24Z",
  "lastModifiedDateTime": "2014-10-19T23:08:24Z",
  "changeKey": "EQAAABYAAACd9nJ/tVysQos2hTfspaWRAAADTIa4",
  "categories": [],
  "parentFolderId": "AAMkAGI2AAEOAAA=",
  "birthday": "1974-07-22",
  "fileAs": "Fort, Garth",
  "displayName": "Garth Fort",
  "givenName": "Garth",
  "initials": "G.F.",
  "middleName": null,
  "nickName": "Garth",
  "surname": "Fort",
  "title": null,
  "yomiGivenName": null,
  "yomiSurname": null,
  "yomiCompanyName": null,
  "generation": null,
  "emailAddresses": [
    {
      "name": "Garth",
      "address": "garth@a830edad9050849NDA1.onmicrosoft.com",
      "type": "unknown"
    },
    {
      "name": "Garth",
      "address": "garth@contoso.onmicrosoft.com",
      "type": "personal"
    }
  ],
  "imAddresses": [
    "sip:garthf@a830edad9050849nda1.onmicrosoft.com"
  ],
  "jobTitle": "Web Marketing Manager",
  "companyName": "Contoso, Inc.",
  "department": "Sales & Marketing",
  "officeLocation": "20/1101",
  "profession": null,
  "assistantName": null,
  "manager": null,
  "phones": [{
    "type": "business",
    "number": "+1 918 555 0101"
  }],
  "postalAddresses": [{
    "type": "business",
    "postOfficeBox": "P.O. Box 100",
    "street": "123 Some street",
    "city": "Seattle",
    "state": "WA",
    "countryOrRegion": "USA",
    "postalCode": "98121"
  }],
  "spouseName": null,
  "personalNotes": null,
  "children": [], 
  "gender": null,
  "websites": [{
      "type": "work",
      "address": "https://www.contoso.com",
      "name": "Contoso"
  }],
  "weddingAnniversary": null
}
```

## <a name="see-also"></a><span data-ttu-id="3841b-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="3841b-155">See also</span></span>

- [<span data-ttu-id="3841b-156">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="3841b-156">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="3841b-157">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="3841b-157">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
