---
title: Agregar educationClass a educationSchool
description: Agregue una clase al centro educativo.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 3e09bd141c0b474d44ce9d691cff29b5164f8f34
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848583"
---
# <a name="add-educationclass-to-educationschool"></a><span data-ttu-id="1aeea-103">Agregar educationClass a educationSchool</span><span class="sxs-lookup"><span data-stu-id="1aeea-103">Add educationClass to educationSchool</span></span>

> <span data-ttu-id="1aeea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1aeea-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1aeea-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1aeea-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1aeea-106">Agregue una clase al centro educativo.</span><span class="sxs-lookup"><span data-stu-id="1aeea-106">Add a class to a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="1aeea-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1aeea-107">Permissions</span></span>
<span data-ttu-id="1aeea-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1aeea-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1aeea-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1aeea-110">Permission type</span></span>      | <span data-ttu-id="1aeea-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1aeea-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1aeea-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1aeea-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="1aeea-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1aeea-113">Not supported.</span></span>  |
|<span data-ttu-id="1aeea-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1aeea-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="1aeea-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1aeea-115">Not supported.</span></span>  |
|<span data-ttu-id="1aeea-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1aeea-116">Application</span></span> | <span data-ttu-id="1aeea-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1aeea-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1aeea-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1aeea-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/classes/$ref
```
## <a name="request-headers"></a><span data-ttu-id="1aeea-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1aeea-119">Request headers</span></span>
| <span data-ttu-id="1aeea-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1aeea-120">Header</span></span>       | <span data-ttu-id="1aeea-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1aeea-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1aeea-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1aeea-122">Authorization</span></span>  | <span data-ttu-id="1aeea-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1aeea-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="1aeea-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1aeea-125">Content-Type</span></span>  | <span data-ttu-id="1aeea-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1aeea-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1aeea-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1aeea-127">Request body</span></span>
<span data-ttu-id="1aeea-128">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationClass](../resources/educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="1aeea-128">In the request body, supply a JSON representation of an [educationClass](../resources/educationclass.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="1aeea-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1aeea-129">Response</span></span>
<span data-ttu-id="1aeea-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1aeea-130">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1aeea-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1aeea-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1aeea-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1aeea-132">Request</span></span>
<span data-ttu-id="1aeea-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1aeea-133">The following is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="1aeea-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1aeea-134">Response</span></span> 
<span data-ttu-id="1aeea-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1aeea-135">The following is an example of the response.</span></span> 

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
