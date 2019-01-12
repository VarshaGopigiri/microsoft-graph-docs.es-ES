---
title: Create Contact
description: Agrega un contacto a la carpeta de contactos raíz o al extremo de `contacts` de otra carpeta de contactos.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: c4ec39584500da4e0aad8f04f03129302fbfd45b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965953"
---
# <a name="create-contact"></a><span data-ttu-id="db5fa-103">Create Contact</span><span class="sxs-lookup"><span data-stu-id="db5fa-103">Create Contact</span></span>

> <span data-ttu-id="db5fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="db5fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="db5fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="db5fa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="db5fa-106">Agregue un contacto a la carpeta de contactos raíz o al punto de conexión de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="db5fa-106">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="db5fa-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="db5fa-107">Permissions</span></span>
<span data-ttu-id="db5fa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="db5fa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="db5fa-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="db5fa-110">Permission type</span></span>      | <span data-ttu-id="db5fa-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="db5fa-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="db5fa-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="db5fa-112">Delegated (work or school account)</span></span> | <span data-ttu-id="db5fa-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="db5fa-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="db5fa-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="db5fa-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="db5fa-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="db5fa-115">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="db5fa-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="db5fa-116">Application</span></span> | <span data-ttu-id="db5fa-117">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="db5fa-117">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="db5fa-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="db5fa-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts

POST /me/contactFolders/{id}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```
## <a name="request-headers"></a><span data-ttu-id="db5fa-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="db5fa-119">Request headers</span></span>
## <a name="request-headers"></a><span data-ttu-id="db5fa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="db5fa-120">Request headers</span></span>
| <span data-ttu-id="db5fa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db5fa-121">Header</span></span>       | <span data-ttu-id="db5fa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="db5fa-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="db5fa-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="db5fa-123">Authorization</span></span>  | <span data-ttu-id="db5fa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="db5fa-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="db5fa-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="db5fa-126">Content-Type</span></span>  | <span data-ttu-id="db5fa-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="db5fa-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="db5fa-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="db5fa-129">Request body</span></span>
<span data-ttu-id="db5fa-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="db5fa-130">In the request body, supply a JSON representation of [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="db5fa-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db5fa-131">Response</span></span>

<span data-ttu-id="db5fa-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="db5fa-132">If successful, this method returns `201 Created` response code and [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="db5fa-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="db5fa-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="db5fa-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="db5fa-134">Request</span></span>
<span data-ttu-id="db5fa-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="db5fa-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contact_from_contactfolder"
}-->
```http
POST https://graph.microsoft.com/beta/me/contactFolders/{id}/contacts
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "2016-10-19T10:37:00Z",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```
<span data-ttu-id="db5fa-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="db5fa-136">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="db5fa-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db5fa-137">Response</span></span>
<span data-ttu-id="db5fa-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="db5fa-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "birthday": "2016-10-19T10:37:00Z",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
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
