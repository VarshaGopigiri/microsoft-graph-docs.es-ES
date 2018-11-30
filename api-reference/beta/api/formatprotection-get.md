---
title: Get FormatProtection
description: Recupera las propiedades y relaciones del objeto formatprotection.
ms.openlocfilehash: 341206df02f966d6458ed1812b33443e23e71daf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085895"
---
# <a name="get-formatprotection"></a><span data-ttu-id="125fc-103">Get FormatProtection</span><span class="sxs-lookup"><span data-stu-id="125fc-103">Get FormatProtection</span></span>

> <span data-ttu-id="125fc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="125fc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="125fc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="125fc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="125fc-106">Recupera las propiedades y relaciones del objeto formatprotection.</span><span class="sxs-lookup"><span data-stu-id="125fc-106">Retrieve the properties and relationships of formatprotection object.</span></span>
## <a name="permissions"></a><span data-ttu-id="125fc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="125fc-107">Permissions</span></span>
<span data-ttu-id="125fc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="125fc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="125fc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="125fc-110">Permission type</span></span>      | <span data-ttu-id="125fc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="125fc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="125fc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="125fc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="125fc-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="125fc-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="125fc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="125fc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="125fc-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="125fc-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="125fc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="125fc-116">Application</span></span> | <span data-ttu-id="125fc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="125fc-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="125fc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="125fc-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/format/protection
GET /workbook/worksheets/{id|name}/range(<address>)/format/protection
GET /workbook/tables/{id|name}/columns/{id|name}/range/format/protection
```
## <a name="optional-query-parameters"></a><span data-ttu-id="125fc-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="125fc-119">Optional query parameters</span></span>
<span data-ttu-id="125fc-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="125fc-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="125fc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="125fc-121">Request headers</span></span>
| <span data-ttu-id="125fc-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="125fc-122">Name</span></span>      |<span data-ttu-id="125fc-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="125fc-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="125fc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="125fc-124">Authorization</span></span>  | <span data-ttu-id="125fc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="125fc-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="125fc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="125fc-127">Request body</span></span>
<span data-ttu-id="125fc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="125fc-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="125fc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="125fc-129">Response</span></span>

<span data-ttu-id="125fc-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [FormatProtection](../resources/formatprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="125fc-130">If successful, this method returns a `200 OK` response code and [FormatProtection](../resources/formatprotection.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="125fc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="125fc-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="125fc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="125fc-132">Request</span></span>
<span data-ttu-id="125fc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="125fc-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_formatprotection"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/format/protection
```
##### <a name="response"></a><span data-ttu-id="125fc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="125fc-134">Response</span></span>
<span data-ttu-id="125fc-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="125fc-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.formatProtection"
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