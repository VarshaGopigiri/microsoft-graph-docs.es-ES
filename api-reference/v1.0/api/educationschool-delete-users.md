---
title: Quitar educationUser de un educationSchool
description: Elimine un usuario de un centro educativo.
ms.openlocfilehash: dbc58a0cde4406fb28323bedf02a1902998e9b0d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031031"
---
# <a name="remove-educationuser-from-an-educationschool"></a><span data-ttu-id="6e410-103">Quitar educationUser de un educationSchool</span><span class="sxs-lookup"><span data-stu-id="6e410-103">Remove educationUser from an educationSchool</span></span>

<span data-ttu-id="6e410-104">Elimine un usuario de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="6e410-104">Delete a user from a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="6e410-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6e410-105">Permissions</span></span>
<span data-ttu-id="6e410-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e410-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e410-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e410-108">Permission type</span></span>      | <span data-ttu-id="6e410-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e410-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6e410-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e410-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="6e410-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e410-111">Not supported.</span></span>  |
|<span data-ttu-id="6e410-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e410-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="6e410-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e410-113">Not supported.</span></span>  |
|<span data-ttu-id="6e410-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e410-114">Application</span></span> | <span data-ttu-id="6e410-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e410-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="6e410-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e410-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/{id}/users/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="6e410-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e410-117">Request headers</span></span>
| <span data-ttu-id="6e410-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e410-118">Header</span></span>       | <span data-ttu-id="6e410-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6e410-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6e410-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e410-120">Authorization</span></span>  | <span data-ttu-id="6e410-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e410-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6e410-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e410-123">Request body</span></span>
<span data-ttu-id="6e410-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6e410-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="6e410-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e410-125">Response</span></span>
<span data-ttu-id="6e410-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="6e410-126">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="6e410-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e410-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6e410-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e410-128">Request</span></span>
<span data-ttu-id="6e410-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e410-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/schools/{school-id}/users/{user-id}
```

##### <a name="response"></a><span data-ttu-id="6e410-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e410-130">Response</span></span>
<span data-ttu-id="6e410-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e410-131">The following is an example of the response.</span></span> 
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