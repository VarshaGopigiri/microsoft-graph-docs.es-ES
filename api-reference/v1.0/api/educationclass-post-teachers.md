---
title: Agregar profesor
description: Agregue un profesor a una clase.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: a8c968890877ec07112510615b11010efb3779a1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987747"
---
# <a name="add-teacher"></a><span data-ttu-id="3bd4f-103">Agregar profesor</span><span class="sxs-lookup"><span data-stu-id="3bd4f-103">Add teacher</span></span>

<span data-ttu-id="3bd4f-104">Agregue un profesor a una clase.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-104">Add a teacher to a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="3bd4f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3bd4f-105">Permissions</span></span>
<span data-ttu-id="3bd4f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3bd4f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3bd4f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3bd4f-108">Permission type</span></span>      | <span data-ttu-id="3bd4f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3bd4f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3bd4f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3bd4f-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="3bd4f-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-111">Not supported.</span></span>  |
|<span data-ttu-id="3bd4f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3bd4f-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="3bd4f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-113">Not supported.</span></span>  |
|<span data-ttu-id="3bd4f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3bd4f-114">Application</span></span> | <span data-ttu-id="3bd4f-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3bd4f-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="3bd4f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3bd4f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/teachers/$ref
```
## <a name="request-headers"></a><span data-ttu-id="3bd4f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3bd4f-117">Request headers</span></span>
| <span data-ttu-id="3bd4f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bd4f-118">Header</span></span>       | <span data-ttu-id="3bd4f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3bd4f-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3bd4f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="3bd4f-120">Authorization</span></span>  | <span data-ttu-id="3bd4f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3bd4f-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3bd4f-123">Content-Type</span></span>  | <span data-ttu-id="3bd4f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3bd4f-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3bd4f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3bd4f-125">Request body</span></span>
<span data-ttu-id="3bd4f-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="3bd4f-126">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="3bd4f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bd4f-127">Response</span></span>
<span data-ttu-id="3bd4f-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-128">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3bd4f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bd4f-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3bd4f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3bd4f-130">Request</span></span>
<span data-ttu-id="3bd4f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationclass"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/classes/{class-id}/teachers/$ref
Content-type: application/json
Content-length: 508

{
  "@odata.id":"https://graph.microsoft.com/v1.0/education/users/14011"
}
```

##### <a name="response"></a><span data-ttu-id="3bd4f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bd4f-132">Response</span></span>
<span data-ttu-id="3bd4f-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-133">The following is an example of the response.</span></span> 

<!-- Add the educationClass object to the response -->

><span data-ttu-id="3bd4f-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
