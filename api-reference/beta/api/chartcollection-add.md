---
title: 'ChartCollection: add'
description: Crea un nuevo gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 19ab5936b563fc491e08923d257d334d9932af98
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936581"
---
# <a name="chartcollection-add"></a><span data-ttu-id="b7c24-103">ChartCollection: add</span><span class="sxs-lookup"><span data-stu-id="b7c24-103">ChartCollection: add</span></span>

> <span data-ttu-id="b7c24-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b7c24-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b7c24-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b7c24-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b7c24-106">Crea un nuevo gráfico.</span><span class="sxs-lookup"><span data-stu-id="b7c24-106">Creates a new chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="b7c24-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7c24-107">Permissions</span></span>
<span data-ttu-id="b7c24-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7c24-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7c24-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7c24-110">Permission type</span></span>      | <span data-ttu-id="b7c24-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7c24-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b7c24-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7c24-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b7c24-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b7c24-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b7c24-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7c24-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b7c24-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b7c24-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b7c24-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7c24-116">Application</span></span> | <span data-ttu-id="b7c24-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7c24-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b7c24-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7c24-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/add

```
## <a name="request-headers"></a><span data-ttu-id="b7c24-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7c24-119">Request headers</span></span>
| <span data-ttu-id="b7c24-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b7c24-120">Name</span></span>       | <span data-ttu-id="b7c24-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7c24-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b7c24-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b7c24-122">Authorization</span></span>  | <span data-ttu-id="b7c24-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7c24-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b7c24-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b7c24-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="b7c24-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b7c24-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b7c24-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7c24-128">Request body</span></span>
<span data-ttu-id="b7c24-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b7c24-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b7c24-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b7c24-130">Parameter</span></span>    | <span data-ttu-id="b7c24-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7c24-131">Type</span></span>   |<span data-ttu-id="b7c24-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7c24-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b7c24-133">type</span><span class="sxs-lookup"><span data-stu-id="b7c24-133">type</span></span>|<span data-ttu-id="b7c24-134">string</span><span class="sxs-lookup"><span data-stu-id="b7c24-134">string</span></span>|<span data-ttu-id="b7c24-p105">Representa el tipo de un gráfico.  Valores posibles: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span><span class="sxs-lookup"><span data-stu-id="b7c24-p105">Represents the type of a chart.  Possible values are: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span></span>|
|<span data-ttu-id="b7c24-137">sourceData</span><span class="sxs-lookup"><span data-stu-id="b7c24-137">sourceData</span></span>|<span data-ttu-id="b7c24-138">string</span><span class="sxs-lookup"><span data-stu-id="b7c24-138">string</span></span>|<span data-ttu-id="b7c24-139">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="b7c24-139">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="b7c24-140">seriesBy</span><span class="sxs-lookup"><span data-stu-id="b7c24-140">seriesBy</span></span>|<span data-ttu-id="b7c24-141">string</span><span class="sxs-lookup"><span data-stu-id="b7c24-141">string</span></span>|<span data-ttu-id="b7c24-p106">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="b7c24-p106">Optional. Specifies the way columns or rows are used as data series on the chart.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="b7c24-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7c24-145">Response</span></span>

<span data-ttu-id="b7c24-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Chart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7c24-146">If successful, this method returns `200 OK` response code and [Chart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b7c24-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7c24-147">Example</span></span>
<span data-ttu-id="b7c24-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b7c24-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b7c24-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7c24-149">Request</span></span>
<span data-ttu-id="b7c24-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7c24-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartcollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/add
Content-type: application/json
Content-length: 94

{
  "type": "ColumnStacked",
  "sourceData": "A1:B1",
  "seriesBy": "Auto"
}
```

##### <a name="response"></a><span data-ttu-id="b7c24-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7c24-151">Response</span></span>
<span data-ttu-id="b7c24-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b7c24-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chart"
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
