---
title: 'Range: Column'
description: Obtiene una columna contenida en el rango.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 5966e8429d2a0406df3b6774db673d286cc4c8b2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870899"
---
# <a name="range-column"></a><span data-ttu-id="1628e-103">Range: Column</span><span class="sxs-lookup"><span data-stu-id="1628e-103">Range: Column</span></span>

<span data-ttu-id="1628e-104">Obtiene una columna contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="1628e-104">Gets a column contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="1628e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1628e-105">Permissions</span></span>
<span data-ttu-id="1628e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1628e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1628e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1628e-108">Permission type</span></span>      | <span data-ttu-id="1628e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1628e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1628e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1628e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1628e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1628e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1628e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1628e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1628e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1628e-113">Not supported.</span></span>    |
|<span data-ttu-id="1628e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1628e-114">Application</span></span> | <span data-ttu-id="1628e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1628e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1628e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1628e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/column
GET /workbook/worksheets/{id|name}/range(address='<address>')/column
GET /workbook/tables/{id|name}/columns/{id|name}/range/column

```
## <a name="request-headers"></a><span data-ttu-id="1628e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1628e-117">Request headers</span></span>
| <span data-ttu-id="1628e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1628e-118">Name</span></span>       | <span data-ttu-id="1628e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1628e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1628e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1628e-120">Authorization</span></span>  | <span data-ttu-id="1628e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1628e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1628e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1628e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="1628e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1628e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="1628e-126">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="1628e-126">Path parameters</span></span>
<span data-ttu-id="1628e-127">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="1628e-127">In the request path, provide the following parameters.</span></span>

| <span data-ttu-id="1628e-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1628e-128">Parameter</span></span>    | <span data-ttu-id="1628e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1628e-129">Type</span></span>   |<span data-ttu-id="1628e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1628e-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1628e-131">column</span><span class="sxs-lookup"><span data-stu-id="1628e-131">column</span></span>|<span data-ttu-id="1628e-132">Int32</span><span class="sxs-lookup"><span data-stu-id="1628e-132">Int32</span></span>|<span data-ttu-id="1628e-p104">Número de columna del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="1628e-p104">Column number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="1628e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1628e-135">Response</span></span>

<span data-ttu-id="1628e-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1628e-136">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1628e-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1628e-137">Example</span></span>
<span data-ttu-id="1628e-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1628e-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1628e-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1628e-139">Request</span></span>
<span data-ttu-id="1628e-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1628e-140">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_column"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/column(column=5)
```

##### <a name="response"></a><span data-ttu-id="1628e-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1628e-141">Response</span></span>
<span data-ttu-id="1628e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1628e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: Column",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
