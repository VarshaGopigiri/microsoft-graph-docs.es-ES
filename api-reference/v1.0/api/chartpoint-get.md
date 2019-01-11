---
title: Get ChartPoint
description: Recuperar las propiedades y relaciones del objeto chartpoint.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: c7e08d292a55891ffedcb3e39ad5dfcefeb44656
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858040"
---
# <a name="get-chartpoint"></a><span data-ttu-id="c3059-103">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="c3059-103">Get ChartPoint</span></span>

<span data-ttu-id="c3059-104">Recuperar las propiedades y relaciones del objeto chartpoint.</span><span class="sxs-lookup"><span data-stu-id="c3059-104">Retrieve the properties and relationships of chartpoint object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c3059-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3059-105">Permissions</span></span>
<span data-ttu-id="c3059-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c3059-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c3059-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3059-108">Permission type</span></span>      | <span data-ttu-id="c3059-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3059-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3059-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3059-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c3059-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c3059-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c3059-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3059-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3059-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3059-113">Not supported.</span></span>    |
|<span data-ttu-id="c3059-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3059-114">Application</span></span> | <span data-ttu-id="c3059-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3059-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c3059-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3059-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points/{point-id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c3059-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c3059-117">Optional query parameters</span></span>
<span data-ttu-id="c3059-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3059-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c3059-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3059-119">Request headers</span></span>
| <span data-ttu-id="c3059-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c3059-120">Name</span></span>      |<span data-ttu-id="c3059-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3059-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c3059-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3059-122">Authorization</span></span>  | <span data-ttu-id="c3059-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3059-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c3059-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c3059-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="c3059-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c3059-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c3059-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c3059-128">Request body</span></span>
<span data-ttu-id="c3059-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c3059-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c3059-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3059-130">Response</span></span>

<span data-ttu-id="c3059-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y [WorkbookChartPoint](../resources/chartpoint.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3059-131">If successful, this method returns a `200 OK` response code and [WorkbookChartPoint](../resources/chartpoint.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c3059-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3059-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c3059-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3059-133">Request</span></span>
<span data-ttu-id="c3059-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c3059-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartpoint"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points/{point-id}
```
##### <a name="response"></a><span data-ttu-id="c3059-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3059-135">Response</span></span>
<span data-ttu-id="c3059-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c3059-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartPoint"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 20

{
  "value": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ChartPoint",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
