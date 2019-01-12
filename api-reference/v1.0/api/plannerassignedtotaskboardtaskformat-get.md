---
title: Obtener plannerAssignedToTaskBoardTaskFormat
description: Recuperar las propiedades y las relaciones del objeto **plannerAssignedToTaskBoardTaskFormat**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: eed81ce74d7e90ba19e90d9d4280686f5716c73e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963461"
---
# <a name="get-plannerassignedtotaskboardtaskformat"></a><span data-ttu-id="c828b-103">Obtener plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="c828b-103">Get plannerAssignedToTaskBoardTaskFormat</span></span>

<span data-ttu-id="c828b-104">Recuperar las propiedades y las relaciones del objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="c828b-104">Retrieve the properties and relationships of **plannerAssignedToTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c828b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c828b-105">Permissions</span></span>
<span data-ttu-id="c828b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c828b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c828b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c828b-108">Permission type</span></span>      | <span data-ttu-id="c828b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c828b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c828b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c828b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c828b-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c828b-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c828b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c828b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c828b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c828b-113">Not supported.</span></span>    |
|<span data-ttu-id="c828b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c828b-114">Application</span></span> | <span data-ttu-id="c828b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c828b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c828b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c828b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/tasks/{id}/assignedToTaskBoardFormat
```
## <a name="request-headers"></a><span data-ttu-id="c828b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c828b-117">Request headers</span></span>
| <span data-ttu-id="c828b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c828b-118">Name</span></span>      |<span data-ttu-id="c828b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c828b-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c828b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c828b-120">Authorization</span></span>  | <span data-ttu-id="c828b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c828b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c828b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c828b-123">Request body</span></span>
<span data-ttu-id="c828b-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c828b-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c828b-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c828b-125">Response</span></span>

<span data-ttu-id="c828b-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c828b-126">If successful, this method returns a `200 OK` response code and [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="c828b-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="c828b-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="c828b-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c828b-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c828b-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c828b-131">Request</span></span>
<span data-ttu-id="c828b-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c828b-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannerassignedtotaskboardtaskformat"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/assignedToTaskBoardFormat
```
##### <a name="response"></a><span data-ttu-id="c828b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c828b-133">Response</span></span>
<span data-ttu-id="c828b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c828b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerAssignedToTaskBoardTaskFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 225

{
  "unassignedOrderHint": "RWk1",
  "orderHintsByAssignee": {
    "6463a5ce-2119-4198-9f2a-628761df4a62":"85752723360752+",
    "aaa27244-1db4-476a-a5cb-004607466324":"90057581;"
  },
  "id": "01gzSlKkIUSUl6DF_EilrmQAKDhh"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerAssignedToTaskBoardTaskFormat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
