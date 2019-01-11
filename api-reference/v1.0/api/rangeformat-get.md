---
title: Get RangeFormat
description: Recuperar las propiedades y relaciones del objeto rangeformat.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 123aeb715a424246f7694e5a98ae5acf1197d6dc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846168"
---
# <a name="get-rangeformat"></a><span data-ttu-id="0b45d-103">Get RangeFormat</span><span class="sxs-lookup"><span data-stu-id="0b45d-103">Get RangeFormat</span></span>

<span data-ttu-id="0b45d-104">Recuperar las propiedades y relaciones del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="0b45d-104">Retrieve the properties and relationships of rangeformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="0b45d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0b45d-105">Permissions</span></span>
<span data-ttu-id="0b45d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0b45d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0b45d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0b45d-108">Permission type</span></span>      | <span data-ttu-id="0b45d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0b45d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0b45d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0b45d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0b45d-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b45d-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0b45d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0b45d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0b45d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b45d-113">Not supported.</span></span>    |
|<span data-ttu-id="0b45d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0b45d-114">Application</span></span> | <span data-ttu-id="0b45d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b45d-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0b45d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b45d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/format
GET /workbook/worksheets/{id|name}/range(address='<address>')/format
GET /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0b45d-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0b45d-117">Optional query parameters</span></span>
<span data-ttu-id="0b45d-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b45d-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0b45d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b45d-119">Request headers</span></span>
| <span data-ttu-id="0b45d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0b45d-120">Name</span></span>      |<span data-ttu-id="0b45d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b45d-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="0b45d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0b45d-122">Authorization</span></span>  | <span data-ttu-id="0b45d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b45d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0b45d-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0b45d-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="0b45d-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0b45d-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0b45d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0b45d-128">Request body</span></span>
<span data-ttu-id="0b45d-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0b45d-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0b45d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b45d-130">Response</span></span>

<span data-ttu-id="0b45d-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y [WorkbookRangeFormat](../resources/rangeformat.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b45d-131">If successful, this method returns a `200 OK` response code and [WorkbookRangeFormat](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0b45d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b45d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0b45d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0b45d-133">Request</span></span>
<span data-ttu-id="0b45d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b45d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_rangeformat"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format
```
##### <a name="response"></a><span data-ttu-id="0b45d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b45d-135">Response</span></span>
<span data-ttu-id="0b45d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0b45d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 96

{
  "columnWidth": 99,
  "horizontalAlignment": "horizontalAlignment-value",
  "rowHeight": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get RangeFormat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
