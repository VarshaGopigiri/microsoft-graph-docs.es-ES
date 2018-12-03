---
title: 'RangeSort: apply'
description: Realizar una operación de ordenación.
ms.openlocfilehash: 76432fb2614d92f5f3acbdc2261712085db5ec83
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030812"
---
# <a name="rangesort-apply"></a><span data-ttu-id="752c9-103">RangeSort: apply</span><span class="sxs-lookup"><span data-stu-id="752c9-103">RangeSort: apply</span></span>

<span data-ttu-id="752c9-104">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="752c9-104">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="752c9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="752c9-105">Permissions</span></span>
<span data-ttu-id="752c9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="752c9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="752c9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="752c9-108">Permission type</span></span>      | <span data-ttu-id="752c9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="752c9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="752c9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="752c9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="752c9-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="752c9-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="752c9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="752c9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="752c9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="752c9-113">Not supported.</span></span>    |
|<span data-ttu-id="752c9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="752c9-114">Application</span></span> | <span data-ttu-id="752c9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="752c9-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="752c9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="752c9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/sort/apply
POST /workbook/worksheets/{id|name}/range(address='<address>')/sort/apply
POST /workbook/tables/{id|name}/columns/{id|name}/range/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="752c9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="752c9-117">Request headers</span></span>
| <span data-ttu-id="752c9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="752c9-118">Name</span></span>       | <span data-ttu-id="752c9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="752c9-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="752c9-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="752c9-120">Authorization</span></span>  | <span data-ttu-id="752c9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="752c9-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="752c9-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="752c9-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="752c9-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="752c9-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="752c9-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="752c9-126">Request body</span></span>
<span data-ttu-id="752c9-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="752c9-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="752c9-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="752c9-128">Parameter</span></span>    | <span data-ttu-id="752c9-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="752c9-129">Type</span></span>   |<span data-ttu-id="752c9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="752c9-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="752c9-131">fields</span><span class="sxs-lookup"><span data-stu-id="752c9-131">fields</span></span>|<span data-ttu-id="752c9-132">Colección de WorkbookSortField</span><span class="sxs-lookup"><span data-stu-id="752c9-132">WorkbookSortField collection</span></span>|<span data-ttu-id="752c9-133">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="752c9-133">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="752c9-134">matchCase</span><span class="sxs-lookup"><span data-stu-id="752c9-134">matchCase</span></span>|<span data-ttu-id="752c9-135">boolean</span><span class="sxs-lookup"><span data-stu-id="752c9-135">boolean</span></span>|<span data-ttu-id="752c9-p104">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="752c9-p104">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="752c9-138">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="752c9-138">hasHeaders</span></span>|<span data-ttu-id="752c9-139">boolean</span><span class="sxs-lookup"><span data-stu-id="752c9-139">boolean</span></span>|<span data-ttu-id="752c9-p105">Opcional. Si el rango tiene un encabezado.</span><span class="sxs-lookup"><span data-stu-id="752c9-p105">Optional. Whether the range has a header.</span></span>|
|<span data-ttu-id="752c9-142">orientation</span><span class="sxs-lookup"><span data-stu-id="752c9-142">orientation</span></span>|<span data-ttu-id="752c9-143">string</span><span class="sxs-lookup"><span data-stu-id="752c9-143">string</span></span>|<span data-ttu-id="752c9-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="752c9-144">Optional.</span></span> <span data-ttu-id="752c9-145">Si la operación ordenar filas o columnas.</span><span class="sxs-lookup"><span data-stu-id="752c9-145">Whether the operation is sorting rows or columns.</span></span>  <span data-ttu-id="752c9-146">Los valores posibles son: `Rows`, `Columns`.</span><span class="sxs-lookup"><span data-stu-id="752c9-146">The possible values are: `Rows`, `Columns`.</span></span>|
|<span data-ttu-id="752c9-147">method</span><span class="sxs-lookup"><span data-stu-id="752c9-147">method</span></span>|<span data-ttu-id="752c9-148">string</span><span class="sxs-lookup"><span data-stu-id="752c9-148">string</span></span>|<span data-ttu-id="752c9-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="752c9-149">Optional.</span></span> <span data-ttu-id="752c9-150">El método de ordenación que se utiliza para los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="752c9-150">The ordering method used for Chinese characters.</span></span>  <span data-ttu-id="752c9-151">Los valores posibles son: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="752c9-151">The possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="752c9-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="752c9-152">Response</span></span>

<span data-ttu-id="752c9-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="752c9-p108">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="752c9-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="752c9-155">Example</span></span>
<span data-ttu-id="752c9-156">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="752c9-156">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="752c9-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="752c9-157">Request</span></span>
<span data-ttu-id="752c9-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="752c9-158">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="752c9-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="752c9-159">Response</span></span>
<span data-ttu-id="752c9-160">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="752c9-160">Here is an example of the response.</span></span> 
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