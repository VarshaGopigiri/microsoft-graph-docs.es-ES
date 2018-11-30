---
title: Eliminar contactFolder.
description: Elimina una contactFolder que no sea la predeterminada.
ms.openlocfilehash: dd1ed79981051a1fbbc362e8f586281aa2659b57
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086933"
---
# <a name="delete-contactfolder"></a><span data-ttu-id="eaad8-103">Eliminar contactFolder.</span><span class="sxs-lookup"><span data-stu-id="eaad8-103">Delete contactFolder</span></span>

> <span data-ttu-id="eaad8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eaad8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eaad8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eaad8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eaad8-106">Elimina una contactFolder que no sea la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="eaad8-106">Delete contactFolder other than the default contactFolder.</span></span>
## <a name="permissions"></a><span data-ttu-id="eaad8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eaad8-107">Permissions</span></span>
<span data-ttu-id="eaad8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eaad8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eaad8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eaad8-110">Permission type</span></span>      | <span data-ttu-id="eaad8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eaad8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eaad8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eaad8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eaad8-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eaad8-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="eaad8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eaad8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eaad8-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eaad8-115">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="eaad8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eaad8-116">Application</span></span> | <span data-ttu-id="eaad8-117">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eaad8-117">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="eaad8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eaad8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/contactFolders/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="eaad8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eaad8-119">Request headers</span></span>
| <span data-ttu-id="eaad8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="eaad8-120">Name</span></span>       | <span data-ttu-id="eaad8-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="eaad8-121">Type</span></span> | <span data-ttu-id="eaad8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="eaad8-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="eaad8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="eaad8-123">Authorization</span></span>  | <span data-ttu-id="eaad8-124">string</span><span class="sxs-lookup"><span data-stu-id="eaad8-124">string</span></span>  | <span data-ttu-id="eaad8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eaad8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eaad8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eaad8-127">Request body</span></span>
<span data-ttu-id="eaad8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eaad8-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eaad8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaad8-129">Response</span></span>

<span data-ttu-id="eaad8-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaad8-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eaad8-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eaad8-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eaad8-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eaad8-133">Request</span></span>
<span data-ttu-id="eaad8-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaad8-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_contactfolder"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="eaad8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaad8-135">Response</span></span>
<span data-ttu-id="eaad8-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaad8-136">Here is an example of the response.</span></span> 
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
