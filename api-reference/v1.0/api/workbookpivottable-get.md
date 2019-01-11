---
title: Get workbookPivotTable
description: Recuperar las propiedades y relaciones del objeto workbookPivotTable.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 660300bad2128c2436d1bca0301a7707e3c1b59b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805848"
---
# <a name="get-workbookpivottable"></a><span data-ttu-id="38d2a-103">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="38d2a-103">Get workbookPivotTable</span></span>

<span data-ttu-id="38d2a-104">Recuperar las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="38d2a-104">Retrieve the properties and relationships of workbookPivotTable object.</span></span>

## <a name="permissions"></a><span data-ttu-id="38d2a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="38d2a-105">Permissions</span></span>
<span data-ttu-id="38d2a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38d2a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="38d2a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38d2a-108">Permission type</span></span>      | <span data-ttu-id="38d2a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38d2a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="38d2a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38d2a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="38d2a-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38d2a-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="38d2a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38d2a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38d2a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38d2a-113">Not supported.</span></span>    |
|<span data-ttu-id="38d2a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38d2a-114">Application</span></span> | <span data-ttu-id="38d2a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38d2a-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="38d2a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38d2a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="38d2a-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="38d2a-117">Optional query parameters</span></span>
<span data-ttu-id="38d2a-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38d2a-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="38d2a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38d2a-119">Request headers</span></span>
| <span data-ttu-id="38d2a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="38d2a-120">Name</span></span>      |<span data-ttu-id="38d2a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="38d2a-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="38d2a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="38d2a-122">Authorization</span></span>  | <span data-ttu-id="38d2a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38d2a-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="38d2a-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="38d2a-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="38d2a-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="38d2a-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="38d2a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38d2a-128">Request body</span></span>
<span data-ttu-id="38d2a-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="38d2a-129">Do not supply a request body for this method.</span></span>
### <a name="response"></a><span data-ttu-id="38d2a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38d2a-130">Response</span></span>
<span data-ttu-id="38d2a-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [workbookPivotTable](../resources/workbookpivottable.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38d2a-131">If successful, this method returns a `200 OK` response code and [workbookPivotTable](../resources/workbookpivottable.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="38d2a-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38d2a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="38d2a-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38d2a-133">Request</span></span>
<span data-ttu-id="38d2a-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38d2a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_workbookpivottable"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/pivotTables/{id}
```
##### <a name="response"></a><span data-ttu-id="38d2a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38d2a-135">Response</span></span>
<span data-ttu-id="38d2a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38d2a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookPivotTable"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 46

{
  "id": "id-value",
  "name": "name-value"
}
```
