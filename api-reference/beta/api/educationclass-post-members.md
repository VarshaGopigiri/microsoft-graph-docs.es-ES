---
title: Agregar un alumno
description: Agregue un miembro a una clase.
ms.openlocfilehash: 0b748a924de1f882372c0117f94d0de06f64dbc9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084019"
---
# <a name="add-a-student"></a><span data-ttu-id="6a9f8-103">Agregar un alumno</span><span class="sxs-lookup"><span data-stu-id="6a9f8-103">Add a student</span></span>

> <span data-ttu-id="6a9f8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6a9f8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6a9f8-106">Agregue un miembro a una clase.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-106">Add a member to a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="6a9f8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6a9f8-107">Permissions</span></span>
<span data-ttu-id="6a9f8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6a9f8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6a9f8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6a9f8-110">Permission type</span></span>      | <span data-ttu-id="6a9f8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6a9f8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6a9f8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6a9f8-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="6a9f8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-113">Not supported.</span></span>  |
|<span data-ttu-id="6a9f8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6a9f8-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="6a9f8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-115">Not supported.</span></span>  |
|<span data-ttu-id="6a9f8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6a9f8-116">Application</span></span> | <span data-ttu-id="6a9f8-117">EduRoster.ReadWrite.All plus Member.Read.Hidden</span><span class="sxs-lookup"><span data-stu-id="6a9f8-117">EduRoster.ReadWrite.All plus Member.Read.Hidden</span></span> | 

## <a name="http-request"></a><span data-ttu-id="6a9f8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6a9f8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="6a9f8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6a9f8-119">Request headers</span></span>
| <span data-ttu-id="6a9f8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a9f8-120">Header</span></span>       | <span data-ttu-id="6a9f8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6a9f8-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6a9f8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="6a9f8-122">Authorization</span></span>  | <span data-ttu-id="6a9f8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="6a9f8-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6a9f8-125">Content-Type</span></span>  | <span data-ttu-id="6a9f8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6a9f8-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6a9f8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6a9f8-127">Request body</span></span>
<span data-ttu-id="6a9f8-128">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="6a9f8-128">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="6a9f8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a9f8-129">Response</span></span>
<span data-ttu-id="6a9f8-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-130">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6a9f8-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6a9f8-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6a9f8-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6a9f8-132">Request</span></span>
<span data-ttu-id="6a9f8-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationclass"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11011/members/$ref
Content-type: application/json
Content-length: 56

{
  "@odata.id":"https://graph.microsoft.com/beta/education/users/13015"
}
```

##### <a name="response"></a><span data-ttu-id="6a9f8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a9f8-134">Response</span></span>
<span data-ttu-id="6a9f8-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-135">The following is an example of the response.</span></span> 


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