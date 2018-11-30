---
title: Update table
description: Actualizar las propiedades del objeto table.
ms.openlocfilehash: a929329ed9a88b7dda6206193292f1ca1e63ced1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086321"
---
# <a name="update-table"></a><span data-ttu-id="76926-103">Actualizar tabla</span><span class="sxs-lookup"><span data-stu-id="76926-103">Update table</span></span>

> <span data-ttu-id="76926-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="76926-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="76926-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="76926-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="76926-106">Actualizar las propiedades del objeto table.</span><span class="sxs-lookup"><span data-stu-id="76926-106">Update the properties of table object.</span></span>
## <a name="permissions"></a><span data-ttu-id="76926-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="76926-107">Permissions</span></span>
<span data-ttu-id="76926-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76926-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76926-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76926-110">Permission type</span></span>      | <span data-ttu-id="76926-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76926-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76926-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76926-112">Delegated (work or school account)</span></span> | <span data-ttu-id="76926-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76926-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="76926-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76926-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76926-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76926-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="76926-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76926-116">Application</span></span> | <span data-ttu-id="76926-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="76926-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="76926-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76926-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="76926-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="76926-119">Optional request headers</span></span>
| <span data-ttu-id="76926-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="76926-120">Name</span></span>       | <span data-ttu-id="76926-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="76926-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="76926-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="76926-122">Authorization</span></span>  | <span data-ttu-id="76926-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76926-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="76926-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="76926-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="76926-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="76926-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="76926-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76926-128">Request body</span></span>
<span data-ttu-id="76926-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="76926-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="76926-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="76926-132">Property</span></span>     | <span data-ttu-id="76926-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="76926-133">Type</span></span>   |<span data-ttu-id="76926-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="76926-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="76926-135">name</span><span class="sxs-lookup"><span data-stu-id="76926-135">name</span></span>|<span data-ttu-id="76926-136">string</span><span class="sxs-lookup"><span data-stu-id="76926-136">string</span></span>|<span data-ttu-id="76926-137">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76926-137">Name of the table.</span></span>|
|<span data-ttu-id="76926-138">showHeaders</span><span class="sxs-lookup"><span data-stu-id="76926-138">showHeaders</span></span>|<span data-ttu-id="76926-139">boolean</span><span class="sxs-lookup"><span data-stu-id="76926-139">boolean</span></span>|<span data-ttu-id="76926-p106">Indica si la fila de encabezado está visible o no. Este valor puede establecerse para que muestre o quite la fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="76926-p106">Indicates whether the header row is visible or not. This value can be set to show or remove the header row.</span></span>|
|<span data-ttu-id="76926-142">showTotals</span><span class="sxs-lookup"><span data-stu-id="76926-142">showTotals</span></span>|<span data-ttu-id="76926-143">boolean</span><span class="sxs-lookup"><span data-stu-id="76926-143">boolean</span></span>|<span data-ttu-id="76926-p107">Indica si la fila de totales está visible o no. Este valor puede establecerse para que muestre o quite la fila de totales.</span><span class="sxs-lookup"><span data-stu-id="76926-p107">Indicates whether the total row is visible or not. This value can be set to show or remove the total row.</span></span>|
|<span data-ttu-id="76926-146">style</span><span class="sxs-lookup"><span data-stu-id="76926-146">style</span></span>|<span data-ttu-id="76926-147">string</span><span class="sxs-lookup"><span data-stu-id="76926-147">string</span></span>|<span data-ttu-id="76926-p108">Valor constante que representa el estilo de tabla. Los valores posibles son: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11. También puede especificarse un estilo personalizado definido por el usuario presente en el libro.</span><span class="sxs-lookup"><span data-stu-id="76926-p108">Constant value that represents the Table style. Possible values are: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11. A custom user-defined style present in the workbook can also be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="76926-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76926-151">Response</span></span>

<span data-ttu-id="76926-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Table](../resources/table.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76926-152">If successful, this method returns a `200 OK` response code and updated [Table](../resources/table.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="76926-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76926-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="76926-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76926-154">Request</span></span>
<span data-ttu-id="76926-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76926-155">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_table"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}
Content-type: application/json
Content-length: 109

{
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```
##### <a name="response"></a><span data-ttu-id="76926-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76926-156">Response</span></span>
<span data-ttu-id="76926-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="76926-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.table"
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
