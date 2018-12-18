---
title: Agregar educationClass a educationSchool
description: Agregue una clase al centro educativo.
author: mmast-msft
ms.openlocfilehash: d5b32f1fabe40383f4c9d8dac79b52f85d9af4b0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303132"
---
# <a name="add-educationclass-to-educationschool"></a><span data-ttu-id="909ed-103">Agregar educationClass a educationSchool</span><span class="sxs-lookup"><span data-stu-id="909ed-103">Add educationClass to educationSchool</span></span>

<span data-ttu-id="909ed-104">Agregue una clase al centro educativo.</span><span class="sxs-lookup"><span data-stu-id="909ed-104">Add a class to a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="909ed-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="909ed-105">Permissions</span></span>
<span data-ttu-id="909ed-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="909ed-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="909ed-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="909ed-108">Permission type</span></span>      | <span data-ttu-id="909ed-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="909ed-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="909ed-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="909ed-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="909ed-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="909ed-111">Not supported.</span></span>  |
|<span data-ttu-id="909ed-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="909ed-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="909ed-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="909ed-113">Not supported.</span></span>  |
|<span data-ttu-id="909ed-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="909ed-114">Application</span></span> | <span data-ttu-id="909ed-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="909ed-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="909ed-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="909ed-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/classes/$ref
```
## <a name="request-headers"></a><span data-ttu-id="909ed-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="909ed-117">Request headers</span></span>
| <span data-ttu-id="909ed-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="909ed-118">Header</span></span>       | <span data-ttu-id="909ed-119">Valor</span><span class="sxs-lookup"><span data-stu-id="909ed-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="909ed-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="909ed-120">Authorization</span></span>  | <span data-ttu-id="909ed-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="909ed-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="909ed-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="909ed-123">Content-Type</span></span>  | <span data-ttu-id="909ed-124">application/json</span><span class="sxs-lookup"><span data-stu-id="909ed-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="909ed-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="909ed-125">Request body</span></span>
<span data-ttu-id="909ed-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationClass](../resources/educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="909ed-126">In the request body, supply a JSON representation of an [educationClass](../resources/educationclass.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="909ed-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="909ed-127">Response</span></span>
<span data-ttu-id="909ed-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="909ed-128">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="909ed-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="909ed-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="909ed-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="909ed-130">Request</span></span>
<span data-ttu-id="909ed-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="909ed-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/schools/{school-id}/classes/$ref
Content-type: application/json
Content-length: 224

{
 "@odata.id":"https://graph.microsoft.com/v1.0/education/classes/11006"
}
```

##### <a name="response"></a><span data-ttu-id="909ed-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="909ed-132">Response</span></span> 
<span data-ttu-id="909ed-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="909ed-133">The following is an example of the response.</span></span> 

<!-- Add the educationClass resource to the response. -->

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