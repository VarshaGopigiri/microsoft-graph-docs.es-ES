---
title: Obtener plannerTask
description: Recuperar las propiedades y las relaciones del objeto **plannertask**.
ms.openlocfilehash: 9ffd959572134f3db0f011a33694cb32eae33f16
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031116"
---
# <a name="get-plannertask"></a><span data-ttu-id="42cd1-103">Obtener plannerTask</span><span class="sxs-lookup"><span data-stu-id="42cd1-103">Get plannerTask</span></span>

<span data-ttu-id="42cd1-104">Recuperar las propiedades y las relaciones del objeto **plannertask**.</span><span class="sxs-lookup"><span data-stu-id="42cd1-104">Retrieve the properties and relationships of **plannertask** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="42cd1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="42cd1-105">Permissions</span></span>
<span data-ttu-id="42cd1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="42cd1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="42cd1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="42cd1-108">Permission type</span></span>      | <span data-ttu-id="42cd1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="42cd1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="42cd1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="42cd1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="42cd1-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="42cd1-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="42cd1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="42cd1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="42cd1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42cd1-113">Not supported.</span></span>    |
|<span data-ttu-id="42cd1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42cd1-114">Application</span></span> | <span data-ttu-id="42cd1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42cd1-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="42cd1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="42cd1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/tasks/{id}
```

## <a name="request-headers"></a><span data-ttu-id="42cd1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="42cd1-117">Request headers</span></span>
| <span data-ttu-id="42cd1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="42cd1-118">Name</span></span>      |<span data-ttu-id="42cd1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="42cd1-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="42cd1-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="42cd1-120">Authorization</span></span>  | <span data-ttu-id="42cd1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="42cd1-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="42cd1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="42cd1-123">Request body</span></span>
<span data-ttu-id="42cd1-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="42cd1-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="42cd1-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42cd1-125">Response</span></span>

<span data-ttu-id="42cd1-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTask](../resources/plannertask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="42cd1-126">If successful, this method returns a `200 OK` response code and [plannerTask](../resources/plannertask.md) object in the response body.</span></span>

<span data-ttu-id="42cd1-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="42cd1-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="42cd1-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42cd1-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="42cd1-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="42cd1-131">Request</span></span>
<span data-ttu-id="42cd1-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42cd1-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannertask"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/tasks/{task-id}
```
##### <a name="response"></a><span data-ttu-id="42cd1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42cd1-133">Response</span></span>
<span data-ttu-id="42cd1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="42cd1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 707

{
  "createdBy": {
    "user": {
      "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
    }
  },
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "bucketId": "gcrYAaAkgU2EQUvpkNNXLGQAGTtu",
  "title": "title-value",
  "orderHint": "9223370609546166567W",
  "assigneePriority": "90057581\"",
  "createdDateTime": "2015-03-25T18:36:49.2407981Z",
  "assignments": {
    "fbab97d0-4932-4511-b675-204639209557": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "assignedBy": {
        "user": {
          "id": "1e9955d2-6acd-45bf-86d3-b546fdc795eb"
        }
      },
      "assignedDateTime": "2015-03-25T18:38:21.956Z",
      "orderHint": "RWk1"
    }
  },
  "id":"01gzSlKkIUSUl6DF_EilrmQAKDhh"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->