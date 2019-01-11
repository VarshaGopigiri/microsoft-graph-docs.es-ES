---
title: List ChartCollection
description: Recuperar una lista de objetos chart.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 9df91acc1d189e57154e130db9fe9b4d5910198a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839651"
---
# <a name="list-chartcollection"></a><span data-ttu-id="465da-103">List ChartCollection</span><span class="sxs-lookup"><span data-stu-id="465da-103">List ChartCollection</span></span>

<span data-ttu-id="465da-104">Recuperar una lista de objetos chart.</span><span class="sxs-lookup"><span data-stu-id="465da-104">Retrieve a list of chart objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="465da-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="465da-105">Permissions</span></span>
<span data-ttu-id="465da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="465da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="465da-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="465da-108">Permission type</span></span>      | <span data-ttu-id="465da-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="465da-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="465da-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="465da-110">Delegated (work or school account)</span></span> | <span data-ttu-id="465da-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="465da-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="465da-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="465da-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="465da-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="465da-113">Not supported.</span></span>    |
|<span data-ttu-id="465da-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="465da-114">Application</span></span> | <span data-ttu-id="465da-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="465da-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="465da-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="465da-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="465da-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="465da-117">Optional query parameters</span></span>
<span data-ttu-id="465da-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="465da-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="465da-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="465da-119">Request headers</span></span>
| <span data-ttu-id="465da-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="465da-120">Name</span></span>      |<span data-ttu-id="465da-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="465da-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="465da-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="465da-122">Authorization</span></span>  | <span data-ttu-id="465da-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="465da-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="465da-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="465da-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="465da-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="465da-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="465da-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="465da-128">Request body</span></span>
<span data-ttu-id="465da-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="465da-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="465da-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="465da-130">Response</span></span>

<span data-ttu-id="465da-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [WorkbookChart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="465da-131">If successful, this method returns a `200 OK` response code and collection of [WorkbookChart](../resources/chart.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="465da-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="465da-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="465da-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="465da-133">Request</span></span>
<span data-ttu-id="465da-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="465da-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartcollection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts
```
##### <a name="response"></a><span data-ttu-id="465da-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="465da-135">Response</span></span>
<span data-ttu-id="465da-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="465da-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 93

{
  "value": [
    {
      "id": "id-value",
      "height": 99,
      "left": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List ChartCollection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
