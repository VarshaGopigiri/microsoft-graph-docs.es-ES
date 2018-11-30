---
title: 'Worksheet: UsedRange'
description: El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.
ms.openlocfilehash: 6da0ad6ab5fe71491d30eac1e95255d39ba37a18
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029056"
---
# <a name="worksheet-usedrange"></a><span data-ttu-id="1aa9e-104">Worksheet: UsedRange</span><span class="sxs-lookup"><span data-stu-id="1aa9e-104">Worksheet: UsedRange</span></span>

<span data-ttu-id="1aa9e-p102">El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-p102">The used range is the smallest range that encompasses any cells that have a value or formatting assigned to them. If the worksheet is blank, this function will return the top left cell.</span></span>
## <a name="permissions"></a><span data-ttu-id="1aa9e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1aa9e-107">Permissions</span></span>
<span data-ttu-id="1aa9e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1aa9e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1aa9e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1aa9e-110">Permission type</span></span>      | <span data-ttu-id="1aa9e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1aa9e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1aa9e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1aa9e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1aa9e-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1aa9e-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1aa9e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1aa9e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1aa9e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-115">Not supported.</span></span>    |
|<span data-ttu-id="1aa9e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1aa9e-116">Application</span></span> | <span data-ttu-id="1aa9e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1aa9e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1aa9e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/usedRange

```

## <a name="function-parameters"></a><span data-ttu-id="1aa9e-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="1aa9e-119">Function parameters</span></span>
<span data-ttu-id="1aa9e-120">En la dirección URL de la solicitud puede proporcionar parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-120">In the request URL you may provide optional parameters.</span></span>

| <span data-ttu-id="1aa9e-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1aa9e-121">Parameter</span></span>    | <span data-ttu-id="1aa9e-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="1aa9e-122">Type</span></span>   |<span data-ttu-id="1aa9e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1aa9e-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1aa9e-124">valuesOnly</span><span class="sxs-lookup"><span data-stu-id="1aa9e-124">valuesOnly</span></span>|<span data-ttu-id="1aa9e-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="1aa9e-125">Boolean</span></span>|<span data-ttu-id="1aa9e-p104">Opcional. Solo tiene en cuenta las celdas con valores como celdas usadas (ignora el formato).</span><span class="sxs-lookup"><span data-stu-id="1aa9e-p104">Optional. Considers only cells with values as used cells (ignores formatting).</span></span>|

## <a name="request-headers"></a><span data-ttu-id="1aa9e-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1aa9e-128">Request headers</span></span>
| <span data-ttu-id="1aa9e-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa9e-129">Name</span></span>       | <span data-ttu-id="1aa9e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1aa9e-130">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1aa9e-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="1aa9e-131">Authorization</span></span>  | <span data-ttu-id="1aa9e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1aa9e-134">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1aa9e-134">Workbook-Session-Id</span></span>  | <span data-ttu-id="1aa9e-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1aa9e-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1aa9e-137">Request body</span></span>
<span data-ttu-id="1aa9e-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1aa9e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1aa9e-139">Response</span></span>

<span data-ttu-id="1aa9e-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-140">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1aa9e-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1aa9e-141">Example</span></span>
<span data-ttu-id="1aa9e-142">Aquí tiene un ejemplo que muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-142">Here is an example that shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="1aa9e-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1aa9e-143">Request</span></span>
<span data-ttu-id="1aa9e-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-144">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "worksheet_usedrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/usedRange
```

##### <a name="response"></a><span data-ttu-id="1aa9e-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1aa9e-145">Response</span></span>
<span data-ttu-id="1aa9e-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "addressLocal": "addressLocal-value"
}
```

<span data-ttu-id="1aa9e-149">Como alternativa, esta función se puede llamar con el opcional `valuesOnly` parámetro.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-149">Alternatively, this function can be called with the optional `valuesOnly` parameter.</span></span>

##### <a name="request"></a><span data-ttu-id="1aa9e-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1aa9e-150">Request</span></span>
<span data-ttu-id="1aa9e-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-151">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "worksheet_usedrange_valuesonly"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/usedRange(valuesOnly=true)
```

##### <a name="response"></a><span data-ttu-id="1aa9e-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1aa9e-152">Response</span></span>
<span data-ttu-id="1aa9e-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1aa9e-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "addressLocal": "addressLocal-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet: UsedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
