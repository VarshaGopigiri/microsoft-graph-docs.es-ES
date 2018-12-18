---
title: Agregar educationUser a un educationSchool
description: Agregue un usuario a un centro educativo.
author: mmast-msft
ms.openlocfilehash: d7cabee054eddb6ac83bfdee5b0dea1ea25f9f36
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323082"
---
# <a name="add-educationuser-to-an-educationschool"></a><span data-ttu-id="5b083-103">Agregar educationUser a un educationSchool</span><span class="sxs-lookup"><span data-stu-id="5b083-103">Add educationUser to an educationSchool</span></span>

<span data-ttu-id="5b083-104">Agregue un usuario a un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="5b083-104">Add a user to a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="5b083-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5b083-105">Permissions</span></span>
<span data-ttu-id="5b083-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5b083-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5b083-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5b083-108">Permission type</span></span>      | <span data-ttu-id="5b083-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5b083-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5b083-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5b083-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="5b083-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b083-111">Not supported.</span></span>  |
|<span data-ttu-id="5b083-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5b083-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="5b083-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b083-113">Not supported.</span></span>  |
|<span data-ttu-id="5b083-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5b083-114">Application</span></span> | <span data-ttu-id="5b083-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5b083-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="5b083-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5b083-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/users/$ref
```
## <a name="request-headers"></a><span data-ttu-id="5b083-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5b083-117">Request headers</span></span>
| <span data-ttu-id="5b083-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b083-118">Header</span></span>       | <span data-ttu-id="5b083-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5b083-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5b083-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5b083-120">Authorization</span></span>  | <span data-ttu-id="5b083-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5b083-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5b083-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5b083-123">Content-Type</span></span>  | <span data-ttu-id="5b083-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5b083-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5b083-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5b083-125">Request body</span></span>
<span data-ttu-id="5b083-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="5b083-126">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="5b083-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b083-127">Response</span></span>
<span data-ttu-id="5b083-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b083-128">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5b083-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b083-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5b083-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5b083-130">Request</span></span>
<span data-ttu-id="5b083-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5b083-131">The following is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="5b083-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b083-132">Response</span></span>
<span data-ttu-id="5b083-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b083-133">The following is an example of the response.</span></span> 

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