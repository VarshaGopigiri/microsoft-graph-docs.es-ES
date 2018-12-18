---
title: List ChartSeriesCollection
description: Recuperar una lista de objetos chartseries.
author: lumine2008
ms.openlocfilehash: 6f3fa59def5632fe76de16f22adcee5c6ce727e0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328129"
---
# <a name="list-chartseriescollection"></a><span data-ttu-id="58272-103">List ChartSeriesCollection</span><span class="sxs-lookup"><span data-stu-id="58272-103">List ChartSeriesCollection</span></span>

> <span data-ttu-id="58272-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58272-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58272-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58272-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="58272-106">Recuperar una lista de objetos chartseries.</span><span class="sxs-lookup"><span data-stu-id="58272-106">Retrieve a list of chartseries objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="58272-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="58272-107">Permissions</span></span>
<span data-ttu-id="58272-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="58272-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="58272-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="58272-110">Permission type</span></span>      | <span data-ttu-id="58272-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="58272-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="58272-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="58272-112">Delegated (work or school account)</span></span> | <span data-ttu-id="58272-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58272-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="58272-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58272-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="58272-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58272-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="58272-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="58272-116">Application</span></span> | <span data-ttu-id="58272-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="58272-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="58272-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58272-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/series
```
## <a name="optional-query-parameters"></a><span data-ttu-id="58272-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="58272-119">Optional query parameters</span></span>
<span data-ttu-id="58272-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58272-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="58272-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58272-121">Request headers</span></span>
| <span data-ttu-id="58272-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="58272-122">Name</span></span>      |<span data-ttu-id="58272-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="58272-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="58272-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="58272-124">Authorization</span></span>  | <span data-ttu-id="58272-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58272-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="58272-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="58272-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="58272-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="58272-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="58272-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="58272-130">Request body</span></span>
<span data-ttu-id="58272-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="58272-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="58272-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58272-132">Response</span></span>

<span data-ttu-id="58272-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ChartSeries](../resources/chartseries.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58272-133">If successful, this method returns a `200 OK` response code and collection of [ChartSeries](../resources/chartseries.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="58272-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58272-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="58272-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58272-135">Request</span></span>
<span data-ttu-id="58272-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58272-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartseriescollection"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series
```
##### <a name="response"></a><span data-ttu-id="58272-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58272-137">Response</span></span>
<span data-ttu-id="58272-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="58272-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartSeries",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 59

{
  "value": [
    {
      "name": "name-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List ChartSeriesCollection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->