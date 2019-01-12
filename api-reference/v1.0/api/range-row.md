---
title: 'Range: Row'
description: Obtiene una fila contenida en el rango.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: ab08c923d7337f53b96ec4a46246a7d8087794b3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919466"
---
# <a name="range-row"></a><span data-ttu-id="b8f6f-103">Range: Row</span><span class="sxs-lookup"><span data-stu-id="b8f6f-103">Range: Row</span></span>

<span data-ttu-id="b8f6f-104">Obtiene una fila contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-104">Gets a row contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="b8f6f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b8f6f-105">Permissions</span></span>
<span data-ttu-id="b8f6f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8f6f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8f6f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8f6f-108">Permission type</span></span>      | <span data-ttu-id="b8f6f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8f6f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b8f6f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8f6f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b8f6f-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b8f6f-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b8f6f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8f6f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b8f6f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-113">Not supported.</span></span>    |
|<span data-ttu-id="b8f6f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8f6f-114">Application</span></span> | <span data-ttu-id="b8f6f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b8f6f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8f6f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/row
POST /workbook/worksheets/{id|name}/range(address='<address>')/row
POST /workbook/tables/{id|name}/columns/{id|name}/range/row

```
## <a name="request-headers"></a><span data-ttu-id="b8f6f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8f6f-117">Request headers</span></span>
| <span data-ttu-id="b8f6f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b8f6f-118">Name</span></span>       | <span data-ttu-id="b8f6f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8f6f-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b8f6f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8f6f-120">Authorization</span></span>  | <span data-ttu-id="b8f6f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b8f6f-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b8f6f-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="b8f6f-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b8f6f-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8f6f-126">Request body</span></span>
<span data-ttu-id="b8f6f-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b8f6f-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b8f6f-128">Parameter</span></span>    | <span data-ttu-id="b8f6f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8f6f-129">Type</span></span>   |<span data-ttu-id="b8f6f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8f6f-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b8f6f-131">row</span><span class="sxs-lookup"><span data-stu-id="b8f6f-131">row</span></span>|<span data-ttu-id="b8f6f-132">Int32</span><span class="sxs-lookup"><span data-stu-id="b8f6f-132">Int32</span></span>|<span data-ttu-id="b8f6f-p104">Número de fila del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-p104">Row number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="b8f6f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8f6f-135">Response</span></span>

<span data-ttu-id="b8f6f-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-136">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8f6f-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8f6f-137">Example</span></span>
<span data-ttu-id="b8f6f-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b8f6f-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8f6f-139">Request</span></span>
<span data-ttu-id="b8f6f-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-140">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_row",
  "idempotent": true,
  "@type": "requestBodyResourceFor.range_row"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/row
Content-type: application/json
Content-length: 18

{
  "row": 2
}
```

##### <a name="response"></a><span data-ttu-id="b8f6f-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8f6f-141">Response</span></span>
<span data-ttu-id="b8f6f-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8f6f-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Row",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
