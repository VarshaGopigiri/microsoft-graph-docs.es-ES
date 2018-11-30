---
title: Update tablecolumn
description: Actualizar las propiedades del objeto tablecolumn.
ms.openlocfilehash: bdf7414186d62f6875488af4f83e302118de3e08
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028633"
---
# <a name="update-tablecolumn"></a><span data-ttu-id="628cf-103">Update tablecolumn</span><span class="sxs-lookup"><span data-stu-id="628cf-103">Update tablecolumn</span></span>

<span data-ttu-id="628cf-104">Actualizar las propiedades del objeto tablecolumn.</span><span class="sxs-lookup"><span data-stu-id="628cf-104">Update the properties of tablecolumn object.</span></span>
## <a name="permissions"></a><span data-ttu-id="628cf-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="628cf-105">Permissions</span></span>
<span data-ttu-id="628cf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="628cf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="628cf-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="628cf-108">Permission type</span></span>      | <span data-ttu-id="628cf-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="628cf-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="628cf-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="628cf-110">Delegated (work or school account)</span></span> | <span data-ttu-id="628cf-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="628cf-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="628cf-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="628cf-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="628cf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="628cf-113">Not supported.</span></span>    |
|<span data-ttu-id="628cf-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="628cf-114">Application</span></span> | <span data-ttu-id="628cf-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="628cf-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="628cf-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="628cf-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/columns/{id|name}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="628cf-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="628cf-117">Optional request headers</span></span>
| <span data-ttu-id="628cf-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="628cf-118">Name</span></span>       | <span data-ttu-id="628cf-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="628cf-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="628cf-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="628cf-120">Authorization</span></span>  | <span data-ttu-id="628cf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="628cf-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="628cf-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="628cf-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="628cf-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="628cf-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="628cf-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="628cf-126">Request body</span></span>
<span data-ttu-id="628cf-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="628cf-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="628cf-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="628cf-130">Property</span></span>     | <span data-ttu-id="628cf-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="628cf-131">Type</span></span>   |<span data-ttu-id="628cf-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="628cf-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="628cf-133">values</span><span class="sxs-lookup"><span data-stu-id="628cf-133">values</span></span>|<span data-ttu-id="628cf-134">Json</span><span class="sxs-lookup"><span data-stu-id="628cf-134">Json</span></span>|<span data-ttu-id="628cf-p105">Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="628cf-p105">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="response"></a><span data-ttu-id="628cf-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="628cf-138">Response</span></span>

<span data-ttu-id="628cf-139">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookTableColumn](../resources/tablecolumn.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="628cf-139">If successful, this method returns a `200 OK` response code and updated [WorkbookTableColumn](../resources/tablecolumn.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="628cf-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="628cf-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="628cf-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="628cf-141">Request</span></span>
<span data-ttu-id="628cf-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="628cf-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_tablecolumn"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}
Content-type: application/json
Content-length: 81

{
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```
##### <a name="response"></a><span data-ttu-id="628cf-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="628cf-143">Response</span></span>
<span data-ttu-id="628cf-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="628cf-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableColumn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tablecolumn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->