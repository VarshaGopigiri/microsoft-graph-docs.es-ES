---
title: List worksheets
description: Recuperar una lista de objetos worksheet.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 8d337eac1ccc1d5543bcca605a30d57867fda63e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878844"
---
# <a name="list-worksheets"></a><span data-ttu-id="9bb47-103">List worksheets</span><span class="sxs-lookup"><span data-stu-id="9bb47-103">List worksheets</span></span>

> <span data-ttu-id="9bb47-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9bb47-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9bb47-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9bb47-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9bb47-106">Recuperar una lista de objetos worksheet.</span><span class="sxs-lookup"><span data-stu-id="9bb47-106">Retrieve a list of worksheet objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="9bb47-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9bb47-107">Permissions</span></span>
<span data-ttu-id="9bb47-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9bb47-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9bb47-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9bb47-110">Permission type</span></span>      | <span data-ttu-id="9bb47-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9bb47-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9bb47-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9bb47-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9bb47-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9bb47-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9bb47-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9bb47-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9bb47-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9bb47-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9bb47-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9bb47-116">Application</span></span> | <span data-ttu-id="9bb47-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9bb47-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9bb47-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9bb47-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9bb47-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9bb47-119">Optional query parameters</span></span>
<span data-ttu-id="9bb47-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9bb47-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9bb47-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9bb47-121">Request headers</span></span>
| <span data-ttu-id="9bb47-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bb47-122">Name</span></span>      |<span data-ttu-id="9bb47-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bb47-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9bb47-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="9bb47-124">Authorization</span></span>  | <span data-ttu-id="9bb47-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9bb47-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9bb47-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9bb47-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="9bb47-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="9bb47-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9bb47-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9bb47-130">Request body</span></span>
<span data-ttu-id="9bb47-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9bb47-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9bb47-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9bb47-132">Response</span></span>

<span data-ttu-id="9bb47-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Worksheet](../resources/worksheet.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9bb47-133">If successful, this method returns a `200 OK` response code and collection of [Worksheet](../resources/worksheet.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9bb47-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9bb47-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9bb47-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9bb47-135">Request</span></span>
<span data-ttu-id="9bb47-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9bb47-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_worksheets"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets
```
##### <a name="response"></a><span data-ttu-id="9bb47-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9bb47-137">Response</span></span>
<span data-ttu-id="9bb47-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9bb47-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.worksheet",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 145

{
  "value": [
    {
      "id": "id-value",
      "position": 99,
      "name": "name-value",
      "visibility": "visibility-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List worksheets",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
