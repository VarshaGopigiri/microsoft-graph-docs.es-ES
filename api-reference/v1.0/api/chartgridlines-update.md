---
title: Actualizar chartgridlines
description: Actualizar las propiedades del objeto chartgridlines.
ms.openlocfilehash: 80eb40f1d92d46313994b8fe9c6dea566edd4a2d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029929"
---
# <a name="update-chartgridlines"></a><span data-ttu-id="6c9bd-103">Actualizar chartgridlines</span><span class="sxs-lookup"><span data-stu-id="6c9bd-103">Update chartgridlines</span></span>

<span data-ttu-id="6c9bd-104">Actualizar las propiedades del objeto chartgridlines.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-104">Update the properties of chartgridlines object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6c9bd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6c9bd-105">Permissions</span></span>
<span data-ttu-id="6c9bd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6c9bd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6c9bd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c9bd-108">Permission type</span></span>      | <span data-ttu-id="6c9bd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c9bd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6c9bd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c9bd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="6c9bd-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c9bd-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6c9bd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c9bd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6c9bd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-113">Not supported.</span></span>    |
|<span data-ttu-id="6c9bd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c9bd-114">Application</span></span> | <span data-ttu-id="6c9bd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6c9bd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c9bd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/minorGridlines
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/majorGridlines
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/majorGridlines
```
## <a name="request-headers"></a><span data-ttu-id="6c9bd-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c9bd-117">Request headers</span></span>
| <span data-ttu-id="6c9bd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c9bd-118">Name</span></span>       | <span data-ttu-id="6c9bd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c9bd-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="6c9bd-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6c9bd-120">Authorization</span></span>  | <span data-ttu-id="6c9bd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6c9bd-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6c9bd-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="6c9bd-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6c9bd-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c9bd-126">Request body</span></span>
<span data-ttu-id="6c9bd-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6c9bd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c9bd-130">Property</span></span>     | <span data-ttu-id="6c9bd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c9bd-131">Type</span></span>   |<span data-ttu-id="6c9bd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c9bd-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6c9bd-133">visible</span><span class="sxs-lookup"><span data-stu-id="6c9bd-133">visible</span></span>|<span data-ttu-id="6c9bd-134">boolean</span><span class="sxs-lookup"><span data-stu-id="6c9bd-134">boolean</span></span>|<span data-ttu-id="6c9bd-135">Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-135">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="response"></a><span data-ttu-id="6c9bd-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c9bd-136">Response</span></span>

<span data-ttu-id="6c9bd-137">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartGridlines](../resources/chartgridlines.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-137">If successful, this method returns a `200 OK` response code and updated [WorkbookChartGridlines](../resources/chartgridlines.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6c9bd-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c9bd-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6c9bd-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c9bd-139">Request</span></span>
<span data-ttu-id="6c9bd-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartgridlines"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/minorGridlines
Content-type: application/json
Content-length: 21

{
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="6c9bd-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c9bd-141">Response</span></span>
<span data-ttu-id="6c9bd-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartGridlines"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 21

{
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartgridlines",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->