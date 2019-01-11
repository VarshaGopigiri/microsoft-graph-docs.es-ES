---
title: Get Icon
description: Recupera las propiedades y relaciones del objeto icon.
localization_priority: Normal
ms.openlocfilehash: b018a9b422cf3f4ae3e83902db1246d737fe608e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829312"
---
# <a name="get-icon"></a><span data-ttu-id="234e0-103">Get Icon</span><span class="sxs-lookup"><span data-stu-id="234e0-103">Get Icon</span></span>

> <span data-ttu-id="234e0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="234e0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="234e0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="234e0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="234e0-106">Recupera las propiedades y relaciones del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="234e0-106">Retrieve the properties and relationships of icon object.</span></span>
## <a name="permissions"></a><span data-ttu-id="234e0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="234e0-107">Permissions</span></span>
<span data-ttu-id="234e0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="234e0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="234e0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="234e0-110">Permission type</span></span>      | <span data-ttu-id="234e0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="234e0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="234e0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="234e0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="234e0-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="234e0-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="234e0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="234e0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="234e0-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="234e0-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="234e0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="234e0-116">Application</span></span> | <span data-ttu-id="234e0-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="234e0-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="234e0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="234e0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/sort/fields/icon
GET /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-query-parameters"></a><span data-ttu-id="234e0-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="234e0-119">Optional query parameters</span></span>
<span data-ttu-id="234e0-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="234e0-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="234e0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="234e0-121">Request headers</span></span>
| <span data-ttu-id="234e0-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="234e0-122">Name</span></span>      |<span data-ttu-id="234e0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="234e0-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="234e0-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="234e0-124">Authorization</span></span>  | <span data-ttu-id="234e0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="234e0-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="234e0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="234e0-127">Request body</span></span>
<span data-ttu-id="234e0-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="234e0-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="234e0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="234e0-129">Response</span></span>

<span data-ttu-id="234e0-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Icon](../resources/icon.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="234e0-130">If successful, this method returns a `200 OK` response code and [Icon](../resources/icon.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="234e0-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="234e0-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="234e0-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="234e0-132">Request</span></span>
<span data-ttu-id="234e0-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="234e0-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_icon"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
```
##### <a name="response"></a><span data-ttu-id="234e0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="234e0-134">Response</span></span>
<span data-ttu-id="234e0-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="234e0-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.icon"
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
