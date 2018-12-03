---
title: 'Chart: setData'
description: Restablece los datos de origen del gráfico.
ms.openlocfilehash: 0646bf77175fbd81feffc8c2fb26ce2179afcaa5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083048"
---
# <a name="chart-setdata"></a><span data-ttu-id="00a26-103">Chart: setData</span><span class="sxs-lookup"><span data-stu-id="00a26-103">Chart: setData</span></span>

> <span data-ttu-id="00a26-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="00a26-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="00a26-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="00a26-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="00a26-106">Restablece los datos de origen del gráfico.</span><span class="sxs-lookup"><span data-stu-id="00a26-106">Resets the source data for the chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="00a26-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="00a26-107">Permissions</span></span>
<span data-ttu-id="00a26-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="00a26-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="00a26-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00a26-110">Permission type</span></span>      | <span data-ttu-id="00a26-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00a26-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="00a26-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00a26-112">Delegated (work or school account)</span></span> | <span data-ttu-id="00a26-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="00a26-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="00a26-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00a26-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="00a26-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="00a26-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="00a26-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00a26-116">Application</span></span> | <span data-ttu-id="00a26-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00a26-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="00a26-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00a26-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/setData

```
## <a name="request-headers"></a><span data-ttu-id="00a26-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00a26-119">Request headers</span></span>
| <span data-ttu-id="00a26-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="00a26-120">Name</span></span>       | <span data-ttu-id="00a26-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="00a26-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="00a26-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="00a26-122">Authorization</span></span>  | <span data-ttu-id="00a26-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00a26-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="00a26-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="00a26-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="00a26-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="00a26-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="00a26-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00a26-128">Request body</span></span>
<span data-ttu-id="00a26-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="00a26-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="00a26-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="00a26-130">Parameter</span></span>    | <span data-ttu-id="00a26-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="00a26-131">Type</span></span>   |<span data-ttu-id="00a26-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="00a26-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="00a26-133">sourceData</span><span class="sxs-lookup"><span data-stu-id="00a26-133">sourceData</span></span>|<span data-ttu-id="00a26-134">string</span><span class="sxs-lookup"><span data-stu-id="00a26-134">string</span></span>|<span data-ttu-id="00a26-135">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="00a26-135">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="00a26-136">seriesBy</span><span class="sxs-lookup"><span data-stu-id="00a26-136">seriesBy</span></span>|<span data-ttu-id="00a26-137">string</span><span class="sxs-lookup"><span data-stu-id="00a26-137">string</span></span>|<span data-ttu-id="00a26-p105">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico. Puede ser de una de las siguientes: Auto (valor predeterminado), Rows, Columns.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="00a26-p105">Optional. Specifies the way columns or rows are used as data series on the chart. Can be one of the following: Auto (default), Rows, Columns.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="00a26-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00a26-142">Response</span></span>

<span data-ttu-id="00a26-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00a26-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="00a26-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00a26-145">Example</span></span>
<span data-ttu-id="00a26-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="00a26-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="00a26-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00a26-147">Request</span></span>
<span data-ttu-id="00a26-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00a26-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setdata"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/setData
Content-type: application/json
Content-length: 70

{
  "sourceData": "sourceData-value",
  "seriesBy": "seriesBy-value"
}
```

##### <a name="response"></a><span data-ttu-id="00a26-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00a26-149">Response</span></span>
<span data-ttu-id="00a26-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00a26-150">Here is an example of the response.</span></span> 
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
  "description": "Chart: setData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->