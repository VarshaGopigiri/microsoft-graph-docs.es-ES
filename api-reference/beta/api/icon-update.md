---
title: Update icon
description: Actualiza las propiedades del objeto icon.
ms.openlocfilehash: 5b9d049eb4d7bf3c596392c289738538799f8386
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089785"
---
# <a name="update-icon"></a><span data-ttu-id="742b3-103">Update icon</span><span class="sxs-lookup"><span data-stu-id="742b3-103">Update icon</span></span>

> <span data-ttu-id="742b3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="742b3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="742b3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="742b3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="742b3-106">Actualiza las propiedades del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="742b3-106">Update the properties of icon object.</span></span>
## <a name="permissions"></a><span data-ttu-id="742b3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="742b3-107">Permissions</span></span>
<span data-ttu-id="742b3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="742b3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="742b3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="742b3-110">Permission type</span></span>      | <span data-ttu-id="742b3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="742b3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="742b3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="742b3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="742b3-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="742b3-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="742b3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="742b3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="742b3-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="742b3-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="742b3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="742b3-116">Application</span></span> | <span data-ttu-id="742b3-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="742b3-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="742b3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="742b3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/sort/fields/icon
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-request-headers"></a><span data-ttu-id="742b3-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="742b3-119">Optional request headers</span></span>
| <span data-ttu-id="742b3-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="742b3-120">Name</span></span>       | <span data-ttu-id="742b3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="742b3-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="742b3-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="742b3-122">Authorization</span></span>  | <span data-ttu-id="742b3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="742b3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="742b3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="742b3-125">Request body</span></span>
<span data-ttu-id="742b3-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="742b3-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="742b3-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="742b3-129">Property</span></span>     | <span data-ttu-id="742b3-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="742b3-130">Type</span></span>   |<span data-ttu-id="742b3-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="742b3-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="742b3-132">index</span><span class="sxs-lookup"><span data-stu-id="742b3-132">index</span></span>|<span data-ttu-id="742b3-133">int</span><span class="sxs-lookup"><span data-stu-id="742b3-133">int</span></span>|<span data-ttu-id="742b3-134">Representa el índice del icono en el conjunto concreto.</span><span class="sxs-lookup"><span data-stu-id="742b3-134">Represents the index of the icon in the given set.</span></span>|
|<span data-ttu-id="742b3-135">set</span><span class="sxs-lookup"><span data-stu-id="742b3-135">set</span></span>|<span data-ttu-id="742b3-136">string</span><span class="sxs-lookup"><span data-stu-id="742b3-136">string</span></span>|<span data-ttu-id="742b3-p105">Representa el conjunto al que pertenece el icono. Valores posibles: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span><span class="sxs-lookup"><span data-stu-id="742b3-p105">Represents the set that the icon is part of. Possible values are: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span></span>|

## <a name="response"></a><span data-ttu-id="742b3-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="742b3-139">Response</span></span>

<span data-ttu-id="742b3-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Icon](../resources/icon.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="742b3-140">If successful, this method returns a `200 OK` response code and updated [Icon](../resources/icon.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="742b3-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="742b3-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="742b3-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="742b3-142">Request</span></span>
<span data-ttu-id="742b3-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="742b3-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_icon"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```
##### <a name="response"></a><span data-ttu-id="742b3-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="742b3-144">Response</span></span>
<span data-ttu-id="742b3-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="742b3-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.icon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->