---
title: Agregar educationClass a educationSchool
description: Agregue una clase al centro educativo.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 0ee3d1ba1a0b0da143ab3dbab5624d0ebb3de4ac
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926214"
---
# <a name="add-educationclass-to-educationschool"></a><span data-ttu-id="53894-103">Agregar educationClass a educationSchool</span><span class="sxs-lookup"><span data-stu-id="53894-103">Add educationClass to educationSchool</span></span>

> <span data-ttu-id="53894-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53894-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53894-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53894-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53894-106">Agregue una clase al centro educativo.</span><span class="sxs-lookup"><span data-stu-id="53894-106">Add a class to a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="53894-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="53894-107">Permissions</span></span>
<span data-ttu-id="53894-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53894-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53894-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53894-110">Permission type</span></span>      | <span data-ttu-id="53894-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53894-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="53894-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53894-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="53894-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53894-113">Not supported.</span></span>  |
|<span data-ttu-id="53894-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53894-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="53894-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53894-115">Not supported.</span></span>  |
|<span data-ttu-id="53894-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53894-116">Application</span></span> | <span data-ttu-id="53894-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53894-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="53894-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53894-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/classes/$ref
```
## <a name="request-headers"></a><span data-ttu-id="53894-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53894-119">Request headers</span></span>
| <span data-ttu-id="53894-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53894-120">Header</span></span>       | <span data-ttu-id="53894-121">Valor</span><span class="sxs-lookup"><span data-stu-id="53894-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="53894-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="53894-122">Authorization</span></span>  | <span data-ttu-id="53894-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53894-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="53894-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="53894-125">Content-Type</span></span>  | <span data-ttu-id="53894-126">application/json</span><span class="sxs-lookup"><span data-stu-id="53894-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="53894-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53894-127">Request body</span></span>
<span data-ttu-id="53894-128">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationClass](../resources/educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="53894-128">In the request body, supply a JSON representation of an [educationClass](../resources/educationclass.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="53894-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53894-129">Response</span></span>
<span data-ttu-id="53894-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53894-130">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53894-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53894-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="53894-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53894-132">Request</span></span>
<span data-ttu-id="53894-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53894-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
POST https://graph.microsoft.com/beta/education/schools/10002/classes/$ref
Content-type: application/json
Content-length: 224

{
 "@odata.id":"https://graph.microsoft.com/beta/education/classes/11006"
}
```

##### <a name="response"></a><span data-ttu-id="53894-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53894-134">Response</span></span> 
<span data-ttu-id="53894-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53894-135">The following is an example of the response.</span></span> 

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
