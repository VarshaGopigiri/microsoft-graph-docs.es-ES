---
title: 'Range: UsedRange'
description: Devuelve el rango usado del objeto de rango especificado.
ms.openlocfilehash: 26938b010a42e58b8bdc01687211c434514277de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031109"
---
# <a name="range-usedrange"></a><span data-ttu-id="eb70a-103">Range: UsedRange</span><span class="sxs-lookup"><span data-stu-id="eb70a-103">Range: UsedRange</span></span>

<span data-ttu-id="eb70a-104">Devuelve el rango usado del objeto de rango especificado.</span><span class="sxs-lookup"><span data-stu-id="eb70a-104">Returns the used range of the given range object.</span></span>
## <a name="permissions"></a><span data-ttu-id="eb70a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="eb70a-105">Permissions</span></span>
<span data-ttu-id="eb70a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb70a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb70a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb70a-108">Permission type</span></span>      | <span data-ttu-id="eb70a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb70a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eb70a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb70a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="eb70a-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eb70a-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="eb70a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb70a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eb70a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb70a-113">Not supported.</span></span>    |
|<span data-ttu-id="eb70a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb70a-114">Application</span></span> | <span data-ttu-id="eb70a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb70a-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="eb70a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb70a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/usedRange
GET /workbook/worksheets/{id|name}/range(address='<address>')/usedRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/usedRange

```
## <a name="request-headers"></a><span data-ttu-id="eb70a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb70a-117">Request headers</span></span>
| <span data-ttu-id="eb70a-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb70a-118">Name</span></span>       | <span data-ttu-id="eb70a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb70a-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="eb70a-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="eb70a-120">Authorization</span></span>  | <span data-ttu-id="eb70a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb70a-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eb70a-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="eb70a-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="eb70a-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="eb70a-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="eb70a-126">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="eb70a-126">Path parameters</span></span>
| <span data-ttu-id="eb70a-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="eb70a-127">Parameter</span></span>    | <span data-ttu-id="eb70a-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb70a-128">Type</span></span>   |<span data-ttu-id="eb70a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb70a-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eb70a-130">valuesOnly</span><span class="sxs-lookup"><span data-stu-id="eb70a-130">valuesOnly</span></span>|<span data-ttu-id="eb70a-131">boolean</span><span class="sxs-lookup"><span data-stu-id="eb70a-131">boolean</span></span>|<span data-ttu-id="eb70a-p104">Opcional. Solo tiene en cuenta las celdas con valores como celdas usadas.</span><span class="sxs-lookup"><span data-stu-id="eb70a-p104">Optional. Considers only cells with values as used cells.</span></span>|

## <a name="response"></a><span data-ttu-id="eb70a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb70a-134">Response</span></span>

<span data-ttu-id="eb70a-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb70a-135">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eb70a-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb70a-136">Example</span></span>
<span data-ttu-id="eb70a-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="eb70a-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="eb70a-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb70a-138">Request</span></span>
<span data-ttu-id="eb70a-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb70a-139">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_usedrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/usedRange
```

##### <a name="response"></a><span data-ttu-id="eb70a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb70a-140">Response</span></span>
<span data-ttu-id="eb70a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb70a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<span data-ttu-id="eb70a-144">Este es un ejemplo que especifica el opcional `valuesOnly` parámetro.</span><span class="sxs-lookup"><span data-stu-id="eb70a-144">Here is an example specifying the optional `valuesOnly` parameter.</span></span>

##### <a name="request"></a><span data-ttu-id="eb70a-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb70a-145">Request</span></span>
<span data-ttu-id="eb70a-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb70a-146">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_usedrange_valuesonly"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/usedRange(valuesOnly=true)
```

##### <a name="response"></a><span data-ttu-id="eb70a-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb70a-147">Response</span></span>

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