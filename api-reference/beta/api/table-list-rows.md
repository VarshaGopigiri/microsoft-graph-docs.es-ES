---
title: List rows
description: Recuperar una lista de objetos tablerow.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 48455cf2700672c7363b591d0963a8c97830be29
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838321"
---
# <a name="list-rows"></a><span data-ttu-id="91b25-103">List rows</span><span class="sxs-lookup"><span data-stu-id="91b25-103">List rows</span></span>

> <span data-ttu-id="91b25-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="91b25-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="91b25-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="91b25-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="91b25-106">Recuperar una lista de objetos tablerow.</span><span class="sxs-lookup"><span data-stu-id="91b25-106">Retrieve a list of tablerow objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="91b25-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="91b25-107">Permissions</span></span>
<span data-ttu-id="91b25-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="91b25-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="91b25-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="91b25-110">Permission type</span></span>      | <span data-ttu-id="91b25-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="91b25-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="91b25-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="91b25-112">Delegated (work or school account)</span></span> | <span data-ttu-id="91b25-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="91b25-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="91b25-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="91b25-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="91b25-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="91b25-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="91b25-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="91b25-116">Application</span></span> | <span data-ttu-id="91b25-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="91b25-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="91b25-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="91b25-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/rows
GET /workbook/worksheets/{id|name}/tables/{id|name}/rows
```
## <a name="optional-query-parameters"></a><span data-ttu-id="91b25-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="91b25-119">Optional query parameters</span></span>
<span data-ttu-id="91b25-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91b25-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> <span data-ttu-id="91b25-121">Con los resultados de confianza, use los parámetros de consulta [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) para examinar los resultados.</span><span class="sxs-lookup"><span data-stu-id="91b25-121">For reliable results, use the [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) query parameters to page through the results.</span></span> <span data-ttu-id="91b25-122">Esto le ayudará a evitar problemas de rendimiento relacionados con grandes conjuntos de resultados.</span><span class="sxs-lookup"><span data-stu-id="91b25-122">This will help avoid performance problems related to large result sets.</span></span>

## <a name="request-headers"></a><span data-ttu-id="91b25-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="91b25-123">Request headers</span></span>
| <span data-ttu-id="91b25-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="91b25-124">Name</span></span>      |<span data-ttu-id="91b25-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="91b25-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="91b25-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="91b25-126">Authorization</span></span>  | <span data-ttu-id="91b25-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="91b25-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="91b25-129">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="91b25-129">Workbook-Session-Id</span></span>  | <span data-ttu-id="91b25-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="91b25-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="91b25-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="91b25-132">Request body</span></span>
<span data-ttu-id="91b25-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="91b25-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="91b25-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91b25-134">Response</span></span>

<span data-ttu-id="91b25-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91b25-135">If successful, this method returns a `200 OK` response code and collection of [TableRow](../resources/tablerow.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="91b25-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91b25-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="91b25-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="91b25-137">Request</span></span>
<span data-ttu-id="91b25-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="91b25-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_rows"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/rows?$top=5&$skip=5
```
##### <a name="response"></a><span data-ttu-id="91b25-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91b25-139">Response</span></span>
<span data-ttu-id="91b25-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="91b25-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableRow",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 82

{
  "value": [
    {
      "index": 99,
      "values": "values-value"
    }
  ]
}
```

> <span data-ttu-id="91b25-143">
  \*\*Nota\*\*: Use los parámetros de consulta [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) para examinar un gran número de filas.</span><span class="sxs-lookup"><span data-stu-id="91b25-143">**Note:** Use the [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) query parameters to page through large numbers of rows.</span></span>

<span data-ttu-id="91b25-144">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="91b25-144">Example:</span></span> 

`https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/rows?$top=5`
`https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/rows?$top=5&$skip=5`

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List rows",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
