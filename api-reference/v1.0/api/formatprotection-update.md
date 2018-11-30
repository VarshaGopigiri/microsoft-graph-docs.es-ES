---
title: Update formatprotection
description: Actualiza las propiedades del objeto formatprotection.
ms.openlocfilehash: 691715a921ae98f725f26566fb144530f27330b9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032638"
---
# <a name="update-formatprotection"></a><span data-ttu-id="774ea-103">Update formatprotection</span><span class="sxs-lookup"><span data-stu-id="774ea-103">Update formatprotection</span></span>

<span data-ttu-id="774ea-104">Actualiza las propiedades del objeto formatprotection.</span><span class="sxs-lookup"><span data-stu-id="774ea-104">Update the properties of formatprotection object.</span></span>
## <a name="permissions"></a><span data-ttu-id="774ea-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="774ea-105">Permissions</span></span>
<span data-ttu-id="774ea-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="774ea-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="774ea-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="774ea-108">Permission type</span></span>      | <span data-ttu-id="774ea-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="774ea-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="774ea-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="774ea-110">Delegated (work or school account)</span></span> | <span data-ttu-id="774ea-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="774ea-111">Files.ReadWrite</span></span>    | 
|<span data-ttu-id="774ea-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="774ea-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="774ea-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="774ea-113">Not supported.</span></span>    | 
|<span data-ttu-id="774ea-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="774ea-114">Application</span></span> | <span data-ttu-id="774ea-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="774ea-115">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="774ea-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="774ea-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names/{name}/range/format/protection
PATCH /workbook/worksheets/{id|name}/range(<address>)/format/protection
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/protection
```
## <a name="optional-request-headers"></a><span data-ttu-id="774ea-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="774ea-117">Optional request headers</span></span>
| <span data-ttu-id="774ea-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="774ea-118">Name</span></span>       | <span data-ttu-id="774ea-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="774ea-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="774ea-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="774ea-120">Authorization</span></span>  | <span data-ttu-id="774ea-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="774ea-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="774ea-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="774ea-123">Request body</span></span>
<span data-ttu-id="774ea-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="774ea-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="774ea-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="774ea-127">Property</span></span>     | <span data-ttu-id="774ea-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="774ea-128">Type</span></span>   |<span data-ttu-id="774ea-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="774ea-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="774ea-130">formulaHidden</span><span class="sxs-lookup"><span data-stu-id="774ea-130">formulaHidden</span></span>|<span data-ttu-id="774ea-131">boolean</span><span class="sxs-lookup"><span data-stu-id="774ea-131">boolean</span></span>|<span data-ttu-id="774ea-p104">Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.</span><span class="sxs-lookup"><span data-stu-id="774ea-p104">Indicates if Excel hides the formula for the cells in the range. A null value indicates that the entire range doesn't have uniform formula hidden setting.</span></span>|
|<span data-ttu-id="774ea-134">locked</span><span class="sxs-lookup"><span data-stu-id="774ea-134">locked</span></span>|<span data-ttu-id="774ea-135">boolean</span><span class="sxs-lookup"><span data-stu-id="774ea-135">boolean</span></span>|<span data-ttu-id="774ea-p105">Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.</span><span class="sxs-lookup"><span data-stu-id="774ea-p105">Indicates if Excel locks the cells in the object. A null value indicates that the entire range doesn't have uniform lock setting.</span></span>|

## <a name="response"></a><span data-ttu-id="774ea-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="774ea-138">Response</span></span>

<span data-ttu-id="774ea-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [FormatProtection](../resources/formatprotection.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="774ea-139">If successful, this method returns a `200 OK` response code and updated [FormatProtection](../resources/formatprotection.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="774ea-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="774ea-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="774ea-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="774ea-141">Request</span></span>
<span data-ttu-id="774ea-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="774ea-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_formatprotection"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/protection
Content-type: application/json
Content-length: 45

{
  "locked": true,
  "formulaHidden": true
}
```
##### <a name="response"></a><span data-ttu-id="774ea-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="774ea-143">Response</span></span>
<span data-ttu-id="774ea-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="774ea-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookFormatProtection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "locked": true,
  "formulaHidden": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update formatprotection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->