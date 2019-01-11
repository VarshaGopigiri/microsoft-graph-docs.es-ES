---
title: Eliminar educationSchool
description: Elimine un centro educativo.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 691bd8090a15a5fc31960c5ac33ba5acabadbeb0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892494"
---
# <a name="delete-educationschool"></a><span data-ttu-id="c49f2-103">Eliminar educationSchool</span><span class="sxs-lookup"><span data-stu-id="c49f2-103">Delete educationSchool</span></span>

> <span data-ttu-id="c49f2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c49f2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c49f2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c49f2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c49f2-106">Elimine un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c49f2-106">Delete a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="c49f2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c49f2-107">Permissions</span></span>
<span data-ttu-id="c49f2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c49f2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c49f2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c49f2-110">Permission type</span></span>      | <span data-ttu-id="c49f2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c49f2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c49f2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c49f2-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="c49f2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c49f2-113">Not supported.</span></span>  |
|<span data-ttu-id="c49f2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c49f2-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="c49f2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c49f2-115">Not supported.</span></span>  |
|<span data-ttu-id="c49f2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c49f2-116">Application</span></span> | <span data-ttu-id="c49f2-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c49f2-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="c49f2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c49f2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c49f2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c49f2-119">Request headers</span></span>
| <span data-ttu-id="c49f2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c49f2-120">Header</span></span>       | <span data-ttu-id="c49f2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c49f2-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c49f2-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c49f2-122">Authorization</span></span>  | <span data-ttu-id="c49f2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c49f2-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c49f2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c49f2-125">Request body</span></span>
<span data-ttu-id="c49f2-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c49f2-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="c49f2-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c49f2-127">Response</span></span>
<span data-ttu-id="c49f2-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c49f2-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c49f2-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c49f2-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c49f2-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c49f2-131">Request</span></span>
<span data-ttu-id="c49f2-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c49f2-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/schools/10002
```
##### <a name="response"></a><span data-ttu-id="c49f2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c49f2-133">Response</span></span>
<span data-ttu-id="c49f2-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c49f2-134">The following is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete educationSchool",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
