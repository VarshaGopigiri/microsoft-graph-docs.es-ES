---
title: 'TableColumnCollection: add'
description: Agrega una nueva columna a la tabla.
ms.openlocfilehash: 64b6fd2c91642c3f7dd6f5d3e6aaa89b526a28a8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090267"
---
# <a name="tablecolumncollection-add"></a><span data-ttu-id="f4b6f-103">TableColumnCollection: add</span><span class="sxs-lookup"><span data-stu-id="f4b6f-103">TableColumnCollection: add</span></span>

> <span data-ttu-id="f4b6f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4b6f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f4b6f-106">Agrega una nueva columna a la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-106">Adds a new column to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="f4b6f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f4b6f-107">Permissions</span></span>
<span data-ttu-id="f4b6f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4b6f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f4b6f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4b6f-110">Permission type</span></span>      | <span data-ttu-id="f4b6f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4b6f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f4b6f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4b6f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f4b6f-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f4b6f-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f4b6f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4b6f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f4b6f-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f4b6f-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f4b6f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4b6f-116">Application</span></span> | <span data-ttu-id="f4b6f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f4b6f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4b6f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/add

```
## <a name="request-headers"></a><span data-ttu-id="f4b6f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4b6f-119">Request headers</span></span>
| <span data-ttu-id="f4b6f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4b6f-120">Name</span></span>       | <span data-ttu-id="f4b6f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4b6f-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f4b6f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f4b6f-122">Authorization</span></span>  | <span data-ttu-id="f4b6f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f4b6f-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f4b6f-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="f4b6f-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f4b6f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4b6f-128">Request body</span></span>
<span data-ttu-id="f4b6f-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f4b6f-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f4b6f-130">Parameter</span></span>    | <span data-ttu-id="f4b6f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4b6f-131">Type</span></span>   |<span data-ttu-id="f4b6f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4b6f-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f4b6f-133">index</span><span class="sxs-lookup"><span data-stu-id="f4b6f-133">index</span></span>|<span data-ttu-id="f4b6f-134">number</span><span class="sxs-lookup"><span data-stu-id="f4b6f-134">number</span></span>|<span data-ttu-id="f4b6f-p105">Especifica la posición relativa de la nueva columna. La columna anterior en esta posición se desplaza hacia la derecha. El valor de índice debe ser igual o menor que el valor de índice de la última columna, por lo que no puede usarse para agregar una columna al final de la tabla. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-p105">Specifies the relative position of the new column. The previous column at this position is shifted to the right. The index value should be equal to or less than the last column's index value, so it cannot be used to append a column at the end of the table. Zero-indexed.</span></span>|
|<span data-ttu-id="f4b6f-139">values</span><span class="sxs-lookup"><span data-stu-id="f4b6f-139">values</span></span>|<span data-ttu-id="f4b6f-140">(boolean, string o number)</span><span class="sxs-lookup"><span data-stu-id="f4b6f-140">(boolean or string or number)</span></span>|<span data-ttu-id="f4b6f-p106">Opcional. Matriz bidimensional de valores sin formato de la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-p106">Optional. A 2-dimensional array of unformatted values of the table column.</span></span>|

## <a name="response"></a><span data-ttu-id="f4b6f-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4b6f-143">Response</span></span>

<span data-ttu-id="f4b6f-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-144">If successful, this method returns `200 OK` response code and [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4b6f-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4b6f-145">Example</span></span>
<span data-ttu-id="f4b6f-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f4b6f-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4b6f-147">Request</span></span>
<span data-ttu-id="f4b6f-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumncollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns/add
Content-type: application/json
Content-length: 51

{
  "index": {
  },
  "values": [
    {
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="f4b6f-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4b6f-149">Response</span></span>
<span data-ttu-id="f4b6f-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4b6f-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn"
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
  "tocPath": ""
}-->