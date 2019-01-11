---
title: 'RangeSort: apply'
description: Realizar una operación de ordenación.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 563e12db5716bbc49072043578e2412b6079df03
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850914"
---
# <a name="rangesort-apply"></a><span data-ttu-id="b1b13-103">RangeSort: apply</span><span class="sxs-lookup"><span data-stu-id="b1b13-103">RangeSort: apply</span></span>

> <span data-ttu-id="b1b13-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b1b13-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b1b13-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b1b13-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b1b13-106">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b1b13-106">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="b1b13-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b1b13-107">Permissions</span></span>
<span data-ttu-id="b1b13-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b1b13-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b1b13-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b1b13-110">Permission type</span></span>      | <span data-ttu-id="b1b13-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b1b13-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b1b13-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b1b13-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b1b13-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1b13-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b1b13-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b1b13-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b1b13-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1b13-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b1b13-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b1b13-116">Application</span></span> | <span data-ttu-id="b1b13-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1b13-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b1b13-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1b13-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/sort/apply
POST /workbook/worksheets/{id|name}/range(address='<address>')/sort/apply
POST /workbook/tables/{id|name}/columns/{id|name}/range/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="b1b13-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1b13-119">Request headers</span></span>
| <span data-ttu-id="b1b13-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1b13-120">Name</span></span>       | <span data-ttu-id="b1b13-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1b13-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b1b13-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b1b13-122">Authorization</span></span>  | <span data-ttu-id="b1b13-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1b13-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b1b13-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b1b13-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="b1b13-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b1b13-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b1b13-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1b13-128">Request body</span></span>
<span data-ttu-id="b1b13-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b1b13-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b1b13-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b1b13-130">Parameter</span></span>    | <span data-ttu-id="b1b13-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1b13-131">Type</span></span>   |<span data-ttu-id="b1b13-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1b13-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b1b13-133">fields</span><span class="sxs-lookup"><span data-stu-id="b1b13-133">fields</span></span>|<span data-ttu-id="b1b13-134">SortField</span><span class="sxs-lookup"><span data-stu-id="b1b13-134">SortField</span></span>|<span data-ttu-id="b1b13-135">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="b1b13-135">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="b1b13-136">matchCase</span><span class="sxs-lookup"><span data-stu-id="b1b13-136">matchCase</span></span>|<span data-ttu-id="b1b13-137">boolean</span><span class="sxs-lookup"><span data-stu-id="b1b13-137">boolean</span></span>|<span data-ttu-id="b1b13-p105">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1b13-p105">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="b1b13-140">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="b1b13-140">hasHeaders</span></span>|<span data-ttu-id="b1b13-141">boolean</span><span class="sxs-lookup"><span data-stu-id="b1b13-141">boolean</span></span>|<span data-ttu-id="b1b13-p106">Opcional. Si el rango tiene un encabezado.</span><span class="sxs-lookup"><span data-stu-id="b1b13-p106">Optional. Whether the range has a header.</span></span>|
|<span data-ttu-id="b1b13-144">orientation</span><span class="sxs-lookup"><span data-stu-id="b1b13-144">orientation</span></span>|<span data-ttu-id="b1b13-145">string</span><span class="sxs-lookup"><span data-stu-id="b1b13-145">string</span></span>|<span data-ttu-id="b1b13-p107">Opcional. Indica si la operación ordena filas o columnas.  Valores posibles: `Rows`, `Columns`.</span><span class="sxs-lookup"><span data-stu-id="b1b13-p107">Optional. Whether the operation is sorting rows or columns.  Possible values are: `Rows`, `Columns`.</span></span>|
|<span data-ttu-id="b1b13-149">method</span><span class="sxs-lookup"><span data-stu-id="b1b13-149">method</span></span>|<span data-ttu-id="b1b13-150">string</span><span class="sxs-lookup"><span data-stu-id="b1b13-150">string</span></span>|<span data-ttu-id="b1b13-p108">Opcional. Método de ordenación que se usa para los caracteres chinos.  Valores posibles: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="b1b13-p108">Optional. The ordering method used for Chinese characters.  Possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="b1b13-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1b13-154">Response</span></span>

<span data-ttu-id="b1b13-p109">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1b13-p109">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b1b13-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1b13-157">Example</span></span>
<span data-ttu-id="b1b13-158">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b1b13-158">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b1b13-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1b13-159">Request</span></span>
<span data-ttu-id="b1b13-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1b13-160">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangesort_apply"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/sort/apply
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

##### <a name="response"></a><span data-ttu-id="b1b13-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1b13-161">Response</span></span>
<span data-ttu-id="b1b13-162">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1b13-162">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
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
