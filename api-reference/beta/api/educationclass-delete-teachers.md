---
title: Quitar profesor
description: Quite un profesor de una clase.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 39a9df74ea6f816b179844f6c26218a0caa17210
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965120"
---
# <a name="remove-teacher"></a><span data-ttu-id="2e1b9-103">Quitar profesor</span><span class="sxs-lookup"><span data-stu-id="2e1b9-103">Remove teacher</span></span>

> <span data-ttu-id="2e1b9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2e1b9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2e1b9-106">Quite un profesor de una clase.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-106">Remove a teacher from a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="2e1b9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2e1b9-107">Permissions</span></span>
<span data-ttu-id="2e1b9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2e1b9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2e1b9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2e1b9-110">Permission type</span></span>      | <span data-ttu-id="2e1b9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2e1b9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2e1b9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2e1b9-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="2e1b9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-113">Not supported.</span></span>  |
|<span data-ttu-id="2e1b9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2e1b9-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="2e1b9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-115">Not supported.</span></span>  |
|<span data-ttu-id="2e1b9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2e1b9-116">Application</span></span> | <span data-ttu-id="2e1b9-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e1b9-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2e1b9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e1b9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/teachers/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="2e1b9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e1b9-119">Request headers</span></span>
| <span data-ttu-id="2e1b9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e1b9-120">Header</span></span>       | <span data-ttu-id="2e1b9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2e1b9-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2e1b9-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2e1b9-122">Authorization</span></span>  | <span data-ttu-id="2e1b9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2e1b9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2e1b9-125">Request body</span></span>
<span data-ttu-id="2e1b9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="2e1b9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e1b9-127">Response</span></span>
<span data-ttu-id="2e1b9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-128">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e1b9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e1b9-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2e1b9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e1b9-130">Request</span></span>
<span data-ttu-id="2e1b9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/<id>/teachers/14012
```

##### <a name="response"></a><span data-ttu-id="2e1b9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e1b9-132">Response</span></span>
<span data-ttu-id="2e1b9-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e1b9-133">The following is an example of the response.</span></span> 
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
