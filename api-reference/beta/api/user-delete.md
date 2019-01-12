---
title: Eliminar un usuario
description: Elimina usuario.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e9a840f83c2bb8806464473ead09deffb30c5a9a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969432"
---
# <a name="delete-a-user"></a><span data-ttu-id="add60-103">Eliminar un usuario</span><span class="sxs-lookup"><span data-stu-id="add60-103">Delete a user</span></span>

> <span data-ttu-id="add60-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="add60-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="add60-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="add60-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="add60-106">Elimina usuario.</span><span class="sxs-lookup"><span data-stu-id="add60-106">Delete user.</span></span>
## <a name="permissions"></a><span data-ttu-id="add60-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="add60-107">Permissions</span></span>
<span data-ttu-id="add60-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="add60-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="add60-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="add60-110">Permission type</span></span>      | <span data-ttu-id="add60-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="add60-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="add60-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="add60-112">Delegated (work or school account)</span></span> | <span data-ttu-id="add60-113">User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="add60-113">User.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="add60-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="add60-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="add60-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="add60-115">Not supported.</span></span>    |
|<span data-ttu-id="add60-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="add60-116">Application</span></span> | <span data-ttu-id="add60-117">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="add60-117">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="add60-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="add60-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}
```

## <a name="request-headers"></a><span data-ttu-id="add60-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="add60-119">Request headers</span></span>
| <span data-ttu-id="add60-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="add60-120">Header</span></span>       | <span data-ttu-id="add60-121">Valor</span><span class="sxs-lookup"><span data-stu-id="add60-121">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="add60-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="add60-122">Authorization</span></span>  | <span data-ttu-id="add60-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="add60-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="add60-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="add60-125">Request body</span></span>
<span data-ttu-id="add60-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="add60-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="add60-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="add60-127">Response</span></span>

<span data-ttu-id="add60-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="add60-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="add60-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="add60-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="add60-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="add60-131">Request</span></span>
<span data-ttu-id="add60-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="add60-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_user"
}-->
```http
DELETE https://graph.microsoft.com/beta/users/ba9a3254-9f18-4209-aeb3-9e42a35b5be4 
```
##### <a name="response"></a><span data-ttu-id="add60-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="add60-133">Response</span></span>
<span data-ttu-id="add60-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="add60-134">Here is an example of the response.</span></span> 
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
