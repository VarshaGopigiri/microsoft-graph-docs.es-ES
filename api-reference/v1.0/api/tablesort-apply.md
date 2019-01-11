---
title: 'TableSort: apply'
description: Realizar una operación de ordenación.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 682cacd558d42cc32b092bd7421aa14967f9c5b6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877045"
---
# <a name="tablesort-apply"></a><span data-ttu-id="9b67e-103">TableSort: apply</span><span class="sxs-lookup"><span data-stu-id="9b67e-103">TableSort: apply</span></span>

<span data-ttu-id="9b67e-104">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="9b67e-104">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="9b67e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b67e-105">Permissions</span></span>
<span data-ttu-id="9b67e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b67e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b67e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b67e-108">Permission type</span></span>      | <span data-ttu-id="9b67e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b67e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b67e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b67e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9b67e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b67e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9b67e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b67e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b67e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b67e-113">Not supported.</span></span>    |
|<span data-ttu-id="9b67e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b67e-114">Application</span></span> | <span data-ttu-id="9b67e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b67e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b67e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b67e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="9b67e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b67e-117">Request headers</span></span>
| <span data-ttu-id="9b67e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b67e-118">Name</span></span>       | <span data-ttu-id="9b67e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b67e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9b67e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b67e-120">Authorization</span></span>  | <span data-ttu-id="9b67e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b67e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9b67e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9b67e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="9b67e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="9b67e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b67e-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b67e-126">Request body</span></span>
<span data-ttu-id="9b67e-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b67e-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9b67e-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9b67e-128">Parameter</span></span>    | <span data-ttu-id="9b67e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b67e-129">Type</span></span>   |<span data-ttu-id="9b67e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b67e-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9b67e-131">fields</span><span class="sxs-lookup"><span data-stu-id="9b67e-131">fields</span></span>|<span data-ttu-id="9b67e-132">Colección de WorkbookSortField</span><span class="sxs-lookup"><span data-stu-id="9b67e-132">WorkbookSortField collection</span></span>|<span data-ttu-id="9b67e-133">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="9b67e-133">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="9b67e-134">matchCase</span><span class="sxs-lookup"><span data-stu-id="9b67e-134">matchCase</span></span>|<span data-ttu-id="9b67e-135">boolean</span><span class="sxs-lookup"><span data-stu-id="9b67e-135">boolean</span></span>|<span data-ttu-id="9b67e-p104">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9b67e-p104">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="9b67e-138">method</span><span class="sxs-lookup"><span data-stu-id="9b67e-138">method</span></span>|<span data-ttu-id="9b67e-139">string</span><span class="sxs-lookup"><span data-stu-id="9b67e-139">string</span></span>|<span data-ttu-id="9b67e-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9b67e-140">Optional.</span></span> <span data-ttu-id="9b67e-141">El método de ordenación que se utiliza para los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="9b67e-141">The ordering method used for Chinese characters.</span></span>  <span data-ttu-id="9b67e-142">Los valores posibles son: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="9b67e-142">The possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="9b67e-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b67e-143">Response</span></span>

<span data-ttu-id="9b67e-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b67e-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b67e-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b67e-146">Example</span></span>
<span data-ttu-id="9b67e-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9b67e-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9b67e-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b67e-148">Request</span></span>
<span data-ttu-id="9b67e-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b67e-149">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="9b67e-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b67e-150">Response</span></span>
<span data-ttu-id="9b67e-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b67e-151">Here is an example of the response.</span></span> 
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
