---
title: Enumerar depósitos
description: Recuperar una lista de objetos **plannerbucket**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 5a5115b7afffebcf663b01c3836ba718d896098e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958225"
---
# <a name="list-buckets"></a><span data-ttu-id="fb8f8-103">Enumerar depósitos</span><span class="sxs-lookup"><span data-stu-id="fb8f8-103">List buckets</span></span>

<span data-ttu-id="fb8f8-104">Recuperar una lista de objetos **plannerbucket**.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-104">Retrieve a list of **plannerbucket** objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="fb8f8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fb8f8-105">Permissions</span></span>
<span data-ttu-id="fb8f8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb8f8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb8f8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb8f8-108">Permission type</span></span>      | <span data-ttu-id="fb8f8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb8f8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fb8f8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb8f8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fb8f8-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fb8f8-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="fb8f8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb8f8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fb8f8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-113">Not supported.</span></span>    |
|<span data-ttu-id="fb8f8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb8f8-114">Application</span></span> | <span data-ttu-id="fb8f8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fb8f8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb8f8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/buckets
```
## <a name="optional-query-parameters"></a><span data-ttu-id="fb8f8-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fb8f8-117">Optional query parameters</span></span>
<span data-ttu-id="fb8f8-118">Este método requiere que se especifique un [filter](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de planId.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-118">This method requires planId [filter](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to be specified.</span></span>

## <a name="request-headers"></a><span data-ttu-id="fb8f8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb8f8-119">Request headers</span></span>
| <span data-ttu-id="fb8f8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb8f8-120">Name</span></span>      |<span data-ttu-id="fb8f8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb8f8-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="fb8f8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="fb8f8-122">Authorization</span></span>  | <span data-ttu-id="fb8f8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fb8f8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb8f8-125">Request body</span></span>
<span data-ttu-id="fb8f8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fb8f8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb8f8-127">Response</span></span>

<span data-ttu-id="fb8f8-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerBucket](../resources/plannerbucket.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-128">If successful, this method returns a `200 OK` response code and collection of [plannerBucket](../resources/plannerbucket.md) objects in the response body.</span></span>

<span data-ttu-id="fb8f8-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="fb8f8-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>
## <a name="example"></a><span data-ttu-id="fb8f8-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb8f8-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fb8f8-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb8f8-133">Request</span></span>
<span data-ttu-id="fb8f8-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_buckets"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/buckets
```
##### <a name="response"></a><span data-ttu-id="fb8f8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb8f8-135">Response</span></span>
<span data-ttu-id="fb8f8-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb8f8-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
