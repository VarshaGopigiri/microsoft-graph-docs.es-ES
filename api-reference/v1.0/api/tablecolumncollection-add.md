---
title: 'TableColumnCollection: add'
description: Agrega una nueva columna a la tabla.
ms.openlocfilehash: 20d06afa207a930db1aeb9ecdf86f17a818b3987
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029990"
---
# <a name="tablecolumncollection-add"></a><span data-ttu-id="137c1-103">TableColumnCollection: add</span><span class="sxs-lookup"><span data-stu-id="137c1-103">TableColumnCollection: add</span></span>

<span data-ttu-id="137c1-104">Agrega una nueva columna a la tabla.</span><span class="sxs-lookup"><span data-stu-id="137c1-104">Adds a new column to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="137c1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="137c1-105">Permissions</span></span>
<span data-ttu-id="137c1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="137c1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="137c1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="137c1-108">Permission type</span></span>      | <span data-ttu-id="137c1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="137c1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="137c1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="137c1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="137c1-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="137c1-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="137c1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="137c1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="137c1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="137c1-113">Not supported.</span></span>    |
|<span data-ttu-id="137c1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="137c1-114">Application</span></span> | <span data-ttu-id="137c1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="137c1-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="137c1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="137c1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/add

```
## <a name="request-headers"></a><span data-ttu-id="137c1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="137c1-117">Request headers</span></span>
| <span data-ttu-id="137c1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="137c1-118">Name</span></span>       | <span data-ttu-id="137c1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="137c1-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="137c1-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="137c1-120">Authorization</span></span>  | <span data-ttu-id="137c1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="137c1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="137c1-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="137c1-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="137c1-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="137c1-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="137c1-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="137c1-126">Request body</span></span>
<span data-ttu-id="137c1-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="137c1-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="137c1-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="137c1-128">Parameter</span></span>    | <span data-ttu-id="137c1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="137c1-129">Type</span></span>   |<span data-ttu-id="137c1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="137c1-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="137c1-131">index</span><span class="sxs-lookup"><span data-stu-id="137c1-131">index</span></span>|<span data-ttu-id="137c1-132">Int32</span><span class="sxs-lookup"><span data-stu-id="137c1-132">Int32</span></span>|<span data-ttu-id="137c1-p104">Especifica la posición relativa de la nueva columna. La columna anterior en esta posición se desplaza hacia la derecha. El valor de índice debe ser igual o menor que el valor de índice de la última columna, por lo que no puede usarse para agregar una columna al final de la tabla. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="137c1-p104">Specifies the relative position of the new column. The previous column at this position is shifted to the right. The index value should be equal to or less than the last column's index value, so it cannot be used to append a column at the end of the table. Zero-indexed.</span></span>|
|<span data-ttu-id="137c1-137">values</span><span class="sxs-lookup"><span data-stu-id="137c1-137">values</span></span>|<span data-ttu-id="137c1-138">Json</span><span class="sxs-lookup"><span data-stu-id="137c1-138">Json</span></span>|<span data-ttu-id="137c1-p105">Opcional. Matriz bidimensional de valores sin formato de la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="137c1-p105">Optional. A 2-dimensional array of unformatted values of the table column.</span></span>|
|<span data-ttu-id="137c1-141">name</span><span class="sxs-lookup"><span data-stu-id="137c1-141">name</span></span>|<span data-ttu-id="137c1-142">string</span><span class="sxs-lookup"><span data-stu-id="137c1-142">string</span></span>|<span data-ttu-id="137c1-143">name</span><span class="sxs-lookup"><span data-stu-id="137c1-143">name</span></span>
## <a name="response"></a><span data-ttu-id="137c1-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="137c1-144">Response</span></span>

<span data-ttu-id="137c1-145">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookTableColumn](../resources/tablecolumn.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="137c1-145">If successful, this method returns `200 OK` response code and [WorkbookTableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="137c1-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="137c1-146">Example</span></span>
<span data-ttu-id="137c1-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="137c1-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="137c1-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="137c1-148">Request</span></span>
<span data-ttu-id="137c1-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="137c1-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumncollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/add
Content-type: application/json
Content-length: 51

{
  "index": 3,
  "values": [
    {
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="137c1-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="137c1-150">Response</span></span>
<span data-ttu-id="137c1-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="137c1-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableColumnCollection: add",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/api/tablecolumncollection-add.md/tablecolumncollection_add/values:
      Inconsistent types between parameter (Object) and table (None)",
    "Error: /api-reference/v1.0/api/tablecolumncollection-add.md/tablecolumncollection_add/values:
      Type mismatch between example and table. Parameter name: values; example type (Collection(Object)) is a collection, while the table description type (microsoft.graph.Json) is not."
  ],
  "tocPath": ""
}-->