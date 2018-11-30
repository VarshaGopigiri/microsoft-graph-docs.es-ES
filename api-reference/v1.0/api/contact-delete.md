---
title: Eliminar contact
description: Elimina un contacto.
ms.openlocfilehash: d81eb136702afd94537ea4651015ad6bbcab5450
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028937"
---
# <a name="delete-contact"></a><span data-ttu-id="771a1-103">Eliminar contact</span><span class="sxs-lookup"><span data-stu-id="771a1-103">Delete contact</span></span>

<span data-ttu-id="771a1-104">Elimina un contacto.</span><span class="sxs-lookup"><span data-stu-id="771a1-104">Delete a contact.</span></span>
## <a name="permissions"></a><span data-ttu-id="771a1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="771a1-105">Permissions</span></span>
<span data-ttu-id="771a1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="771a1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="771a1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="771a1-108">Permission type</span></span>      | <span data-ttu-id="771a1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="771a1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="771a1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="771a1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="771a1-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="771a1-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="771a1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="771a1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="771a1-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="771a1-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="771a1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="771a1-114">Application</span></span> | <span data-ttu-id="771a1-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="771a1-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="771a1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="771a1-116">HTTP request</span></span>
<span data-ttu-id="771a1-117"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde predeterminado de un usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="771a1-117"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contacts/{id}
DELETE /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="771a1-118">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="771a1-118">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contactFolders/{id}/contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="771a1-p102">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="771a1-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
DELETE /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="771a1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="771a1-121">Request headers</span></span>
| <span data-ttu-id="771a1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="771a1-122">Header</span></span>       | <span data-ttu-id="771a1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="771a1-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="771a1-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="771a1-124">Authorization</span></span>  | <span data-ttu-id="771a1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="771a1-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="771a1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="771a1-127">Request body</span></span>
<span data-ttu-id="771a1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="771a1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="771a1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="771a1-129">Response</span></span>

<span data-ttu-id="771a1-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="771a1-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="771a1-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="771a1-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="771a1-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="771a1-133">Request</span></span>
<span data-ttu-id="771a1-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="771a1-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_contact"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="771a1-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="771a1-135">Response</span></span>
<span data-ttu-id="771a1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="771a1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
