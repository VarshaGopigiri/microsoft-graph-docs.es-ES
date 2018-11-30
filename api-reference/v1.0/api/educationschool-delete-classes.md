---
title: Quitar educationClass
description: Elimine una clase de un centro educativo.
ms.openlocfilehash: 5103265bbb0c0f74def65c9adba9cc28dc41785b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031712"
---
# <a name="remove-educationclass"></a><span data-ttu-id="24d9d-103">Quitar educationClass</span><span class="sxs-lookup"><span data-stu-id="24d9d-103">Remove educationClass</span></span>

<span data-ttu-id="24d9d-104">Elimine una clase de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="24d9d-104">Delete a class from a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="24d9d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="24d9d-105">Permissions</span></span>
<span data-ttu-id="24d9d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="24d9d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="24d9d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="24d9d-108">Permission type</span></span>      | <span data-ttu-id="24d9d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="24d9d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="24d9d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="24d9d-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="24d9d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24d9d-111">Not supported.</span></span>  |
|<span data-ttu-id="24d9d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="24d9d-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="24d9d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24d9d-113">Not supported.</span></span>  |
|<span data-ttu-id="24d9d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="24d9d-114">Application</span></span> | <span data-ttu-id="24d9d-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24d9d-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="24d9d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="24d9d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/{id}/classes/{classId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="24d9d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="24d9d-117">Request headers</span></span>
| <span data-ttu-id="24d9d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24d9d-118">Header</span></span>       | <span data-ttu-id="24d9d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="24d9d-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="24d9d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="24d9d-120">Authorization</span></span>  | <span data-ttu-id="24d9d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="24d9d-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="24d9d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="24d9d-123">Request body</span></span>
<span data-ttu-id="24d9d-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="24d9d-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="24d9d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24d9d-125">Response</span></span>
<span data-ttu-id="24d9d-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24d9d-126">If successful, this method returns a `204 No Content` response code and a response body.</span></span>

## <a name="example"></a><span data-ttu-id="24d9d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="24d9d-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="24d9d-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="24d9d-128">Request</span></span>
<span data-ttu-id="24d9d-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="24d9d-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/schools/{school-id}/classes/{class-id}
```

##### <a name="response"></a><span data-ttu-id="24d9d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24d9d-130">Response</span></span>
<span data-ttu-id="24d9d-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24d9d-131">The following is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->