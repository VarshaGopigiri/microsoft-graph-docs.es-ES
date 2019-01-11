---
title: Update photo
description: Actualiza las propiedades del objeto photo.
localization_priority: Normal
ms.openlocfilehash: 80c866eab74307d3001887110e050aa438cdde9f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883786"
---
# <a name="update-photo"></a><span data-ttu-id="79d87-103">Update photo</span><span class="sxs-lookup"><span data-stu-id="79d87-103">Update photo</span></span>

<span data-ttu-id="79d87-104">Actualiza las propiedades del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="79d87-104">Update the properties of photo object.</span></span>
## <a name="permissions"></a><span data-ttu-id="79d87-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="79d87-105">Permissions</span></span>
<span data-ttu-id="79d87-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="79d87-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="79d87-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79d87-108">Permission type</span></span>      | <span data-ttu-id="79d87-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79d87-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79d87-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79d87-110">Delegated (work or school account)</span></span> | <span data-ttu-id="79d87-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79d87-111">Not supported.</span></span>    |
|<span data-ttu-id="79d87-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79d87-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79d87-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79d87-113">Not supported.</span></span>    |
|<span data-ttu-id="79d87-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79d87-114">Application</span></span> | <span data-ttu-id="79d87-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79d87-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="79d87-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79d87-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}/photo
PATCH /groups/{id}/photo
PATCH /drive/root/createdByUser/photo
```

## <a name="request-headers"></a><span data-ttu-id="79d87-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79d87-117">Request headers</span></span>
| <span data-ttu-id="79d87-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="79d87-118">Name</span></span>       | <span data-ttu-id="79d87-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="79d87-119">Type</span></span> | <span data-ttu-id="79d87-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="79d87-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="79d87-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="79d87-121">Authorization</span></span>  | <span data-ttu-id="79d87-122">string</span><span class="sxs-lookup"><span data-stu-id="79d87-122">string</span></span>  | <span data-ttu-id="79d87-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79d87-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="79d87-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79d87-125">Request body</span></span>
<span data-ttu-id="79d87-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="79d87-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="79d87-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="79d87-129">Property</span></span>     | <span data-ttu-id="79d87-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="79d87-130">Type</span></span>   |<span data-ttu-id="79d87-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="79d87-131">Description</span></span>|
|:---------------|:--------|:----------|

## <a name="response"></a><span data-ttu-id="79d87-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79d87-132">Response</span></span>

<span data-ttu-id="79d87-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79d87-133">If successful, this method returns a `200 OK` response code and updated [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="79d87-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79d87-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="79d87-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79d87-135">Request</span></span>
<span data-ttu-id="79d87-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79d87-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_photo"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```
##### <a name="response"></a><span data-ttu-id="79d87-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79d87-137">Response</span></span>
<span data-ttu-id="79d87-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79d87-138">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
