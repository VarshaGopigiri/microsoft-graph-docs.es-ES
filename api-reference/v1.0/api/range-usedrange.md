---
title: 'Range: UsedRange'
description: Devuelve el rango usado del objeto de rango especificado.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: db17537de2cd002a16b2c0306d4e4c9304010e44
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961480"
---
# <a name="range-usedrange"></a><span data-ttu-id="f4293-103">Range: UsedRange</span><span class="sxs-lookup"><span data-stu-id="f4293-103">Range: UsedRange</span></span>

<span data-ttu-id="f4293-104">Devuelve el rango usado del objeto de rango especificado.</span><span class="sxs-lookup"><span data-stu-id="f4293-104">Returns the used range of the given range object.</span></span>
## <a name="permissions"></a><span data-ttu-id="f4293-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f4293-105">Permissions</span></span>
<span data-ttu-id="f4293-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4293-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f4293-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4293-108">Permission type</span></span>      | <span data-ttu-id="f4293-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4293-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f4293-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4293-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f4293-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f4293-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f4293-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4293-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f4293-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4293-113">Not supported.</span></span>    |
|<span data-ttu-id="f4293-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4293-114">Application</span></span> | <span data-ttu-id="f4293-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4293-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f4293-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4293-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/usedRange
GET /workbook/worksheets/{id|name}/range(address='<address>')/usedRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/usedRange

```
## <a name="request-headers"></a><span data-ttu-id="f4293-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4293-117">Request headers</span></span>
| <span data-ttu-id="f4293-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4293-118">Name</span></span>       | <span data-ttu-id="f4293-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4293-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f4293-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f4293-120">Authorization</span></span>  | <span data-ttu-id="f4293-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f4293-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f4293-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f4293-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="f4293-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f4293-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="f4293-126">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="f4293-126">Path parameters</span></span>
| <span data-ttu-id="f4293-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f4293-127">Parameter</span></span>    | <span data-ttu-id="f4293-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4293-128">Type</span></span>   |<span data-ttu-id="f4293-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4293-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f4293-130">valuesOnly</span><span class="sxs-lookup"><span data-stu-id="f4293-130">valuesOnly</span></span>|<span data-ttu-id="f4293-131">boolean</span><span class="sxs-lookup"><span data-stu-id="f4293-131">boolean</span></span>|<span data-ttu-id="f4293-p104">Opcional. Solo tiene en cuenta las celdas con valores como celdas usadas.</span><span class="sxs-lookup"><span data-stu-id="f4293-p104">Optional. Considers only cells with values as used cells.</span></span>|

## <a name="response"></a><span data-ttu-id="f4293-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4293-134">Response</span></span>

<span data-ttu-id="f4293-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4293-135">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4293-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4293-136">Example</span></span>
<span data-ttu-id="f4293-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f4293-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f4293-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4293-138">Request</span></span>
<span data-ttu-id="f4293-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4293-139">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_usedrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/usedRange
```

##### <a name="response"></a><span data-ttu-id="f4293-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4293-140">Response</span></span>
<span data-ttu-id="f4293-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4293-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<span data-ttu-id="f4293-144">Este es un ejemplo que especifica el opcional `valuesOnly` parámetro.</span><span class="sxs-lookup"><span data-stu-id="f4293-144">Here is an example specifying the optional `valuesOnly` parameter.</span></span>

##### <a name="request"></a><span data-ttu-id="f4293-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4293-145">Request</span></span>
<span data-ttu-id="f4293-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4293-146">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_usedrange_valuesonly"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/usedRange(valuesOnly=true)
```

##### <a name="response"></a><span data-ttu-id="f4293-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4293-147">Response</span></span>

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
  "cellCount": 90,
  "columnCount": 90,
  "columnIndex": 90,
  "valueTypes": "valueTypes-value"
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: UsedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
