---
title: Eliminar educationSchool
description: Elimine un centro educativo.
author: mmast-msft
ms.openlocfilehash: 16c7edc747fe481fe10180f919a12c39dbfcd150
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303232"
---
# <a name="delete-educationschool"></a><span data-ttu-id="e4f66-103">Eliminar educationSchool</span><span class="sxs-lookup"><span data-stu-id="e4f66-103">Delete educationSchool</span></span>

<span data-ttu-id="e4f66-104">Elimine un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e4f66-104">Delete a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="e4f66-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4f66-105">Permissions</span></span>
<span data-ttu-id="e4f66-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4f66-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e4f66-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4f66-108">Permission type</span></span>      | <span data-ttu-id="e4f66-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4f66-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e4f66-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4f66-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="e4f66-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4f66-111">Not supported.</span></span>  |
|<span data-ttu-id="e4f66-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4f66-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e4f66-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4f66-113">Not supported.</span></span>  |
|<span data-ttu-id="e4f66-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4f66-114">Application</span></span> | <span data-ttu-id="e4f66-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4f66-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e4f66-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4f66-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e4f66-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4f66-117">Request headers</span></span>
| <span data-ttu-id="e4f66-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4f66-118">Header</span></span>       | <span data-ttu-id="e4f66-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e4f66-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e4f66-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e4f66-120">Authorization</span></span>  | <span data-ttu-id="e4f66-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4f66-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e4f66-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4f66-123">Request body</span></span>
<span data-ttu-id="e4f66-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e4f66-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="e4f66-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4f66-125">Response</span></span>
<span data-ttu-id="e4f66-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4f66-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e4f66-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4f66-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e4f66-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4f66-129">Request</span></span>
<span data-ttu-id="e4f66-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4f66-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/schools/{school-id}
```
##### <a name="response"></a><span data-ttu-id="e4f66-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4f66-131">Response</span></span>
<span data-ttu-id="e4f66-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4f66-132">The following is an example of the response.</span></span> 

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
  "description": "Delete educationSchool",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->