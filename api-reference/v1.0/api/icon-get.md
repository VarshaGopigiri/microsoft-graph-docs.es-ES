---
title: Get Icon
description: Recupera las propiedades y relaciones del objeto icon.
localization_priority: Normal
ms.openlocfilehash: 8d5f7f88892492230d2e77d587dc7f45b863f163
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869107"
---
# <a name="get-icon"></a><span data-ttu-id="ecbba-103">Get Icon</span><span class="sxs-lookup"><span data-stu-id="ecbba-103">Get Icon</span></span>

<span data-ttu-id="ecbba-104">Recupera las propiedades y relaciones del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="ecbba-104">Retrieve the properties and relationships of icon object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ecbba-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ecbba-105">Permissions</span></span>
<span data-ttu-id="ecbba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ecbba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ecbba-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ecbba-108">Permission type</span></span>      | <span data-ttu-id="ecbba-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ecbba-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="ecbba-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ecbba-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ecbba-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ecbba-111">Files.ReadWrite</span></span>    | 
|<span data-ttu-id="ecbba-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ecbba-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ecbba-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecbba-113">Not supported.</span></span>    | 
|<span data-ttu-id="ecbba-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ecbba-114">Application</span></span> | <span data-ttu-id="ecbba-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecbba-115">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ecbba-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ecbba-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/sort/fields/icon
GET /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ecbba-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ecbba-117">Optional query parameters</span></span>
<span data-ttu-id="ecbba-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecbba-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ecbba-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ecbba-119">Request headers</span></span>
| <span data-ttu-id="ecbba-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="ecbba-120">Name</span></span>      |<span data-ttu-id="ecbba-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecbba-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ecbba-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ecbba-122">Authorization</span></span>  | <span data-ttu-id="ecbba-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ecbba-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ecbba-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ecbba-125">Request body</span></span>
<span data-ttu-id="ecbba-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ecbba-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ecbba-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecbba-127">Response</span></span>

<span data-ttu-id="ecbba-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Icon](../resources/icon.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecbba-128">If successful, this method returns a `200 OK` response code and [Icon](../resources/icon.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ecbba-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ecbba-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ecbba-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ecbba-130">Request</span></span>
<span data-ttu-id="ecbba-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ecbba-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_icon"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
```
##### <a name="response"></a><span data-ttu-id="ecbba-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecbba-132">Response</span></span>
<span data-ttu-id="ecbba-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ecbba-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookIcon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get Icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
