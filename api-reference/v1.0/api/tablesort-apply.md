---
title: 'TableSort: apply'
description: Realizar una operación de ordenación.
author: lumine2008
ms.openlocfilehash: d3e19dbd1ed77f32a215dfa165ebc796706b09a6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309684"
---
# <a name="tablesort-apply"></a><span data-ttu-id="f76f4-103">TableSort: apply</span><span class="sxs-lookup"><span data-stu-id="f76f4-103">TableSort: apply</span></span>

<span data-ttu-id="f76f4-104">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="f76f4-104">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="f76f4-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f76f4-105">Permissions</span></span>
<span data-ttu-id="f76f4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f76f4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f76f4-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f76f4-108">Permission type</span></span>      | <span data-ttu-id="f76f4-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f76f4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f76f4-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f76f4-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f76f4-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f76f4-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f76f4-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f76f4-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f76f4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f76f4-113">Not supported.</span></span>    |
|<span data-ttu-id="f76f4-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f76f4-114">Application</span></span> | <span data-ttu-id="f76f4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f76f4-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f76f4-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f76f4-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="f76f4-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f76f4-117">Request headers</span></span>
| <span data-ttu-id="f76f4-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f76f4-118">Name</span></span>       | <span data-ttu-id="f76f4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f76f4-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f76f4-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f76f4-120">Authorization</span></span>  | <span data-ttu-id="f76f4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f76f4-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f76f4-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f76f4-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="f76f4-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f76f4-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f76f4-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f76f4-126">Request body</span></span>
<span data-ttu-id="f76f4-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f76f4-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f76f4-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f76f4-128">Parameter</span></span>    | <span data-ttu-id="f76f4-129">Type</span><span class="sxs-lookup"><span data-stu-id="f76f4-129">Type</span></span>   |<span data-ttu-id="f76f4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f76f4-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f76f4-131">fields</span><span class="sxs-lookup"><span data-stu-id="f76f4-131">fields</span></span>|<span data-ttu-id="f76f4-132">Colección de WorkbookSortField</span><span class="sxs-lookup"><span data-stu-id="f76f4-132">WorkbookSortField collection</span></span>|<span data-ttu-id="f76f4-133">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="f76f4-133">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="f76f4-134">matchCase</span><span class="sxs-lookup"><span data-stu-id="f76f4-134">matchCase</span></span>|<span data-ttu-id="f76f4-135">boolean</span><span class="sxs-lookup"><span data-stu-id="f76f4-135">boolean</span></span>|<span data-ttu-id="f76f4-p104">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f76f4-p104">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="f76f4-138">method</span><span class="sxs-lookup"><span data-stu-id="f76f4-138">method</span></span>|<span data-ttu-id="f76f4-139">string</span><span class="sxs-lookup"><span data-stu-id="f76f4-139">string</span></span>|<span data-ttu-id="f76f4-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f76f4-140">Optional.</span></span> <span data-ttu-id="f76f4-141">El método de ordenación que se utiliza para los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="f76f4-141">The ordering method used for Chinese characters.</span></span>  <span data-ttu-id="f76f4-142">Los valores posibles son: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="f76f4-142">The possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="f76f4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f76f4-143">Response</span></span>

<span data-ttu-id="f76f4-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f76f4-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f76f4-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f76f4-146">Example</span></span>
<span data-ttu-id="f76f4-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f76f4-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f76f4-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f76f4-148">Request</span></span>
<span data-ttu-id="f76f4-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f76f4-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/apply
Content-type: application/json
Content-length: 298

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
  "method": "method-value"
}
```

##### <a name="response"></a><span data-ttu-id="f76f4-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f76f4-150">Response</span></span>
<span data-ttu-id="f76f4-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f76f4-151">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->