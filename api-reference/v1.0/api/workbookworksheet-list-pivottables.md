---
title: List pivotTables
description: Recuperar una lista de objetos workbookpivottable.
ms.openlocfilehash: 1390c25a324db523cec4d44d6ca77ac40a57cdfa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029429"
---
# <a name="list-pivottables"></a><span data-ttu-id="1302d-103">List pivotTables</span><span class="sxs-lookup"><span data-stu-id="1302d-103">List pivotTables</span></span>

<span data-ttu-id="1302d-104">Recuperar una lista de objetos workbookpivottable.</span><span class="sxs-lookup"><span data-stu-id="1302d-104">Retrieve a list of workbookpivottable objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="1302d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1302d-105">Permissions</span></span>
<span data-ttu-id="1302d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1302d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="1302d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1302d-108">Permission type</span></span>      | <span data-ttu-id="1302d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1302d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1302d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1302d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1302d-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1302d-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1302d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1302d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1302d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1302d-113">Not supported.</span></span>    |
|<span data-ttu-id="1302d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1302d-114">Application</span></span> | <span data-ttu-id="1302d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1302d-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1302d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1302d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/pivotTables
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1302d-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1302d-117">Optional query parameters</span></span>
<span data-ttu-id="1302d-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1302d-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1302d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1302d-119">Request headers</span></span>
| <span data-ttu-id="1302d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1302d-120">Name</span></span>      |<span data-ttu-id="1302d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1302d-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1302d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1302d-122">Authorization</span></span>  | <span data-ttu-id="1302d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1302d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1302d-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1302d-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="1302d-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1302d-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1302d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1302d-128">Request body</span></span>
<span data-ttu-id="1302d-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1302d-129">Do not supply a request body for this method.</span></span>
### <a name="response"></a><span data-ttu-id="1302d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1302d-130">Response</span></span>
<span data-ttu-id="1302d-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [workbookPivotTable](../resources/workbookpivottable.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1302d-131">If successful, this method returns a `200 OK` response code and collection of [workbookPivotTable](../resources/workbookpivottable.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1302d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1302d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1302d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1302d-133">Request</span></span>
<span data-ttu-id="1302d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1302d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_pivottables"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/pivotTables
```
##### <a name="response"></a><span data-ttu-id="1302d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1302d-135">Response</span></span>
<span data-ttu-id="1302d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1302d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookPivotTable",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 83

{
  "value": [
    {
      "id": "id-value",
      "name": "name-value"
    }
  ]
}
```
