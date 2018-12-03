---
title: Get FormatProtection
description: Recupera las propiedades y relaciones del objeto formatprotection.
ms.openlocfilehash: 4c586d070b506dd0ab10db8291863e051137f840
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030538"
---
# <a name="get-formatprotection"></a><span data-ttu-id="35dc8-103">Get FormatProtection</span><span class="sxs-lookup"><span data-stu-id="35dc8-103">Get FormatProtection</span></span>

<span data-ttu-id="35dc8-104">Recupera las propiedades y relaciones del objeto formatprotection.</span><span class="sxs-lookup"><span data-stu-id="35dc8-104">Retrieve the properties and relationships of formatprotection object.</span></span>
## <a name="permissions"></a><span data-ttu-id="35dc8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="35dc8-105">Permissions</span></span>
<span data-ttu-id="35dc8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35dc8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="35dc8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35dc8-108">Permission type</span></span>      | <span data-ttu-id="35dc8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35dc8-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="35dc8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35dc8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="35dc8-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="35dc8-111">Files.ReadWrite</span></span>    | 
|<span data-ttu-id="35dc8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35dc8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="35dc8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35dc8-113">Not supported.</span></span>    | 
|<span data-ttu-id="35dc8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35dc8-114">Application</span></span> | <span data-ttu-id="35dc8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35dc8-115">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="35dc8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35dc8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/format/protection
GET /workbook/worksheets/{id|name}/range(<address>)/format/protection
GET /workbook/tables/{id|name}/columns/{id|name}/range/format/protection
```
## <a name="optional-query-parameters"></a><span data-ttu-id="35dc8-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="35dc8-117">Optional query parameters</span></span>
<span data-ttu-id="35dc8-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35dc8-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="35dc8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35dc8-119">Request headers</span></span>
| <span data-ttu-id="35dc8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="35dc8-120">Name</span></span>      |<span data-ttu-id="35dc8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="35dc8-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="35dc8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="35dc8-122">Authorization</span></span>  | <span data-ttu-id="35dc8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35dc8-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="35dc8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35dc8-125">Request body</span></span>
<span data-ttu-id="35dc8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35dc8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35dc8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35dc8-127">Response</span></span>

<span data-ttu-id="35dc8-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [FormatProtection](../resources/formatprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35dc8-128">If successful, this method returns a `200 OK` response code and [FormatProtection](../resources/formatprotection.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="35dc8-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35dc8-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="35dc8-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35dc8-130">Request</span></span>
<span data-ttu-id="35dc8-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35dc8-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_formatprotection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/protection
```
##### <a name="response"></a><span data-ttu-id="35dc8-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35dc8-132">Response</span></span>
<span data-ttu-id="35dc8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35dc8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookFormatProtection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "locked": true,
  "formulaHidden": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get FormatProtection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->