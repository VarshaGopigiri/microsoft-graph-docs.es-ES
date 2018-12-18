---
title: Quitar educationClass
description: Elimine una clase de un centro educativo.
author: mmast-msft
ms.openlocfilehash: 6f917946e0fc24a34c5560e5b01a2bd4acca030d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331580"
---
# <a name="remove-educationclass"></a><span data-ttu-id="e13ae-103">Quitar educationClass</span><span class="sxs-lookup"><span data-stu-id="e13ae-103">Remove educationClass</span></span>

<span data-ttu-id="e13ae-104">Elimine una clase de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e13ae-104">Delete a class from a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="e13ae-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e13ae-105">Permissions</span></span>
<span data-ttu-id="e13ae-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e13ae-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e13ae-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e13ae-108">Permission type</span></span>      | <span data-ttu-id="e13ae-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e13ae-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e13ae-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e13ae-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="e13ae-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e13ae-111">Not supported.</span></span>  |
|<span data-ttu-id="e13ae-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e13ae-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e13ae-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e13ae-113">Not supported.</span></span>  |
|<span data-ttu-id="e13ae-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e13ae-114">Application</span></span> | <span data-ttu-id="e13ae-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e13ae-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e13ae-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e13ae-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/{id}/classes/{classId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="e13ae-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e13ae-117">Request headers</span></span>
| <span data-ttu-id="e13ae-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e13ae-118">Header</span></span>       | <span data-ttu-id="e13ae-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e13ae-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e13ae-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e13ae-120">Authorization</span></span>  | <span data-ttu-id="e13ae-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e13ae-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e13ae-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e13ae-123">Request body</span></span>
<span data-ttu-id="e13ae-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e13ae-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="e13ae-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e13ae-125">Response</span></span>
<span data-ttu-id="e13ae-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e13ae-126">If successful, this method returns a `204 No Content` response code and a response body.</span></span>

## <a name="example"></a><span data-ttu-id="e13ae-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e13ae-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e13ae-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e13ae-128">Request</span></span>
<span data-ttu-id="e13ae-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e13ae-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/schools/{school-id}/classes/{class-id}
```

##### <a name="response"></a><span data-ttu-id="e13ae-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e13ae-130">Response</span></span>
<span data-ttu-id="e13ae-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e13ae-131">The following is an example of the response.</span></span> 

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