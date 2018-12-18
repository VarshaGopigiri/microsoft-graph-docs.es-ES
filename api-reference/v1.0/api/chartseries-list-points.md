---
title: List points
description: Recuperar una lista de objetos chartpoints.
author: lumine2008
ms.openlocfilehash: 7385c589f87604e454c8cd7e5a9cda260feb9440
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309306"
---
# <a name="list-points"></a><span data-ttu-id="82825-103">List points</span><span class="sxs-lookup"><span data-stu-id="82825-103">List points</span></span>

<span data-ttu-id="82825-104">Recuperar una lista de objetos chartpoints.</span><span class="sxs-lookup"><span data-stu-id="82825-104">Retrieve a list of chartpoints objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="82825-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="82825-105">Permissions</span></span>
<span data-ttu-id="82825-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="82825-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="82825-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="82825-108">Permission type</span></span>      | <span data-ttu-id="82825-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="82825-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="82825-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="82825-110">Delegated (work or school account)</span></span> | <span data-ttu-id="82825-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="82825-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="82825-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="82825-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="82825-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82825-113">Not supported.</span></span>    |
|<span data-ttu-id="82825-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="82825-114">Application</span></span> | <span data-ttu-id="82825-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82825-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="82825-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="82825-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points
```
## <a name="optional-query-parameters"></a><span data-ttu-id="82825-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="82825-117">Optional query parameters</span></span>
<span data-ttu-id="82825-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82825-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="82825-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="82825-119">Request headers</span></span>
| <span data-ttu-id="82825-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="82825-120">Name</span></span>      |<span data-ttu-id="82825-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="82825-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="82825-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="82825-122">Authorization</span></span>  | <span data-ttu-id="82825-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="82825-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="82825-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="82825-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="82825-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="82825-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="82825-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="82825-128">Request body</span></span>
<span data-ttu-id="82825-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="82825-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="82825-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82825-130">Response</span></span>

<span data-ttu-id="82825-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ChartPoints](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82825-131">If successful, this method returns a `200 OK` response code and collection of [ChartPoints](../resources/chartpoint.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="82825-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82825-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="82825-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="82825-133">Request</span></span>
<span data-ttu-id="82825-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="82825-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_points"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points
```
##### <a name="response"></a><span data-ttu-id="82825-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82825-135">Response</span></span>
<span data-ttu-id="82825-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="82825-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartPoint",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 32

{
  "value": [
    {
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List points",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->