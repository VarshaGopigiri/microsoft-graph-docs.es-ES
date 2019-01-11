---
title: 'Chart: setData'
description: Restablece los datos de origen del gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: b295b38df2cf7be1c568588d58bfb2cf529f4dc4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858152"
---
# <a name="chart-setdata"></a><span data-ttu-id="2fba0-103">Chart: setData</span><span class="sxs-lookup"><span data-stu-id="2fba0-103">Chart: setData</span></span>

<span data-ttu-id="2fba0-104">Restablece los datos de origen del gráfico.</span><span class="sxs-lookup"><span data-stu-id="2fba0-104">Resets the source data for the chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="2fba0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2fba0-105">Permissions</span></span>
<span data-ttu-id="2fba0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2fba0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2fba0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2fba0-108">Permission type</span></span>      | <span data-ttu-id="2fba0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2fba0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2fba0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2fba0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2fba0-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2fba0-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2fba0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2fba0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2fba0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2fba0-113">Not supported.</span></span>    |
|<span data-ttu-id="2fba0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2fba0-114">Application</span></span> | <span data-ttu-id="2fba0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2fba0-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2fba0-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2fba0-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/setData

```
## <a name="request-headers"></a><span data-ttu-id="2fba0-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2fba0-117">Request headers</span></span>
| <span data-ttu-id="2fba0-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2fba0-118">Name</span></span>       | <span data-ttu-id="2fba0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fba0-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2fba0-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="2fba0-120">Authorization</span></span>  | <span data-ttu-id="2fba0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2fba0-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2fba0-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2fba0-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="2fba0-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2fba0-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2fba0-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2fba0-126">Request body</span></span>
<span data-ttu-id="2fba0-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2fba0-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2fba0-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2fba0-128">Parameter</span></span>    | <span data-ttu-id="2fba0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fba0-129">Type</span></span>   |<span data-ttu-id="2fba0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fba0-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2fba0-131">sourceData</span><span class="sxs-lookup"><span data-stu-id="2fba0-131">sourceData</span></span>|<span data-ttu-id="2fba0-132">Json</span><span class="sxs-lookup"><span data-stu-id="2fba0-132">Json</span></span>|<span data-ttu-id="2fba0-133">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="2fba0-133">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="2fba0-134">seriesBy</span><span class="sxs-lookup"><span data-stu-id="2fba0-134">seriesBy</span></span>|<span data-ttu-id="2fba0-135">string</span><span class="sxs-lookup"><span data-stu-id="2fba0-135">string</span></span>|<span data-ttu-id="2fba0-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2fba0-136">Optional.</span></span> <span data-ttu-id="2fba0-137">Especifica las filas o columnas de forma que se usan como series de datos en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="2fba0-137">Specifies the way columns or rows are used as data series on the chart.</span></span> <span data-ttu-id="2fba0-138">Puede ser una de las siguientes opciones: automático (valor predeterminado), filas, columnas.</span><span class="sxs-lookup"><span data-stu-id="2fba0-138">Can be one of the following: Auto (default), Rows, Columns.</span></span>  <span data-ttu-id="2fba0-139">Los valores posibles son: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="2fba0-139">The possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="2fba0-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2fba0-140">Response</span></span>

<span data-ttu-id="2fba0-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2fba0-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2fba0-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2fba0-143">Example</span></span>
<span data-ttu-id="2fba0-144">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2fba0-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2fba0-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2fba0-145">Request</span></span>
<span data-ttu-id="2fba0-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2fba0-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setdata"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setData
Content-type: application/json
Content-length: 70

{
  "sourceData": "sourceData-value",
  "seriesBy": "seriesBy-value"
}
```

##### <a name="response"></a><span data-ttu-id="2fba0-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2fba0-147">Response</span></span>
<span data-ttu-id="2fba0-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2fba0-148">Here is an example of the response.</span></span> 
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
  "description": "Chart: setData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
