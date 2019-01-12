---
title: List columns
description: Recuperar una lista de objetos tablecolumn.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 07dae774ddf8d8c006d76ec4422a932e0eb3a7e5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918297"
---
# <a name="list-columns"></a><span data-ttu-id="18513-103">List columns</span><span class="sxs-lookup"><span data-stu-id="18513-103">List columns</span></span>

> <span data-ttu-id="18513-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18513-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18513-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18513-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="18513-106">Recuperar una lista de objetos tablecolumn.</span><span class="sxs-lookup"><span data-stu-id="18513-106">Retrieve a list of tablecolumn objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="18513-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="18513-107">Permissions</span></span>
<span data-ttu-id="18513-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18513-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="18513-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18513-110">Permission type</span></span>      | <span data-ttu-id="18513-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18513-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="18513-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18513-112">Delegated (work or school account)</span></span> | <span data-ttu-id="18513-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="18513-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="18513-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18513-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="18513-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="18513-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="18513-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18513-116">Application</span></span> | <span data-ttu-id="18513-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18513-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="18513-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18513-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/columns
GET /workbook/worksheets/{id|name}/tables/{id|name}/columns
```
## <a name="optional-query-parameters"></a><span data-ttu-id="18513-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="18513-119">Optional query parameters</span></span>
<span data-ttu-id="18513-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18513-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> <span data-ttu-id="18513-121">Con los resultados de confianza, use los parámetros de consulta [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) para examinar los resultados.</span><span class="sxs-lookup"><span data-stu-id="18513-121">For reliable results, use the [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) query parameters to page through the results.</span></span> <span data-ttu-id="18513-122">Esto le ayudará a evitar problemas de rendimiento relacionados con grandes conjuntos de resultados.</span><span class="sxs-lookup"><span data-stu-id="18513-122">This will help avoid performance problems related to large result sets.</span></span>

## <a name="request-headers"></a><span data-ttu-id="18513-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18513-123">Request headers</span></span>
| <span data-ttu-id="18513-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="18513-124">Name</span></span>      |<span data-ttu-id="18513-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="18513-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="18513-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="18513-126">Authorization</span></span>  | <span data-ttu-id="18513-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18513-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="18513-129">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="18513-129">Workbook-Session-Id</span></span>  | <span data-ttu-id="18513-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="18513-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="18513-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18513-132">Request body</span></span>
<span data-ttu-id="18513-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="18513-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="18513-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18513-134">Response</span></span>

<span data-ttu-id="18513-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [TableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18513-135">If successful, this method returns a `200 OK` response code and collection of [TableColumn](../resources/tablecolumn.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="18513-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18513-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="18513-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18513-137">Request</span></span>
<span data-ttu-id="18513-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18513-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_columns"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns?$top=5&$skip=5
```
##### <a name="response"></a><span data-ttu-id="18513-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18513-139">Response</span></span>
<span data-ttu-id="18513-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18513-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn",
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

> <span data-ttu-id="18513-143">
  \*\*Nota\*\*: Use los parámetros de consulta [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) para examinar un gran número de columnas.</span><span class="sxs-lookup"><span data-stu-id="18513-143">**Note:** Use the [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skip-parameter) query parameters to page through large numbers of columns.</span></span>

<span data-ttu-id="18513-144">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="18513-144">Example:</span></span> 

`https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns?$top=5`
`https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns?$top=5&$skip=5`

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List columns",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
