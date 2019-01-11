---
title: 'ChartCollection: add'
description: Crea un nuevo gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 4aa1a017da88fdd06b8e396130d5b09fbbeaebb5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867945"
---
# <a name="chartcollection-add"></a><span data-ttu-id="0ca93-103">ChartCollection: add</span><span class="sxs-lookup"><span data-stu-id="0ca93-103">ChartCollection: add</span></span>

<span data-ttu-id="0ca93-104">Crea un nuevo gráfico.</span><span class="sxs-lookup"><span data-stu-id="0ca93-104">Creates a new chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="0ca93-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0ca93-105">Permissions</span></span>
<span data-ttu-id="0ca93-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0ca93-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0ca93-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0ca93-108">Permission type</span></span>      | <span data-ttu-id="0ca93-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0ca93-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0ca93-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0ca93-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0ca93-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0ca93-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0ca93-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0ca93-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0ca93-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ca93-113">Not supported.</span></span>    |
|<span data-ttu-id="0ca93-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0ca93-114">Application</span></span> | <span data-ttu-id="0ca93-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ca93-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0ca93-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0ca93-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/add

```
## <a name="request-headers"></a><span data-ttu-id="0ca93-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0ca93-117">Request headers</span></span>
| <span data-ttu-id="0ca93-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="0ca93-118">Name</span></span>       | <span data-ttu-id="0ca93-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ca93-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0ca93-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="0ca93-120">Authorization</span></span>  | <span data-ttu-id="0ca93-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0ca93-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0ca93-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0ca93-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="0ca93-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0ca93-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0ca93-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0ca93-126">Request body</span></span>
<span data-ttu-id="0ca93-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0ca93-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0ca93-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0ca93-128">Parameter</span></span>    | <span data-ttu-id="0ca93-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ca93-129">Type</span></span>   |<span data-ttu-id="0ca93-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ca93-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0ca93-131">type</span><span class="sxs-lookup"><span data-stu-id="0ca93-131">type</span></span>|<span data-ttu-id="0ca93-132">string</span><span class="sxs-lookup"><span data-stu-id="0ca93-132">string</span></span>|<span data-ttu-id="0ca93-133">Representa el tipo de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="0ca93-133">Represents the type of a chart.</span></span>  <span data-ttu-id="0ca93-134">Los valores posibles son: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span><span class="sxs-lookup"><span data-stu-id="0ca93-134">The possible values are: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span></span>|
|<span data-ttu-id="0ca93-135">sourceData</span><span class="sxs-lookup"><span data-stu-id="0ca93-135">sourceData</span></span>|<span data-ttu-id="0ca93-136">Json</span><span class="sxs-lookup"><span data-stu-id="0ca93-136">Json</span></span>|<span data-ttu-id="0ca93-137">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="0ca93-137">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="0ca93-138">seriesBy</span><span class="sxs-lookup"><span data-stu-id="0ca93-138">seriesBy</span></span>|<span data-ttu-id="0ca93-139">string</span><span class="sxs-lookup"><span data-stu-id="0ca93-139">string</span></span>|<span data-ttu-id="0ca93-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0ca93-140">Optional.</span></span> <span data-ttu-id="0ca93-141">Especifica las filas o columnas de forma que se usan como series de datos en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="0ca93-141">Specifies the way columns or rows are used as data series on the chart.</span></span>  <span data-ttu-id="0ca93-142">Los valores posibles son: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="0ca93-142">The possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="0ca93-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ca93-143">Response</span></span>

<span data-ttu-id="0ca93-144">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookChart](../resources/chart.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ca93-144">If successful, this method returns `200 OK` response code and [WorkbookChart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0ca93-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0ca93-145">Example</span></span>
<span data-ttu-id="0ca93-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0ca93-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0ca93-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0ca93-147">Request</span></span>
<span data-ttu-id="0ca93-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ca93-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/add
Content-type: application/json
Content-length: 94

{
  "type": "ColumnStacked",
  "sourceData": "A1:B1",
  "seriesBy": "Auto"
}
```

##### <a name="response"></a><span data-ttu-id="0ca93-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ca93-149">Response</span></span>
<span data-ttu-id="0ca93-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0ca93-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
