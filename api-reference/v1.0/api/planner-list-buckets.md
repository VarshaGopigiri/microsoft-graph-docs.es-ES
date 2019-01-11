---
title: Enumerar depósitos
description: Recuperar una lista de objetos **plannerbucket**.
localization_priority: Normal
ms.openlocfilehash: ea467d4a8aaa70eb298156c786c935608e21b440
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826204"
---
# <a name="list-buckets"></a><span data-ttu-id="65596-103">Enumerar depósitos</span><span class="sxs-lookup"><span data-stu-id="65596-103">List buckets</span></span>

<span data-ttu-id="65596-104">Recuperar una lista de objetos **plannerbucket**.</span><span class="sxs-lookup"><span data-stu-id="65596-104">Retrieve a list of **plannerbucket** objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="65596-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="65596-105">Permissions</span></span>
<span data-ttu-id="65596-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65596-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="65596-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65596-108">Permission type</span></span>      | <span data-ttu-id="65596-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65596-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="65596-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65596-110">Delegated (work or school account)</span></span> | <span data-ttu-id="65596-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="65596-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="65596-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65596-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="65596-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65596-113">Not supported.</span></span>    |
|<span data-ttu-id="65596-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65596-114">Application</span></span> | <span data-ttu-id="65596-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65596-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="65596-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65596-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/buckets
```
## <a name="optional-query-parameters"></a><span data-ttu-id="65596-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="65596-117">Optional query parameters</span></span>
<span data-ttu-id="65596-118">Este método requiere que se especifique un [filter](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de planId.</span><span class="sxs-lookup"><span data-stu-id="65596-118">This method requires planId [filter](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to be specified.</span></span>

## <a name="request-headers"></a><span data-ttu-id="65596-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65596-119">Request headers</span></span>
| <span data-ttu-id="65596-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="65596-120">Name</span></span>      |<span data-ttu-id="65596-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="65596-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="65596-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="65596-122">Authorization</span></span>  | <span data-ttu-id="65596-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="65596-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="65596-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65596-125">Request body</span></span>
<span data-ttu-id="65596-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="65596-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="65596-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65596-127">Response</span></span>

<span data-ttu-id="65596-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerBucket](../resources/plannerbucket.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65596-128">If successful, this method returns a `200 OK` response code and collection of [plannerBucket](../resources/plannerbucket.md) objects in the response body.</span></span>

<span data-ttu-id="65596-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="65596-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>
## <a name="example"></a><span data-ttu-id="65596-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65596-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="65596-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65596-133">Request</span></span>
<span data-ttu-id="65596-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65596-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_buckets"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/buckets
```
##### <a name="response"></a><span data-ttu-id="65596-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65596-135">Response</span></span>
<span data-ttu-id="65596-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65596-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucket",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 251

{
  "value": [
    {
      "@odata.etag": "W/\"JzEtQnVja2V0QEBAQEBAQEBAQEBAQEBARCc=\"",
      "name": "To do",
      "planId": "2txjA-BMZEq-bKi6Wfj5aGQAB1OJ",
      "orderHint": "85752723360752+",
      "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List buckets",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
