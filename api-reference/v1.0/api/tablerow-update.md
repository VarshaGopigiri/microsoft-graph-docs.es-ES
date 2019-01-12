---
title: Update tablerow
description: Actualizar las propiedades del objeto tablerow.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 82eb1d10ebca09dd569718a7ce8e797586e7e374
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911984"
---
# <a name="update-tablerow"></a><span data-ttu-id="a78fd-103">Update tablerow</span><span class="sxs-lookup"><span data-stu-id="a78fd-103">Update tablerow</span></span>

<span data-ttu-id="a78fd-104">Actualizar las propiedades del objeto tablerow.</span><span class="sxs-lookup"><span data-stu-id="a78fd-104">Update the properties of tablerow object.</span></span>
## <a name="permissions"></a><span data-ttu-id="a78fd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a78fd-105">Permissions</span></span>
<span data-ttu-id="a78fd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a78fd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a78fd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a78fd-108">Permission type</span></span>      | <span data-ttu-id="a78fd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a78fd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a78fd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a78fd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a78fd-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a78fd-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a78fd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a78fd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a78fd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a78fd-113">Not supported.</span></span>    |
|<span data-ttu-id="a78fd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a78fd-114">Application</span></span> | <span data-ttu-id="a78fd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a78fd-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a78fd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a78fd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/rows/{index}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/rows/{index}
```
## <a name="optional-request-headers"></a><span data-ttu-id="a78fd-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="a78fd-117">Optional request headers</span></span>
| <span data-ttu-id="a78fd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="a78fd-118">Name</span></span>       | <span data-ttu-id="a78fd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a78fd-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="a78fd-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a78fd-120">Authorization</span></span>  | <span data-ttu-id="a78fd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a78fd-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a78fd-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="a78fd-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="a78fd-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="a78fd-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a78fd-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a78fd-126">Request body</span></span>
<span data-ttu-id="a78fd-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a78fd-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a78fd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a78fd-130">Property</span></span>     | <span data-ttu-id="a78fd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a78fd-131">Type</span></span>   |<span data-ttu-id="a78fd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a78fd-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a78fd-133">values</span><span class="sxs-lookup"><span data-stu-id="a78fd-133">values</span></span>|<span data-ttu-id="a78fd-134">Json</span><span class="sxs-lookup"><span data-stu-id="a78fd-134">Json</span></span>|<span data-ttu-id="a78fd-p105">Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="a78fd-p105">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="response"></a><span data-ttu-id="a78fd-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a78fd-138">Response</span></span>

<span data-ttu-id="a78fd-139">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookTableRow](../resources/tablerow.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a78fd-139">If successful, this method returns a `200 OK` response code and updated [WorkbookTableRow](../resources/tablerow.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a78fd-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a78fd-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a78fd-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a78fd-141">Request</span></span>
<span data-ttu-id="a78fd-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a78fd-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_tablerow"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows/{index}
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```
##### <a name="response"></a><span data-ttu-id="a78fd-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a78fd-143">Response</span></span>
<span data-ttu-id="a78fd-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a78fd-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tablerow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
