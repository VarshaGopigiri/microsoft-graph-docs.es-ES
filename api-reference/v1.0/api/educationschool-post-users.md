---
title: Agregar educationUser a un educationSchool
description: Agregue un usuario a un centro educativo.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: d566d9231070cf57fad9f1908feecabc0657eae0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860273"
---
# <a name="add-educationuser-to-an-educationschool"></a><span data-ttu-id="a4577-103">Agregar educationUser a un educationSchool</span><span class="sxs-lookup"><span data-stu-id="a4577-103">Add educationUser to an educationSchool</span></span>

<span data-ttu-id="a4577-104">Agregue un usuario a un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a4577-104">Add a user to a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="a4577-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a4577-105">Permissions</span></span>
<span data-ttu-id="a4577-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4577-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a4577-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4577-108">Permission type</span></span>      | <span data-ttu-id="a4577-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4577-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a4577-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4577-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="a4577-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4577-111">Not supported.</span></span>  |
|<span data-ttu-id="a4577-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4577-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="a4577-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4577-113">Not supported.</span></span>  |
|<span data-ttu-id="a4577-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4577-114">Application</span></span> | <span data-ttu-id="a4577-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4577-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a4577-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4577-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/users/$ref
```
## <a name="request-headers"></a><span data-ttu-id="a4577-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4577-117">Request headers</span></span>
| <span data-ttu-id="a4577-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4577-118">Header</span></span>       | <span data-ttu-id="a4577-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a4577-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a4577-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4577-120">Authorization</span></span>  | <span data-ttu-id="a4577-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a4577-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a4577-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a4577-123">Content-Type</span></span>  | <span data-ttu-id="a4577-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a4577-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a4577-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4577-125">Request body</span></span>
<span data-ttu-id="a4577-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="a4577-126">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="a4577-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4577-127">Response</span></span>
<span data-ttu-id="a4577-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4577-128">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4577-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4577-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a4577-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4577-130">Request</span></span>
<span data-ttu-id="a4577-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4577-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationschool"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/schools/{id}/users/$ref
Content-type: application/json
Content-length: 56

{
  "@odata.id":"https://graph.microsoft.com/v1.0/education/users/14008"
}
```

##### <a name="response"></a><span data-ttu-id="a4577-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4577-132">Response</span></span>
<span data-ttu-id="a4577-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4577-133">The following is an example of the response.</span></span> 

<!-- Add the educationClass resource to the response. -->

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
