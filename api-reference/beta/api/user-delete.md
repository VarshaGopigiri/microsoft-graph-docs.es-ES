---
title: Eliminar un usuario
description: Elimina usuario.
author: dkershaw10
ms.openlocfilehash: d6f1a09e02fd054767a3e54050b9b0a9cb0042a7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320590"
---
# <a name="delete-a-user"></a><span data-ttu-id="61727-103">Eliminar un usuario</span><span class="sxs-lookup"><span data-stu-id="61727-103">Delete a user</span></span>

> <span data-ttu-id="61727-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="61727-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="61727-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="61727-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="61727-106">Elimina usuario.</span><span class="sxs-lookup"><span data-stu-id="61727-106">Delete user.</span></span>
## <a name="permissions"></a><span data-ttu-id="61727-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="61727-107">Permissions</span></span>
<span data-ttu-id="61727-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="61727-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="61727-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61727-110">Permission type</span></span>      | <span data-ttu-id="61727-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61727-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="61727-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61727-112">Delegated (work or school account)</span></span> | <span data-ttu-id="61727-113">User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="61727-113">User.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="61727-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61727-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="61727-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61727-115">Not supported.</span></span>    |
|<span data-ttu-id="61727-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61727-116">Application</span></span> | <span data-ttu-id="61727-117">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61727-117">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="61727-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61727-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}
```

## <a name="request-headers"></a><span data-ttu-id="61727-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61727-119">Request headers</span></span>
| <span data-ttu-id="61727-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61727-120">Header</span></span>       | <span data-ttu-id="61727-121">Valor</span><span class="sxs-lookup"><span data-stu-id="61727-121">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="61727-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="61727-122">Authorization</span></span>  | <span data-ttu-id="61727-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="61727-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="61727-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="61727-125">Request body</span></span>
<span data-ttu-id="61727-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="61727-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="61727-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61727-127">Response</span></span>

<span data-ttu-id="61727-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61727-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61727-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61727-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="61727-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="61727-131">Request</span></span>
<span data-ttu-id="61727-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61727-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_user"
}-->
```http
DELETE https://graph.microsoft.com/beta/users/ba9a3254-9f18-4209-aeb3-9e42a35b5be4 
```
##### <a name="response"></a><span data-ttu-id="61727-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61727-133">Response</span></span>
<span data-ttu-id="61727-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61727-134">Here is an example of the response.</span></span> 
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
  "description": "Delete user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->