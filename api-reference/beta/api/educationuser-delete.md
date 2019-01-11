---
title: Eliminar educationUser
description: Elimine un usuario.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: bc6e27e3bfb9326b147ab1121b5c900d7878ff85
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866853"
---
# <a name="delete-educationuser"></a><span data-ttu-id="5c579-103">Eliminar educationUser</span><span class="sxs-lookup"><span data-stu-id="5c579-103">Delete educationUser</span></span>

> <span data-ttu-id="5c579-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5c579-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5c579-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5c579-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5c579-106">Elimine un usuario.</span><span class="sxs-lookup"><span data-stu-id="5c579-106">Delete a user.</span></span>


## <a name="permissions"></a><span data-ttu-id="5c579-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5c579-107">Permissions</span></span>
<span data-ttu-id="5c579-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5c579-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5c579-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c579-110">Permission type</span></span>      | <span data-ttu-id="5c579-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c579-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5c579-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c579-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="5c579-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c579-113">Not supported.</span></span>  |
|<span data-ttu-id="5c579-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c579-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="5c579-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c579-115">Not supported.</span></span>  |
|<span data-ttu-id="5c579-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c579-116">Application</span></span> | <span data-ttu-id="5c579-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5c579-117">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5c579-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c579-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="5c579-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c579-119">Request headers</span></span>
| <span data-ttu-id="5c579-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c579-120">Header</span></span>       | <span data-ttu-id="5c579-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5c579-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5c579-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5c579-122">Authorization</span></span>  | <span data-ttu-id="5c579-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5c579-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5c579-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5c579-125">Request body</span></span>
<span data-ttu-id="5c579-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5c579-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="5c579-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c579-127">Response</span></span>
<span data-ttu-id="5c579-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c579-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5c579-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c579-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5c579-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c579-131">Request</span></span>
<span data-ttu-id="5c579-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c579-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationuser"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/users/13019
```
##### <a name="response"></a><span data-ttu-id="5c579-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c579-133">Response</span></span>
<span data-ttu-id="5c579-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c579-134">The following is an example of the response.</span></span> 
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
