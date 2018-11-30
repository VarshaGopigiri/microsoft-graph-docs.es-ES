---
title: Eliminar educationUser
description: Elimine un usuario.
ms.openlocfilehash: 9f0eba350026c45f0371c6de5c8db6e76fc71dfa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085307"
---
# <a name="delete-educationuser"></a><span data-ttu-id="4369c-103">Eliminar educationUser</span><span class="sxs-lookup"><span data-stu-id="4369c-103">Delete educationUser</span></span>

> <span data-ttu-id="4369c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4369c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4369c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4369c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4369c-106">Elimine un usuario.</span><span class="sxs-lookup"><span data-stu-id="4369c-106">Delete a user.</span></span>


## <a name="permissions"></a><span data-ttu-id="4369c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4369c-107">Permissions</span></span>
<span data-ttu-id="4369c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4369c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4369c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4369c-110">Permission type</span></span>      | <span data-ttu-id="4369c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4369c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4369c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4369c-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="4369c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4369c-113">Not supported.</span></span>  |
|<span data-ttu-id="4369c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4369c-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="4369c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4369c-115">Not supported.</span></span>  |
|<span data-ttu-id="4369c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4369c-116">Application</span></span> | <span data-ttu-id="4369c-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4369c-117">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4369c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4369c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="4369c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4369c-119">Request headers</span></span>
| <span data-ttu-id="4369c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4369c-120">Header</span></span>       | <span data-ttu-id="4369c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4369c-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4369c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="4369c-122">Authorization</span></span>  | <span data-ttu-id="4369c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4369c-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4369c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4369c-125">Request body</span></span>
<span data-ttu-id="4369c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4369c-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="4369c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4369c-127">Response</span></span>
<span data-ttu-id="4369c-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4369c-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4369c-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4369c-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4369c-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4369c-131">Request</span></span>
<span data-ttu-id="4369c-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4369c-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationuser"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/users/13019
```
##### <a name="response"></a><span data-ttu-id="4369c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4369c-133">Response</span></span>
<span data-ttu-id="4369c-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4369c-134">The following is an example of the response.</span></span> 
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
  "description": "Delete educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->