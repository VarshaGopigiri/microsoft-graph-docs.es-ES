---
title: 'TableSort: apply'
description: Realizar una operación de ordenación.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 69fda9b0a49c59a86a17e9a41eb89159085d857e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963762"
---
# <a name="tablesort-apply"></a><span data-ttu-id="28bcb-103">TableSort: apply</span><span class="sxs-lookup"><span data-stu-id="28bcb-103">TableSort: apply</span></span>

<span data-ttu-id="28bcb-104">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="28bcb-104">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="28bcb-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="28bcb-105">Permissions</span></span>
<span data-ttu-id="28bcb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="28bcb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="28bcb-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="28bcb-108">Permission type</span></span>      | <span data-ttu-id="28bcb-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="28bcb-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="28bcb-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="28bcb-110">Delegated (work or school account)</span></span> | <span data-ttu-id="28bcb-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="28bcb-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="28bcb-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="28bcb-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="28bcb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28bcb-113">Not supported.</span></span>    |
|<span data-ttu-id="28bcb-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="28bcb-114">Application</span></span> | <span data-ttu-id="28bcb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28bcb-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="28bcb-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28bcb-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="28bcb-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28bcb-117">Request headers</span></span>
| <span data-ttu-id="28bcb-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="28bcb-118">Name</span></span>       | <span data-ttu-id="28bcb-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="28bcb-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="28bcb-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="28bcb-120">Authorization</span></span>  | <span data-ttu-id="28bcb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="28bcb-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="28bcb-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="28bcb-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="28bcb-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="28bcb-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="28bcb-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28bcb-126">Request body</span></span>
<span data-ttu-id="28bcb-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="28bcb-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="28bcb-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="28bcb-128">Parameter</span></span>    | <span data-ttu-id="28bcb-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="28bcb-129">Type</span></span>   |<span data-ttu-id="28bcb-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="28bcb-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="28bcb-131">fields</span><span class="sxs-lookup"><span data-stu-id="28bcb-131">fields</span></span>|<span data-ttu-id="28bcb-132">Colección de WorkbookSortField</span><span class="sxs-lookup"><span data-stu-id="28bcb-132">WorkbookSortField collection</span></span>|<span data-ttu-id="28bcb-133">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="28bcb-133">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="28bcb-134">matchCase</span><span class="sxs-lookup"><span data-stu-id="28bcb-134">matchCase</span></span>|<span data-ttu-id="28bcb-135">boolean</span><span class="sxs-lookup"><span data-stu-id="28bcb-135">boolean</span></span>|<span data-ttu-id="28bcb-p104">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="28bcb-p104">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="28bcb-138">method</span><span class="sxs-lookup"><span data-stu-id="28bcb-138">method</span></span>|<span data-ttu-id="28bcb-139">string</span><span class="sxs-lookup"><span data-stu-id="28bcb-139">string</span></span>|<span data-ttu-id="28bcb-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="28bcb-140">Optional.</span></span> <span data-ttu-id="28bcb-141">El método de ordenación que se utiliza para los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="28bcb-141">The ordering method used for Chinese characters.</span></span>  <span data-ttu-id="28bcb-142">Los valores posibles son: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="28bcb-142">The possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="28bcb-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28bcb-143">Response</span></span>

<span data-ttu-id="28bcb-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28bcb-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="28bcb-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28bcb-146">Example</span></span>
<span data-ttu-id="28bcb-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="28bcb-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="28bcb-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28bcb-148">Request</span></span>
<span data-ttu-id="28bcb-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28bcb-149">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="28bcb-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28bcb-150">Response</span></span>
<span data-ttu-id="28bcb-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28bcb-151">Here is an example of the response.</span></span> 
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
