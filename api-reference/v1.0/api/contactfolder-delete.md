---
title: Eliminar contactFolder.
description: Elimina una contactFolder que no sea la predeterminada.
author: angelgolfer-ms
ms.openlocfilehash: 3111958deba7f18585d0594bd718ebd3155ac517
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304966"
---
# <a name="delete-contactfolder"></a><span data-ttu-id="59462-103">Eliminar contactFolder.</span><span class="sxs-lookup"><span data-stu-id="59462-103">Delete contactFolder</span></span>

<span data-ttu-id="59462-104">Elimina una contactFolder que no sea la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="59462-104">Delete contactFolder other than the default contactFolder.</span></span>
## <a name="permissions"></a><span data-ttu-id="59462-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="59462-105">Permissions</span></span>
<span data-ttu-id="59462-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59462-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="59462-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59462-108">Permission type</span></span>      | <span data-ttu-id="59462-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59462-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="59462-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59462-110">Delegated (work or school account)</span></span> | <span data-ttu-id="59462-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59462-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="59462-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59462-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="59462-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59462-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="59462-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59462-114">Application</span></span> | <span data-ttu-id="59462-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59462-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="59462-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59462-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/contactFolders/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="59462-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59462-117">Request headers</span></span>
| <span data-ttu-id="59462-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="59462-118">Name</span></span>       | <span data-ttu-id="59462-119">Type</span><span class="sxs-lookup"><span data-stu-id="59462-119">Type</span></span> | <span data-ttu-id="59462-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="59462-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="59462-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="59462-121">Authorization</span></span>  | <span data-ttu-id="59462-122">string</span><span class="sxs-lookup"><span data-stu-id="59462-122">string</span></span>  | <span data-ttu-id="59462-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="59462-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="59462-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59462-125">Request body</span></span>
<span data-ttu-id="59462-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="59462-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="59462-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59462-127">Response</span></span>

<span data-ttu-id="59462-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59462-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59462-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59462-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="59462-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59462-131">Request</span></span>
<span data-ttu-id="59462-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59462-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_contactfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="59462-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59462-133">Response</span></span>
<span data-ttu-id="59462-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59462-134">Here is an example of the response.</span></span> 
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
  "description": "Delete contactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
