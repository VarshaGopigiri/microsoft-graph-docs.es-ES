---
title: Update photo
description: Actualiza las propiedades del objeto photo.
ms.openlocfilehash: 0b062372ac12ec86f3035af276680310191818d9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029879"
---
# <a name="update-photo"></a><span data-ttu-id="207e9-103">Update photo</span><span class="sxs-lookup"><span data-stu-id="207e9-103">Update photo</span></span>

<span data-ttu-id="207e9-104">Actualiza las propiedades del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="207e9-104">Update the properties of photo object.</span></span>
## <a name="permissions"></a><span data-ttu-id="207e9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="207e9-105">Permissions</span></span>
<span data-ttu-id="207e9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="207e9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="207e9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="207e9-108">Permission type</span></span>      | <span data-ttu-id="207e9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="207e9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="207e9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="207e9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="207e9-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="207e9-111">Not supported.</span></span>    |
|<span data-ttu-id="207e9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="207e9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="207e9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="207e9-113">Not supported.</span></span>    |
|<span data-ttu-id="207e9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="207e9-114">Application</span></span> | <span data-ttu-id="207e9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="207e9-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="207e9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="207e9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}/photo
PATCH /groups/{id}/photo
PATCH /drive/root/createdByUser/photo
```

## <a name="request-headers"></a><span data-ttu-id="207e9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="207e9-117">Request headers</span></span>
| <span data-ttu-id="207e9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="207e9-118">Name</span></span>       | <span data-ttu-id="207e9-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="207e9-119">Type</span></span> | <span data-ttu-id="207e9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="207e9-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="207e9-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="207e9-121">Authorization</span></span>  | <span data-ttu-id="207e9-122">string</span><span class="sxs-lookup"><span data-stu-id="207e9-122">string</span></span>  | <span data-ttu-id="207e9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="207e9-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="207e9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="207e9-125">Request body</span></span>
<span data-ttu-id="207e9-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="207e9-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="207e9-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="207e9-129">Property</span></span>     | <span data-ttu-id="207e9-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="207e9-130">Type</span></span>   |<span data-ttu-id="207e9-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="207e9-131">Description</span></span>|
|:---------------|:--------|:----------|

## <a name="response"></a><span data-ttu-id="207e9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="207e9-132">Response</span></span>

<span data-ttu-id="207e9-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="207e9-133">If successful, this method returns a `200 OK` response code and updated [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="207e9-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="207e9-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="207e9-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="207e9-135">Request</span></span>
<span data-ttu-id="207e9-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="207e9-136">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="207e9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="207e9-137">Response</span></span>
<span data-ttu-id="207e9-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="207e9-138">Here is an example of the response.</span></span>
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
