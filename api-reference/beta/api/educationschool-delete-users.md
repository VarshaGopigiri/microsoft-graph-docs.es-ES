---
title: Quitar educationUser de un educationSchool
description: Elimine un usuario de un centro educativo.
author: mmast-msft
ms.openlocfilehash: ce4a1f3d77d91cc31520f658788e788986923dbb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352692"
---
# <a name="remove-educationuser-from-an-educationschool"></a><span data-ttu-id="d7c7e-103">Quitar educationUser de un educationSchool</span><span class="sxs-lookup"><span data-stu-id="d7c7e-103">Remove educationUser from an educationSchool</span></span>

> <span data-ttu-id="d7c7e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7c7e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7c7e-106">Elimine un usuario de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-106">Delete a user from a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="d7c7e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7c7e-107">Permissions</span></span>
<span data-ttu-id="d7c7e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d7c7e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d7c7e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7c7e-110">Permission type</span></span>      | <span data-ttu-id="d7c7e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7c7e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d7c7e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7c7e-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="d7c7e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-113">Not supported.</span></span>  |
|<span data-ttu-id="d7c7e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7c7e-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="d7c7e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-115">Not supported.</span></span>  |
|<span data-ttu-id="d7c7e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7c7e-116">Application</span></span> | <span data-ttu-id="d7c7e-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7c7e-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="d7c7e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7c7e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/<id>/users/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="d7c7e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7c7e-119">Request headers</span></span>
| <span data-ttu-id="d7c7e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7c7e-120">Header</span></span>       | <span data-ttu-id="d7c7e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d7c7e-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d7c7e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d7c7e-122">Authorization</span></span>  | <span data-ttu-id="d7c7e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d7c7e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7c7e-125">Request body</span></span>
<span data-ttu-id="d7c7e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="d7c7e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7c7e-127">Response</span></span>
<span data-ttu-id="d7c7e-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-128">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="d7c7e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7c7e-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d7c7e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7c7e-130">Request</span></span>
<span data-ttu-id="d7c7e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/schools/10001/users/13006
```

##### <a name="response"></a><span data-ttu-id="d7c7e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7c7e-132">Response</span></span>
<span data-ttu-id="d7c7e-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7c7e-133">The following is an example of the response.</span></span> 
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