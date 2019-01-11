---
title: Obtener plannerBucketTaskBoardTaskFormat
description: Recuperar las propiedades y las relaciones del objeto **plannerBucketTaskBoardTaskFormat**.
localization_priority: Normal
ms.openlocfilehash: cf9ce0f3016c941bbe02409ba218b00a8d0712c4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848142"
---
# <a name="get-plannerbuckettaskboardtaskformat"></a><span data-ttu-id="56e80-103">Obtener plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="56e80-103">Get plannerBucketTaskBoardTaskFormat</span></span>

<span data-ttu-id="56e80-104">Recuperar las propiedades y las relaciones del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="56e80-104">Retrieve the properties and relationships of **plannerBucketTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="56e80-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="56e80-105">Permissions</span></span>
<span data-ttu-id="56e80-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="56e80-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="56e80-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56e80-108">Permission type</span></span>      | <span data-ttu-id="56e80-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56e80-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="56e80-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56e80-110">Delegated (work or school account)</span></span> | <span data-ttu-id="56e80-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56e80-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="56e80-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56e80-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="56e80-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56e80-113">Not supported.</span></span>    |
|<span data-ttu-id="56e80-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56e80-114">Application</span></span> | <span data-ttu-id="56e80-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56e80-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="56e80-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56e80-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/tasks/{id}/bucketTaskBoardFormat
```

## <a name="request-headers"></a><span data-ttu-id="56e80-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56e80-117">Request headers</span></span>
| <span data-ttu-id="56e80-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="56e80-118">Name</span></span>      |<span data-ttu-id="56e80-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="56e80-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="56e80-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="56e80-120">Authorization</span></span>  | <span data-ttu-id="56e80-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="56e80-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="56e80-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56e80-123">Request body</span></span>
<span data-ttu-id="56e80-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="56e80-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="56e80-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56e80-125">Response</span></span>

<span data-ttu-id="56e80-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56e80-126">If successful, this method returns a `200 OK` response code and [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="56e80-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="56e80-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="56e80-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56e80-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="56e80-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56e80-131">Request</span></span>
<span data-ttu-id="56e80-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56e80-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannerbuckettaskboardtaskformat"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/bucketTaskBoardFormat
```
##### <a name="response"></a><span data-ttu-id="56e80-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56e80-133">Response</span></span>
<span data-ttu-id="56e80-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56e80-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 76

{
  "id": "01gzSlKkIUSUl6DF_EilrmQAKDhh",
  "orderHint": "85752723360752+"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerBucketTaskBoardTaskFormat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
