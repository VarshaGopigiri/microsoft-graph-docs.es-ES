---
title: Crear contacto
description: Agregue un contacto a la carpeta de contactos raíz o al punto de conexión de `contacts` de otra carpeta de contactos.
author: angelgolfer-ms
ms.openlocfilehash: 29432762aca0ad8d80b8d755ae3c0f45e754cb45
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321444"
---
# <a name="create-contact"></a><span data-ttu-id="177a7-103">Crear contacto</span><span class="sxs-lookup"><span data-stu-id="177a7-103">Create contact</span></span>

<span data-ttu-id="177a7-104">Agregue un contacto a la carpeta de contactos raíz o al punto de conexión de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="177a7-104">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="177a7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="177a7-105">Permissions</span></span>

<span data-ttu-id="177a7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="177a7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="177a7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="177a7-108">Permission type</span></span>      | <span data-ttu-id="177a7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="177a7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="177a7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="177a7-110">Delegated (work or school account)</span></span> | <span data-ttu-id="177a7-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="177a7-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="177a7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="177a7-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="177a7-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="177a7-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="177a7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="177a7-114">Application</span></span> | <span data-ttu-id="177a7-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="177a7-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="177a7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="177a7-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts

POST /me/contactFolders/{id}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```

<br/>

## <a name="request-headers"></a><span data-ttu-id="177a7-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="177a7-117">Request headers</span></span>

| <span data-ttu-id="177a7-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="177a7-118">Header</span></span>       | <span data-ttu-id="177a7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="177a7-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="177a7-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="177a7-120">Authorization</span></span>  | <span data-ttu-id="177a7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="177a7-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="177a7-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="177a7-123">Content-Type</span></span>  | <span data-ttu-id="177a7-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="177a7-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="177a7-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="177a7-126">Request body</span></span>
<span data-ttu-id="177a7-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="177a7-127">In the request body, supply a JSON representation of the [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="177a7-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="177a7-128">Response</span></span>

<span data-ttu-id="177a7-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="177a7-129">If successful, this method returns `201 Created` response code and the [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="177a7-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="177a7-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="177a7-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="177a7-131">Request</span></span>

<span data-ttu-id="177a7-132">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="177a7-132">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_contact_from_contactfolder"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```

<br/>

<span data-ttu-id="177a7-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="177a7-133">In the request body, supply a JSON representation of the [Contact](../resources/contact.md) object.</span></span>

### <a name="response"></a><span data-ttu-id="177a7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="177a7-134">Response</span></span>

<span data-ttu-id="177a7-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="177a7-135">Here is an example of the response.</span></span> <span data-ttu-id="177a7-136">**Nota:** Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="177a7-136">**Note:** The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="177a7-137">Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="177a7-137">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```

<br/>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
