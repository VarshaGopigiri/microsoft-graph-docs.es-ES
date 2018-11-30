---
title: List TableCollection
description: Recuperar una lista de objetos table.
ms.openlocfilehash: 56864105d199b461b14e66543f683e1815b28021
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029237"
---
# <a name="list-tablecollection"></a><span data-ttu-id="73d3b-103">List TableCollection</span><span class="sxs-lookup"><span data-stu-id="73d3b-103">List TableCollection</span></span>

<span data-ttu-id="73d3b-104">Recuperar una lista de objetos table.</span><span class="sxs-lookup"><span data-stu-id="73d3b-104">Retrieve a list of table objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="73d3b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="73d3b-105">Permissions</span></span>
<span data-ttu-id="73d3b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="73d3b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="73d3b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73d3b-108">Permission type</span></span>      | <span data-ttu-id="73d3b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73d3b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="73d3b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73d3b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="73d3b-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="73d3b-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="73d3b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73d3b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="73d3b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73d3b-113">Not supported.</span></span>    |
|<span data-ttu-id="73d3b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73d3b-114">Application</span></span> | <span data-ttu-id="73d3b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73d3b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="73d3b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73d3b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables
GET /workbook/worksheets/{id|name}/tables
```
## <a name="optional-query-parameters"></a><span data-ttu-id="73d3b-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="73d3b-117">Optional query parameters</span></span>
<span data-ttu-id="73d3b-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73d3b-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="73d3b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73d3b-119">Request headers</span></span>
| <span data-ttu-id="73d3b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="73d3b-120">Name</span></span>      |<span data-ttu-id="73d3b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="73d3b-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="73d3b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="73d3b-122">Authorization</span></span>  | <span data-ttu-id="73d3b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73d3b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="73d3b-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="73d3b-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="73d3b-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="73d3b-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="73d3b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73d3b-128">Request body</span></span>
<span data-ttu-id="73d3b-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="73d3b-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="73d3b-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73d3b-130">Response</span></span>

<span data-ttu-id="73d3b-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [WorkbookTable](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73d3b-131">If successful, this method returns a `200 OK` response code and collection of [WorkbookTable](../resources/table.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="73d3b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73d3b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="73d3b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73d3b-133">Request</span></span>
<span data-ttu-id="73d3b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73d3b-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tablecollection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables
```
##### <a name="response"></a><span data-ttu-id="73d3b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73d3b-135">Response</span></span>
<span data-ttu-id="73d3b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="73d3b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTable",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 158

{
  "value": [
    {
      "id": "99",
      "name": "name-value",
      "showHeaders": true,
      "showTotals": true,
      "style": "style-value"
    }
  ]
}
```
> <span data-ttu-id="73d3b-139">**Nota**: Use los parámetros de consulta [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) para examinar un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="73d3b-139">**Note:** Use the [$top](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top) query parameters to page through large numbers of tables.</span></span>

<span data-ttu-id="73d3b-140">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="73d3b-140">Example:</span></span> 

`https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables?$top=5`
`https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables?$top=5&$skip=5`

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List TableCollection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
