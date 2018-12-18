---
title: Get ChartSeries
description: Recuperar las propiedades y relaciones del objeto chartseries.
author: lumine2008
ms.openlocfilehash: ea89b115b2f812d4f0aaeb786096e766d97a5b1d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358180"
---
# <a name="get-chartseries"></a><span data-ttu-id="d9425-103">Get ChartSeries</span><span class="sxs-lookup"><span data-stu-id="d9425-103">Get ChartSeries</span></span>

<span data-ttu-id="d9425-104">Recuperar las propiedades y relaciones del objeto chartseries.</span><span class="sxs-lookup"><span data-stu-id="d9425-104">Retrieve the properties and relationships of chartseries object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d9425-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d9425-105">Permissions</span></span>
<span data-ttu-id="d9425-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d9425-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d9425-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d9425-108">Permission type</span></span>      | <span data-ttu-id="d9425-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d9425-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d9425-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d9425-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d9425-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9425-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d9425-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d9425-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d9425-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9425-113">Not supported.</span></span>    |
|<span data-ttu-id="d9425-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d9425-114">Application</span></span> | <span data-ttu-id="d9425-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9425-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9425-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9425-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts/{name}/series/{series-id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d9425-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d9425-117">Optional query parameters</span></span>
<span data-ttu-id="d9425-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9425-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d9425-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9425-119">Request headers</span></span>
| <span data-ttu-id="d9425-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9425-120">Name</span></span>      |<span data-ttu-id="d9425-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9425-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d9425-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9425-122">Authorization</span></span>  | <span data-ttu-id="d9425-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9425-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d9425-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d9425-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="d9425-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9425-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d9425-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9425-128">Request body</span></span>
<span data-ttu-id="d9425-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d9425-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d9425-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9425-130">Response</span></span>

<span data-ttu-id="d9425-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y [WorkbookChartSeries](../resources/chartseries.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9425-131">If successful, this method returns a `200 OK` response code and [WorkbookChartSeries](../resources/chartseries.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d9425-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9425-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d9425-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9425-133">Request</span></span>
<span data-ttu-id="d9425-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9425-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartseries"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/{series-id}
```
##### <a name="response"></a><span data-ttu-id="d9425-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9425-135">Response</span></span>
<span data-ttu-id="d9425-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d9425-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartSeries"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ChartSeries",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->