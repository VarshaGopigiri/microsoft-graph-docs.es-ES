---
title: Crear contacto
description: Agregue un contacto a la carpeta de contactos raíz o al punto de conexión de `contacts` de otra carpeta de contactos.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: cd0c6d8473347ed86aff0bd83a8cd663e9b2c1ba
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967122"
---
# <a name="create-contact"></a><span data-ttu-id="d2945-103">Crear contacto</span><span class="sxs-lookup"><span data-stu-id="d2945-103">Create contact</span></span>

<span data-ttu-id="d2945-104">Agregue un contacto a la carpeta de contactos raíz o al punto de conexión de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="d2945-104">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2945-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2945-105">Permissions</span></span>

<span data-ttu-id="d2945-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2945-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2945-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2945-108">Permission type</span></span>      | <span data-ttu-id="d2945-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2945-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2945-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2945-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d2945-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2945-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="d2945-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2945-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2945-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2945-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="d2945-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2945-114">Application</span></span> | <span data-ttu-id="d2945-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2945-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2945-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2945-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts

POST /me/contactFolders/{id}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```

<br/>

## <a name="request-headers"></a><span data-ttu-id="d2945-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2945-117">Request headers</span></span>

| <span data-ttu-id="d2945-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2945-118">Header</span></span>       | <span data-ttu-id="d2945-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d2945-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d2945-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2945-120">Authorization</span></span>  | <span data-ttu-id="d2945-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2945-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d2945-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d2945-123">Content-Type</span></span>  | <span data-ttu-id="d2945-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2945-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d2945-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2945-126">Request body</span></span>
<span data-ttu-id="d2945-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="d2945-127">In the request body, supply a JSON representation of the [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="d2945-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2945-128">Response</span></span>

<span data-ttu-id="d2945-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2945-129">If successful, this method returns `201 Created` response code and the [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2945-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2945-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="d2945-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2945-131">Request</span></span>

<span data-ttu-id="d2945-132">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2945-132">Here is an example of the request.</span></span>

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

<span data-ttu-id="d2945-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="d2945-133">In the request body, supply a JSON representation of the [Contact](../resources/contact.md) object.</span></span>

### <a name="response"></a><span data-ttu-id="d2945-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2945-134">Response</span></span>

<span data-ttu-id="d2945-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2945-135">Here is an example of the response.</span></span> <span data-ttu-id="d2945-136">**Nota:** Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="d2945-136">**Note:** The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="d2945-137">Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2945-137">All the properties will be returned from an actual call.</span></span>

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
