---
title: Quitar educationClass
description: Elimine una clase de un centro educativo.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 3cf61d77171e7dc3161aa3b3cc48d663de784649
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950952"
---
# <a name="remove-educationclass"></a><span data-ttu-id="9a532-103">Quitar educationClass</span><span class="sxs-lookup"><span data-stu-id="9a532-103">Remove educationClass</span></span>

<span data-ttu-id="9a532-104">Elimine una clase de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="9a532-104">Delete a class from a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="9a532-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a532-105">Permissions</span></span>
<span data-ttu-id="9a532-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9a532-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9a532-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a532-108">Permission type</span></span>      | <span data-ttu-id="9a532-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a532-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9a532-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a532-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="9a532-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a532-111">Not supported.</span></span>  |
|<span data-ttu-id="9a532-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a532-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9a532-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a532-113">Not supported.</span></span>  |
|<span data-ttu-id="9a532-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a532-114">Application</span></span> | <span data-ttu-id="9a532-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9a532-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9a532-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a532-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/{id}/classes/{classId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="9a532-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a532-117">Request headers</span></span>
| <span data-ttu-id="9a532-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a532-118">Header</span></span>       | <span data-ttu-id="9a532-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9a532-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9a532-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a532-120">Authorization</span></span>  | <span data-ttu-id="9a532-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a532-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9a532-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a532-123">Request body</span></span>
<span data-ttu-id="9a532-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9a532-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="9a532-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a532-125">Response</span></span>
<span data-ttu-id="9a532-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a532-126">If successful, this method returns a `204 No Content` response code and a response body.</span></span>

## <a name="example"></a><span data-ttu-id="9a532-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a532-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9a532-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a532-128">Request</span></span>
<span data-ttu-id="9a532-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a532-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/schools/{school-id}/classes/{class-id}
```

##### <a name="response"></a><span data-ttu-id="9a532-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a532-130">Response</span></span>
<span data-ttu-id="9a532-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a532-131">The following is an example of the response.</span></span> 

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
