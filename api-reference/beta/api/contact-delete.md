---
title: Eliminar contact
description: Eliminar el contacto.
author: angelgolfer-ms
ms.openlocfilehash: a8f1ea8c1ee0f202e60d4efb05f65022a9269c01
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319274"
---
# <a name="delete-contact"></a><span data-ttu-id="99323-103">Eliminar contact</span><span class="sxs-lookup"><span data-stu-id="99323-103">Delete contact</span></span>

> <span data-ttu-id="99323-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99323-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99323-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99323-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="99323-106">Eliminar el contacto.</span><span class="sxs-lookup"><span data-stu-id="99323-106">Delete contact.</span></span>
## <a name="permissions"></a><span data-ttu-id="99323-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="99323-107">Permissions</span></span>
<span data-ttu-id="99323-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="99323-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="99323-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99323-110">Permission type</span></span>      | <span data-ttu-id="99323-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99323-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="99323-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99323-112">Delegated (work or school account)</span></span> | <span data-ttu-id="99323-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="99323-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="99323-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99323-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="99323-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="99323-115">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="99323-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99323-116">Application</span></span> | <span data-ttu-id="99323-117">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="99323-117">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="99323-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99323-118">HTTP request</span></span>
<span data-ttu-id="99323-119"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde de predeterminado del usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="99323-119"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contacts/{id}
DELETE /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="99323-120">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="99323-120">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contactFolders/{id}/contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="99323-121">[Póngase en contacto con](../resources/contact.md) contenidos en una carpeta secundaria de un [contactFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="99323-121">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md).</span></span>  <span data-ttu-id="99323-122">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="99323-122">The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
DELETE /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="99323-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99323-123">Request headers</span></span>
| <span data-ttu-id="99323-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99323-124">Header</span></span>       | <span data-ttu-id="99323-125">Valor</span><span class="sxs-lookup"><span data-stu-id="99323-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="99323-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="99323-126">Authorization</span></span>  | <span data-ttu-id="99323-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="99323-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="99323-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99323-129">Request body</span></span>
<span data-ttu-id="99323-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="99323-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="99323-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99323-131">Response</span></span>

<span data-ttu-id="99323-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99323-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="99323-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99323-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="99323-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99323-135">Request</span></span>
<span data-ttu-id="99323-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99323-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_contact"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="99323-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99323-137">Response</span></span>
<span data-ttu-id="99323-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99323-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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