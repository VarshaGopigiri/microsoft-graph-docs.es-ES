---
title: 'RangeSort: apply'
description: Realizar una operación de ordenación.
author: lumine2008
ms.openlocfilehash: 98585be62b8aa227ea5e648d1e24e2a09cb023d9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352111"
---
# <a name="rangesort-apply"></a><span data-ttu-id="cc029-103">RangeSort: apply</span><span class="sxs-lookup"><span data-stu-id="cc029-103">RangeSort: apply</span></span>

<span data-ttu-id="cc029-104">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="cc029-104">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="cc029-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="cc029-105">Permissions</span></span>
<span data-ttu-id="cc029-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc029-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc029-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc029-108">Permission type</span></span>      | <span data-ttu-id="cc029-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc029-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc029-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc029-110">Delegated (work or school account)</span></span> | <span data-ttu-id="cc029-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cc029-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="cc029-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc029-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc029-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc029-113">Not supported.</span></span>    |
|<span data-ttu-id="cc029-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc029-114">Application</span></span> | <span data-ttu-id="cc029-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc029-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc029-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc029-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/sort/apply
POST /workbook/worksheets/{id|name}/range(address='<address>')/sort/apply
POST /workbook/tables/{id|name}/columns/{id|name}/range/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="cc029-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc029-117">Request headers</span></span>
| <span data-ttu-id="cc029-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc029-118">Name</span></span>       | <span data-ttu-id="cc029-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc029-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="cc029-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc029-120">Authorization</span></span>  | <span data-ttu-id="cc029-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc029-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cc029-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="cc029-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="cc029-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="cc029-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="cc029-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc029-126">Request body</span></span>
<span data-ttu-id="cc029-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="cc029-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="cc029-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cc029-128">Parameter</span></span>    | <span data-ttu-id="cc029-129">Type</span><span class="sxs-lookup"><span data-stu-id="cc029-129">Type</span></span>   |<span data-ttu-id="cc029-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc029-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cc029-131">fields</span><span class="sxs-lookup"><span data-stu-id="cc029-131">fields</span></span>|<span data-ttu-id="cc029-132">Colección de WorkbookSortField</span><span class="sxs-lookup"><span data-stu-id="cc029-132">WorkbookSortField collection</span></span>|<span data-ttu-id="cc029-133">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="cc029-133">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="cc029-134">matchCase</span><span class="sxs-lookup"><span data-stu-id="cc029-134">matchCase</span></span>|<span data-ttu-id="cc029-135">boolean</span><span class="sxs-lookup"><span data-stu-id="cc029-135">boolean</span></span>|<span data-ttu-id="cc029-p104">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cc029-p104">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="cc029-138">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="cc029-138">hasHeaders</span></span>|<span data-ttu-id="cc029-139">boolean</span><span class="sxs-lookup"><span data-stu-id="cc029-139">boolean</span></span>|<span data-ttu-id="cc029-p105">Opcional. Si el rango tiene un encabezado.</span><span class="sxs-lookup"><span data-stu-id="cc029-p105">Optional. Whether the range has a header.</span></span>|
|<span data-ttu-id="cc029-142">orientation</span><span class="sxs-lookup"><span data-stu-id="cc029-142">orientation</span></span>|<span data-ttu-id="cc029-143">string</span><span class="sxs-lookup"><span data-stu-id="cc029-143">string</span></span>|<span data-ttu-id="cc029-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cc029-144">Optional.</span></span> <span data-ttu-id="cc029-145">Si la operación ordenar filas o columnas.</span><span class="sxs-lookup"><span data-stu-id="cc029-145">Whether the operation is sorting rows or columns.</span></span>  <span data-ttu-id="cc029-146">Los valores posibles son: `Rows`, `Columns`.</span><span class="sxs-lookup"><span data-stu-id="cc029-146">The possible values are: `Rows`, `Columns`.</span></span>|
|<span data-ttu-id="cc029-147">method</span><span class="sxs-lookup"><span data-stu-id="cc029-147">method</span></span>|<span data-ttu-id="cc029-148">string</span><span class="sxs-lookup"><span data-stu-id="cc029-148">string</span></span>|<span data-ttu-id="cc029-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cc029-149">Optional.</span></span> <span data-ttu-id="cc029-150">El método de ordenación que se utiliza para los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="cc029-150">The ordering method used for Chinese characters.</span></span>  <span data-ttu-id="cc029-151">Los valores posibles son: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="cc029-151">The possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="cc029-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc029-152">Response</span></span>

<span data-ttu-id="cc029-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc029-p108">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc029-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc029-155">Example</span></span>
<span data-ttu-id="cc029-156">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="cc029-156">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="cc029-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc029-157">Request</span></span>
<span data-ttu-id="cc029-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc029-158">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangesort_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/sort/apply
Content-type: application/json
Content-length: 358

{
  "fields": [
    {
      "key": 99,
      "sortOn": "sortOn-value",
      "ascending": true,
      "color": "color-value",
      "dataOption": "dataOption-value",
      "icon": {
        "set": "set-value",
        "index": 99
      }
    }
  ],
  "matchCase": true,
  "hasHeaders": true,
  "orientation": "orientation-value",
  "method": "method-value"
}
```

##### <a name="response"></a><span data-ttu-id="cc029-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc029-159">Response</span></span>
<span data-ttu-id="cc029-160">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc029-160">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeSort: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->