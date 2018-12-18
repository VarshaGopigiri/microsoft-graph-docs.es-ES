---
title: Agregar educationUser a un educationSchool
description: Agregue un usuario a un centro educativo.
author: mmast-msft
ms.openlocfilehash: 4c77a94b7b1c9af11d954a4ab903c597eded6a04
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352734"
---
# <a name="add-educationuser-to-an-educationschool"></a><span data-ttu-id="b7d31-103">Agregar educationUser a un educationSchool</span><span class="sxs-lookup"><span data-stu-id="b7d31-103">Add educationUser to an educationSchool</span></span>

> <span data-ttu-id="b7d31-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b7d31-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b7d31-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b7d31-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b7d31-106">Agregue un usuario a un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="b7d31-106">Add a user to a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="b7d31-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7d31-107">Permissions</span></span>
<span data-ttu-id="b7d31-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7d31-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7d31-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7d31-110">Permission type</span></span>      | <span data-ttu-id="b7d31-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7d31-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b7d31-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7d31-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="b7d31-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7d31-113">Not supported.</span></span>  |
|<span data-ttu-id="b7d31-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7d31-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="b7d31-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7d31-115">Not supported.</span></span>  |
|<span data-ttu-id="b7d31-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7d31-116">Application</span></span> | <span data-ttu-id="b7d31-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b7d31-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="b7d31-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7d31-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/users/$ref
```
## <a name="request-headers"></a><span data-ttu-id="b7d31-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7d31-119">Request headers</span></span>
| <span data-ttu-id="b7d31-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7d31-120">Header</span></span>       | <span data-ttu-id="b7d31-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b7d31-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b7d31-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b7d31-122">Authorization</span></span>  | <span data-ttu-id="b7d31-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7d31-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b7d31-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b7d31-125">Content-Type</span></span>  | <span data-ttu-id="b7d31-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b7d31-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b7d31-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7d31-127">Request body</span></span>
<span data-ttu-id="b7d31-128">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="b7d31-128">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="b7d31-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7d31-129">Response</span></span>
<span data-ttu-id="b7d31-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7d31-130">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b7d31-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7d31-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b7d31-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7d31-132">Request</span></span>
<span data-ttu-id="b7d31-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7d31-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationschool"
}-->
```http
POST https://graph.microsoft.com/beta/education/schools/<id>/users/$ref
Content-type: application/json
Content-length: 56

{
  "@odata.id":"https://graph.microsoft.com/beta/education/users/14008"
}
```

##### <a name="response"></a><span data-ttu-id="b7d31-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7d31-134">Response</span></span>
<span data-ttu-id="b7d31-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7d31-135">The following is an example of the response.</span></span> 

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