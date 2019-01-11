---
title: Update photo
description: Actualiza las propiedades del objeto photo.
localization_priority: Normal
ms.openlocfilehash: 56a8d892ae92f92f5103dc3d88a2f95a5bbb262b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818385"
---
# <a name="update-photo"></a><span data-ttu-id="43248-103">Update photo</span><span class="sxs-lookup"><span data-stu-id="43248-103">Update photo</span></span>

> <span data-ttu-id="43248-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="43248-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="43248-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="43248-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="43248-106">Actualiza las propiedades del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="43248-106">Update the properties of photo object.</span></span>
## <a name="permissions"></a><span data-ttu-id="43248-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="43248-107">Permissions</span></span>
<span data-ttu-id="43248-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43248-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43248-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43248-110">Permission type</span></span>      | <span data-ttu-id="43248-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43248-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="43248-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43248-112">Delegated (work or school account)</span></span> | <span data-ttu-id="43248-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43248-113">Not supported.</span></span>    |
|<span data-ttu-id="43248-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43248-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43248-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43248-115">Not supported.</span></span>    |
|<span data-ttu-id="43248-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43248-116">Application</span></span> | <span data-ttu-id="43248-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43248-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="43248-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43248-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}/photo
PATCH /groups/{id}/photo
PATCH /drive/root/createdByUser/photo
```

## <a name="request-headers"></a><span data-ttu-id="43248-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43248-119">Request headers</span></span>
| <span data-ttu-id="43248-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="43248-120">Name</span></span>       | <span data-ttu-id="43248-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="43248-121">Type</span></span> | <span data-ttu-id="43248-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="43248-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="43248-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="43248-123">Authorization</span></span>  | <span data-ttu-id="43248-124">string</span><span class="sxs-lookup"><span data-stu-id="43248-124">string</span></span>  | <span data-ttu-id="43248-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43248-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="43248-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43248-127">Request body</span></span>
<span data-ttu-id="43248-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="43248-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="43248-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43248-131">Property</span></span>     | <span data-ttu-id="43248-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="43248-132">Type</span></span>   |<span data-ttu-id="43248-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="43248-133">Description</span></span>|
|:---------------|:--------|:----------|

## <a name="response"></a><span data-ttu-id="43248-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43248-134">Response</span></span>

<span data-ttu-id="43248-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43248-135">If successful, this method returns a `200 OK` response code and updated [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="43248-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43248-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="43248-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43248-137">Request</span></span>
<span data-ttu-id="43248-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43248-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_photo"
}-->
```http
PATCH https://graph.microsoft.com/beta/users/{id|userPrincipalName}/photo
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```
##### <a name="response"></a><span data-ttu-id="43248-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43248-139">Response</span></span>
<span data-ttu-id="43248-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43248-140">Here is an example of the response.</span></span>
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
