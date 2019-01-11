---
title: Agregar un alumno
description: Agregue un miembro a una clase.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: f69d29a1726545c6c0a85af2200294cfc1d6fe00
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804527"
---
# <a name="add-a-student"></a><span data-ttu-id="5a984-103">Agregar un alumno</span><span class="sxs-lookup"><span data-stu-id="5a984-103">Add a student</span></span>

<span data-ttu-id="5a984-104">Agregue un miembro a una clase.</span><span class="sxs-lookup"><span data-stu-id="5a984-104">Add a member to a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="5a984-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5a984-105">Permissions</span></span>
<span data-ttu-id="5a984-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5a984-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5a984-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5a984-108">Permission type</span></span>      | <span data-ttu-id="5a984-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5a984-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5a984-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5a984-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="5a984-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a984-111">Not supported.</span></span>  |
|<span data-ttu-id="5a984-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5a984-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="5a984-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a984-113">Not supported.</span></span>  |
|<span data-ttu-id="5a984-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5a984-114">Application</span></span> | <span data-ttu-id="5a984-115">EduRoster.ReadWrite.All plus Member.Read.Hidden</span><span class="sxs-lookup"><span data-stu-id="5a984-115">EduRoster.ReadWrite.All plus Member.Read.Hidden</span></span> | 

## <a name="http-request"></a><span data-ttu-id="5a984-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a984-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="5a984-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a984-117">Request headers</span></span>
| <span data-ttu-id="5a984-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a984-118">Header</span></span>       | <span data-ttu-id="5a984-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5a984-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5a984-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5a984-120">Authorization</span></span>  | <span data-ttu-id="5a984-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5a984-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5a984-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5a984-123">Content-Type</span></span>  | <span data-ttu-id="5a984-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5a984-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5a984-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a984-125">Request body</span></span>
<span data-ttu-id="5a984-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="5a984-126">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="5a984-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a984-127">Response</span></span>
<span data-ttu-id="5a984-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a984-128">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5a984-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a984-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5a984-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a984-130">Request</span></span>
<span data-ttu-id="5a984-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a984-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationclass"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/classes/{class-id}/members/$ref
Content-type: application/json
Content-length: 56

{
  "@odata.id":"https://graph.microsoft.com/v1.0/education/users/13015"
}
```

##### <a name="response"></a><span data-ttu-id="5a984-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a984-132">Response</span></span>
<span data-ttu-id="5a984-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a984-133">The following is an example of the response.</span></span> 


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
