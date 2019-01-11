---
title: List columns
description: Recuperar una lista de objetos tablecolumn.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 17e1d552c4c7880befdfb2bd8ff01d852be9a137
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811133"
---
# <a name="list-columns"></a><span data-ttu-id="7b9da-103">List columns</span><span class="sxs-lookup"><span data-stu-id="7b9da-103">List columns</span></span>

<span data-ttu-id="7b9da-104">Recuperar una lista de objetos tablecolumn.</span><span class="sxs-lookup"><span data-stu-id="7b9da-104">Retrieve a list of tablecolumn objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="7b9da-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b9da-105">Permissions</span></span>
<span data-ttu-id="7b9da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b9da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7b9da-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b9da-108">Permission type</span></span>      | <span data-ttu-id="7b9da-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b9da-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7b9da-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b9da-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7b9da-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b9da-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7b9da-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b9da-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b9da-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b9da-113">Not supported.</span></span>    |
|<span data-ttu-id="7b9da-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b9da-114">Application</span></span> | <span data-ttu-id="7b9da-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b9da-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7b9da-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b9da-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/columns
GET /workbook/worksheets/{id|name}/tables/{id|name}/columns
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7b9da-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7b9da-117">Optional query parameters</span></span>
<span data-ttu-id="7b9da-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b9da-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>  <span data-ttu-id="7b9da-119">Con los resultados de confianza, use los parámetros de consulta [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) para examinar los resultados.</span><span class="sxs-lookup"><span data-stu-id="7b9da-119">For reliable results, use the [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) query parameters to page through the results.</span></span> <span data-ttu-id="7b9da-120">Esto le ayudará a evitar problemas de rendimiento relacionados con grandes conjuntos de resultados.</span><span class="sxs-lookup"><span data-stu-id="7b9da-120">This will help avoid performance problems related to large result sets.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7b9da-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b9da-121">Request headers</span></span>
| <span data-ttu-id="7b9da-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b9da-122">Name</span></span>      |<span data-ttu-id="7b9da-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b9da-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="7b9da-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="7b9da-124">Authorization</span></span>  | <span data-ttu-id="7b9da-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b9da-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7b9da-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="7b9da-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="7b9da-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7b9da-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7b9da-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b9da-130">Request body</span></span>
<span data-ttu-id="7b9da-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7b9da-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7b9da-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b9da-132">Response</span></span>

<span data-ttu-id="7b9da-133">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [WorkbookTableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b9da-133">If successful, this method returns a `200 OK` response code and collection of [WorkbookTableColumn](../resources/tablecolumn.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7b9da-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b9da-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7b9da-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b9da-135">Request</span></span>
<span data-ttu-id="7b9da-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b9da-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_columns"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns?$top=5&$skip=5
```
##### <a name="response"></a><span data-ttu-id="7b9da-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b9da-137">Response</span></span>
<span data-ttu-id="7b9da-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b9da-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableColumn",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 126

{
  "value": [
    {
      "id": 99,
      "name": "name-value",
      "index": 99,
      "values": "values-value"
    }
  ]
}
```

> <span data-ttu-id="7b9da-141">
  \*\*Nota\*\*: Use los parámetros de consulta [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) para examinar un gran número de columnas.</span><span class="sxs-lookup"><span data-stu-id="7b9da-141">**Note:** Use the [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) query parameters to page through large numbers of columns.</span></span>

<span data-ttu-id="7b9da-142">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7b9da-142">Example:</span></span> 

`https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns?$top=5`
`https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns?$top=5&$skip=5`

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List columns",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
