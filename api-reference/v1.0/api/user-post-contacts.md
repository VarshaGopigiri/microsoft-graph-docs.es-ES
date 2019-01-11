---
title: Create Contact
description: Agrega un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: bde2046f8b8dc687f40c53856c3aeabbcb75fdee
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806884"
---
# <a name="create-contact"></a><span data-ttu-id="a537d-103">Create Contact</span><span class="sxs-lookup"><span data-stu-id="a537d-103">Create Contact</span></span>

<span data-ttu-id="a537d-104">Agrega un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="a537d-104">Add a contact to the root Contacts folder or to the contacts endpoint of another contact folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="a537d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a537d-105">Permissions</span></span>
<span data-ttu-id="a537d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a537d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a537d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a537d-108">Permission type</span></span>      | <span data-ttu-id="a537d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a537d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a537d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a537d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a537d-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a537d-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="a537d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a537d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a537d-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a537d-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="a537d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a537d-114">Application</span></span> | <span data-ttu-id="a537d-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a537d-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a537d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a537d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts
POST /me/contactFolders/{contactFolderId}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{contactFolderId}/contacts
```
## <a name="request-headers"></a><span data-ttu-id="a537d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a537d-117">Request headers</span></span>
| <span data-ttu-id="a537d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a537d-118">Header</span></span>       | <span data-ttu-id="a537d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a537d-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a537d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a537d-120">Authorization</span></span>  | <span data-ttu-id="a537d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a537d-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a537d-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a537d-123">Content-Type</span></span>  | <span data-ttu-id="a537d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a537d-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a537d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a537d-125">Request body</span></span>
<span data-ttu-id="a537d-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="a537d-126">In the request body, supply a JSON representation of [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="a537d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a537d-127">Response</span></span>

<span data-ttu-id="a537d-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a537d-128">If successful, this method returns `201 Created` response code and [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a537d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a537d-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a537d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a537d-130">Request</span></span>
<span data-ttu-id="a537d-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a537d-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contact_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contacts
Content-type: application/json

{
  "givenName": "Pavel",
  "surname": "Bansky",
  "emailAddresses": [
    {
      "address": "pavelb@fabrikam.onmicrosoft.com",
      "name": "Pavel Bansky"
    }
  ],
  "businessPhones": [
    "+1 732 555 0102"
  ]
}
```
<span data-ttu-id="a537d-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="a537d-132">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="a537d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a537d-133">Response</span></span>
<span data-ttu-id="a537d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a537d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "id-value",
  "createdDateTime": "2015-11-09T02:14:32Z",
  "lastModifiedDateTime": "2015-11-09T02:14:32Z",
   "displayName": "Pavel Bansky"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
