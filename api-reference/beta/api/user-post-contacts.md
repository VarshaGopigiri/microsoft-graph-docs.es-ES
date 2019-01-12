---
title: Create Contact
description: Agrega un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: b443a522d4f821861191bcbe7deeff2b6063b236
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967899"
---
# <a name="create-contact"></a><span data-ttu-id="e8ae6-103">Create Contact</span><span class="sxs-lookup"><span data-stu-id="e8ae6-103">Create Contact</span></span>

> <span data-ttu-id="e8ae6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e8ae6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e8ae6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e8ae6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e8ae6-106">Agrega un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="e8ae6-106">Add a contact to the root Contacts folder or to the contacts endpoint of another contact folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="e8ae6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e8ae6-107">Permissions</span></span>
<span data-ttu-id="e8ae6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8ae6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8ae6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8ae6-110">Permission type</span></span>      | <span data-ttu-id="e8ae6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8ae6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e8ae6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8ae6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e8ae6-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8ae6-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="e8ae6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8ae6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e8ae6-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8ae6-115">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="e8ae6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8ae6-116">Application</span></span> | <span data-ttu-id="e8ae6-117">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8ae6-117">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e8ae6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8ae6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts
POST /me/contactFolders/{contactFolderId}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{contactFolderId}/contacts
```
## <a name="request-headers"></a><span data-ttu-id="e8ae6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8ae6-119">Request headers</span></span>
| <span data-ttu-id="e8ae6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8ae6-120">Header</span></span>       | <span data-ttu-id="e8ae6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e8ae6-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e8ae6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e8ae6-122">Authorization</span></span>  | <span data-ttu-id="e8ae6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e8ae6-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e8ae6-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e8ae6-125">Content-Type</span></span>  | <span data-ttu-id="e8ae6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e8ae6-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e8ae6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8ae6-127">Request body</span></span>
<span data-ttu-id="e8ae6-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="e8ae6-128">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e8ae6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8ae6-129">Response</span></span>

<span data-ttu-id="e8ae6-130">Si tiene éxito, este método devuelve `201 Created` objeto de código y [póngase en contacto con](../resources/contact.md) respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8ae6-130">If successful, this method returns `201 Created` response code and [contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e8ae6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8ae6-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e8ae6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8ae6-132">Request</span></span>
<span data-ttu-id="e8ae6-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8ae6-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contact_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/contacts
Content-type: application/json

{
  "givenName": "Pavel",
  "surname": "Bansky",
  "emailAddresses": [
    {
      "address": "pavelb@contoso.onmicrosoft.com",
      "name": "Pavel Bansky",
      "type": "personal"
    },
    {
      "address": "pavelb@fabrikam.onmicrosoft.com",
      "name": "Pavel Bansky",
      "type": "other",
      "otherLabel": "Volunteer work"
    }
  ],
  "phones" : [
    {
      "number": "+1 732 555 0102",
      "type": "business"
    }
  ]
}
```
<span data-ttu-id="e8ae6-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="e8ae6-134">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="e8ae6-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8ae6-135">Response</span></span>
<span data-ttu-id="e8ae6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e8ae6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('c3e1fcd2-db78-42a8-aec5-1f2cd59abb5c')/contacts/$entity",
    "@odata.etag":"W/\"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7fW\"",
    "id":"AAMkADh6v5AAAvgTCEAAA=",
    "createdDateTime":"2018-06-11T19:56:07Z",
    "lastModifiedDateTime":"2018-06-11T19:56:07Z",
    "changeKey":"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7fW",
    "categories":[

    ],
    "parentFolderId":"AAMkADh6v5AAAAAAEOAAA=",
    "birthday":null,
    "fileAs":"",
    "displayName":"Pavel Bansky",
    "givenName":"Pavel",
    "initials":null,
    "middleName":null,
    "nickName":null,
    "surname":"Bansky",
    "title":null,
    "yomiGivenName":null,
    "yomiSurname":null,
    "yomiCompanyName":null,
    "generation":null,
    "imAddresses":[

    ],
    "jobTitle":null,
    "companyName":null,
    "department":null,
    "officeLocation":null,
    "profession":null,
    "assistantName":null,
    "manager":null,
    "spouseName":null,
    "personalNotes":"",
    "children":[

    ],
    "gender":null,
    "isFavorite":null,
    "emailAddresses":[
        {
            "type":"personal",
            "name":"Pavel Bansky",
            "address":"pavelb@contoso.onmicrosoft.com"
        },
        {
            "otherLabel": "Volunteer work",
            "type":"other",
            "name":"Pavel Bansky",
            "address":"pavelb@fabrikam.onmicrosoft.com"
        }
    ],
    "websites":[

    ],
    "phones":[
        {
            "type":"business",
            "number":"+1 732 555 0102"
        }
    ],
    "postalAddresses":[

    ],
    "flag":{
        "flagStatus":"notFlagged"
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e8ae6-139">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e8ae6-139">See also</span></span>

- [<span data-ttu-id="e8ae6-140">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="e8ae6-140">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="e8ae6-141">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="e8ae6-141">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
