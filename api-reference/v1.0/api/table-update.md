---
title: Update table
description: Actualizar las propiedades del objeto table.
ms.openlocfilehash: 0bf3979dcc056b6a32e9c4bb7c89bf3d6a7fab57
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030431"
---
# <a name="update-table"></a><span data-ttu-id="c438f-103">Update table</span><span class="sxs-lookup"><span data-stu-id="c438f-103">Update table</span></span>

<span data-ttu-id="c438f-104">Actualizar las propiedades del objeto table.</span><span class="sxs-lookup"><span data-stu-id="c438f-104">Update the properties of table object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c438f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c438f-105">Permissions</span></span>
<span data-ttu-id="c438f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c438f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c438f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c438f-108">Permission type</span></span>      | <span data-ttu-id="c438f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c438f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c438f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c438f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c438f-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c438f-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c438f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c438f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c438f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c438f-113">Not supported.</span></span>    |
|<span data-ttu-id="c438f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c438f-114">Application</span></span> | <span data-ttu-id="c438f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c438f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c438f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c438f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="c438f-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="c438f-117">Optional request headers</span></span>
| <span data-ttu-id="c438f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c438f-118">Name</span></span>       | <span data-ttu-id="c438f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c438f-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="c438f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c438f-120">Authorization</span></span>  | <span data-ttu-id="c438f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c438f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c438f-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c438f-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="c438f-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c438f-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c438f-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c438f-126">Request body</span></span>
<span data-ttu-id="c438f-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c438f-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c438f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c438f-130">Property</span></span>     | <span data-ttu-id="c438f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c438f-131">Type</span></span>   |<span data-ttu-id="c438f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c438f-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c438f-133">name</span><span class="sxs-lookup"><span data-stu-id="c438f-133">name</span></span>|<span data-ttu-id="c438f-134">string</span><span class="sxs-lookup"><span data-stu-id="c438f-134">string</span></span>|<span data-ttu-id="c438f-135">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c438f-135">Name of the table.</span></span>|
|<span data-ttu-id="c438f-136">showHeaders</span><span class="sxs-lookup"><span data-stu-id="c438f-136">showHeaders</span></span>|<span data-ttu-id="c438f-137">boolean</span><span class="sxs-lookup"><span data-stu-id="c438f-137">boolean</span></span>|<span data-ttu-id="c438f-p105">Indica si la fila de encabezado está visible o no. Este valor puede establecerse para que muestre o quite la fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c438f-p105">Indicates whether the header row is visible or not. This value can be set to show or remove the header row.</span></span>|
|<span data-ttu-id="c438f-140">showTotals</span><span class="sxs-lookup"><span data-stu-id="c438f-140">showTotals</span></span>|<span data-ttu-id="c438f-141">boolean</span><span class="sxs-lookup"><span data-stu-id="c438f-141">boolean</span></span>|<span data-ttu-id="c438f-p106">Indica si la fila de totales está visible o no. Este valor puede establecerse para que muestre o quite la fila de totales.</span><span class="sxs-lookup"><span data-stu-id="c438f-p106">Indicates whether the total row is visible or not. This value can be set to show or remove the total row.</span></span>|
|<span data-ttu-id="c438f-144">style</span><span class="sxs-lookup"><span data-stu-id="c438f-144">style</span></span>|<span data-ttu-id="c438f-145">string</span><span class="sxs-lookup"><span data-stu-id="c438f-145">string</span></span>|<span data-ttu-id="c438f-146">Valor constante que representa el estilo de tabla.</span><span class="sxs-lookup"><span data-stu-id="c438f-146">Constant value that represents the Table style.</span></span> <span data-ttu-id="c438f-147">Los valores posibles son: TableStyleLight1 a través de TableStyleLight21, TableStyleMedium1 a través de TableStyleMedium28, TableStyleStyleDark1 a través de TableStyleStyleDark11.</span><span class="sxs-lookup"><span data-stu-id="c438f-147">The possible values are: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11.</span></span> <span data-ttu-id="c438f-148">También se puede especificar un personalizadas definidas por el usuario estilo presente en el libro.</span><span class="sxs-lookup"><span data-stu-id="c438f-148">A custom user-defined style present in the workbook can also be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="c438f-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c438f-149">Response</span></span>

<span data-ttu-id="c438f-150">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookTable](../resources/table.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c438f-150">If successful, this method returns a `200 OK` response code and updated [WorkbookTable](../resources/table.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c438f-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c438f-151">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c438f-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c438f-152">Request</span></span>
<span data-ttu-id="c438f-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c438f-153">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_table"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}
Content-type: application/json
Content-length: 109

{
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```
##### <a name="response"></a><span data-ttu-id="c438f-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c438f-154">Response</span></span>
<span data-ttu-id="c438f-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c438f-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTable"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 109

{
  "id": "99",
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update table",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->