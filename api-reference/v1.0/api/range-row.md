---
title: 'Range: Row'
description: Obtiene una fila contenida en el rango.
author: lumine2008
ms.openlocfilehash: d758af607fa80314abe6c3f90e611eb87ac62914
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315032"
---
# <a name="range-row"></a><span data-ttu-id="38a7e-103">Range: Row</span><span class="sxs-lookup"><span data-stu-id="38a7e-103">Range: Row</span></span>

<span data-ttu-id="38a7e-104">Obtiene una fila contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="38a7e-104">Gets a row contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="38a7e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="38a7e-105">Permissions</span></span>
<span data-ttu-id="38a7e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38a7e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38a7e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38a7e-108">Permission type</span></span>      | <span data-ttu-id="38a7e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38a7e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="38a7e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38a7e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="38a7e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38a7e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="38a7e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38a7e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38a7e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38a7e-113">Not supported.</span></span>    |
|<span data-ttu-id="38a7e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38a7e-114">Application</span></span> | <span data-ttu-id="38a7e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38a7e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="38a7e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38a7e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/row
POST /workbook/worksheets/{id|name}/range(address='<address>')/row
POST /workbook/tables/{id|name}/columns/{id|name}/range/row

```
## <a name="request-headers"></a><span data-ttu-id="38a7e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38a7e-117">Request headers</span></span>
| <span data-ttu-id="38a7e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="38a7e-118">Name</span></span>       | <span data-ttu-id="38a7e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="38a7e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="38a7e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="38a7e-120">Authorization</span></span>  | <span data-ttu-id="38a7e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38a7e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="38a7e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="38a7e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="38a7e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="38a7e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="38a7e-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38a7e-126">Request body</span></span>
<span data-ttu-id="38a7e-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="38a7e-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="38a7e-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="38a7e-128">Parameter</span></span>    | <span data-ttu-id="38a7e-129">Type</span><span class="sxs-lookup"><span data-stu-id="38a7e-129">Type</span></span>   |<span data-ttu-id="38a7e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="38a7e-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38a7e-131">row</span><span class="sxs-lookup"><span data-stu-id="38a7e-131">row</span></span>|<span data-ttu-id="38a7e-132">Int32</span><span class="sxs-lookup"><span data-stu-id="38a7e-132">Int32</span></span>|<span data-ttu-id="38a7e-p104">Número de fila del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="38a7e-p104">Row number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="38a7e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38a7e-135">Response</span></span>

<span data-ttu-id="38a7e-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38a7e-136">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38a7e-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38a7e-137">Example</span></span>
<span data-ttu-id="38a7e-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="38a7e-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="38a7e-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38a7e-139">Request</span></span>
<span data-ttu-id="38a7e-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38a7e-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="38a7e-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38a7e-141">Response</span></span>
<span data-ttu-id="38a7e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38a7e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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