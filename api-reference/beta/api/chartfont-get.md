---
title: Get ChartFont
description: Recuperar las propiedades y relaciones del objeto chartfont.
author: lumine2008
ms.openlocfilehash: 2a40686b95e1cd30ca51c177c692ead08a62a7f5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316516"
---
# <a name="get-chartfont"></a><span data-ttu-id="068ca-103">Get ChartFont</span><span class="sxs-lookup"><span data-stu-id="068ca-103">Get ChartFont</span></span>

> <span data-ttu-id="068ca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="068ca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="068ca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="068ca-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="068ca-106">Recuperar las propiedades y relaciones del objeto chartfont.</span><span class="sxs-lookup"><span data-stu-id="068ca-106">Retrieve the properties and relationships of chartfont object.</span></span>
## <a name="permissions"></a><span data-ttu-id="068ca-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="068ca-107">Permissions</span></span>
<span data-ttu-id="068ca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="068ca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="068ca-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="068ca-110">Permission type</span></span>      | <span data-ttu-id="068ca-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="068ca-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="068ca-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="068ca-112">Delegated (work or school account)</span></span> | <span data-ttu-id="068ca-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="068ca-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="068ca-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="068ca-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="068ca-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="068ca-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="068ca-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="068ca-116">Application</span></span> | <span data-ttu-id="068ca-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="068ca-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="068ca-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="068ca-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/format/font
GET /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/format/font
GET /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/format/font
```
## <a name="optional-query-parameters"></a><span data-ttu-id="068ca-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="068ca-119">Optional query parameters</span></span>
<span data-ttu-id="068ca-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="068ca-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="068ca-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="068ca-121">Request headers</span></span>
| <span data-ttu-id="068ca-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="068ca-122">Name</span></span>      |<span data-ttu-id="068ca-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="068ca-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="068ca-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="068ca-124">Authorization</span></span>  | <span data-ttu-id="068ca-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="068ca-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="068ca-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="068ca-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="068ca-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="068ca-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="068ca-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="068ca-130">Request body</span></span>
<span data-ttu-id="068ca-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="068ca-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="068ca-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="068ca-132">Response</span></span>

<span data-ttu-id="068ca-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartFont](../resources/chartfont.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="068ca-133">If successful, this method returns a `200 OK` response code and [ChartFont](../resources/chartfont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="068ca-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="068ca-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="068ca-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="068ca-135">Request</span></span>
<span data-ttu-id="068ca-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="068ca-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartfont"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/format/font
```
##### <a name="response"></a><span data-ttu-id="068ca-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="068ca-137">Response</span></span>
<span data-ttu-id="068ca-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="068ca-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartFont"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "bold": true,
  "color": "color-value",
  "italic": true,
  "name": "name-value",
  "size": 99,
  "underline": "underline-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ChartFont",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->