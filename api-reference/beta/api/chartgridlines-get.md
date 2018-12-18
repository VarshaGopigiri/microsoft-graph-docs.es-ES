---
title: Get ChartGridlines
description: Recuperar las propiedades y relaciones del objeto chartgridlines.
author: lumine2008
ms.openlocfilehash: aae489ec766f7a3f03407915ad2a01f60ca13f8c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343515"
---
# <a name="get-chartgridlines"></a><span data-ttu-id="cac30-103">Get ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="cac30-103">Get ChartGridlines</span></span>

> <span data-ttu-id="cac30-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cac30-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cac30-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cac30-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cac30-106">Recuperar las propiedades y relaciones del objeto chartgridlines.</span><span class="sxs-lookup"><span data-stu-id="cac30-106">Retrieve the properties and relationships of chartgridlines object.</span></span>
## <a name="permissions"></a><span data-ttu-id="cac30-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cac30-107">Permissions</span></span>
<span data-ttu-id="cac30-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cac30-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cac30-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cac30-110">Permission type</span></span>      | <span data-ttu-id="cac30-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cac30-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cac30-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cac30-112">Delegated (work or school account)</span></span> | <span data-ttu-id="cac30-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cac30-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="cac30-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cac30-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cac30-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cac30-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="cac30-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cac30-116">Application</span></span> | <span data-ttu-id="cac30-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cac30-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="cac30-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cac30-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/minorgridlines
GET /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/majorgridlines
GET /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/majorgridlines
```
## <a name="optional-query-parameters"></a><span data-ttu-id="cac30-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cac30-119">Optional query parameters</span></span>
<span data-ttu-id="cac30-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cac30-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cac30-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cac30-121">Request headers</span></span>
| <span data-ttu-id="cac30-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="cac30-122">Name</span></span>      |<span data-ttu-id="cac30-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="cac30-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="cac30-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="cac30-124">Authorization</span></span>  | <span data-ttu-id="cac30-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cac30-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cac30-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="cac30-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="cac30-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="cac30-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="cac30-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cac30-130">Request body</span></span>
<span data-ttu-id="cac30-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cac30-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cac30-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cac30-132">Response</span></span>

<span data-ttu-id="cac30-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartGridlines](../resources/chartgridlines.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cac30-133">If successful, this method returns a `200 OK` response code and [ChartGridlines](../resources/chartgridlines.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cac30-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cac30-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cac30-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cac30-135">Request</span></span>
<span data-ttu-id="cac30-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cac30-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartgridlines"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/minorgridlines
```
##### <a name="response"></a><span data-ttu-id="cac30-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cac30-137">Response</span></span>
<span data-ttu-id="cac30-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cac30-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartGridLines"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 21

{
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ChartGridlines",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->