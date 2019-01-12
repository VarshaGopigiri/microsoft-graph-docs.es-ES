---
title: Enumerar planes
description: Recuperar una lista de objetos **plannerPlan** que pertenecen a un objeto de grupo.
localization_priority: Priority
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 0212968b0882c4090044519d12157a52c85b421b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972491"
---
# <a name="list-plans"></a><span data-ttu-id="b1af2-103">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="b1af2-103">List plans</span></span>

<span data-ttu-id="b1af2-104">Recuperar una lista de objetos **plannerPlan** que pertenecen a un objeto de [grupo](../resources/group.md) .</span><span class="sxs-lookup"><span data-stu-id="b1af2-104">Retrieve a list of **plannerPlan** objects owned by a [group](../resources/group.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="b1af2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b1af2-105">Permissions</span></span>
<span data-ttu-id="b1af2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b1af2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b1af2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b1af2-108">Permission type</span></span>      | <span data-ttu-id="b1af2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b1af2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b1af2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b1af2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b1af2-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b1af2-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b1af2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b1af2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b1af2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1af2-113">Not supported.</span></span>    |
|<span data-ttu-id="b1af2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b1af2-114">Application</span></span> | <span data-ttu-id="b1af2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1af2-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b1af2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1af2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{group-id}/planner/plans
```

## <a name="request-headers"></a><span data-ttu-id="b1af2-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1af2-117">Request headers</span></span>
| <span data-ttu-id="b1af2-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1af2-118">Name</span></span>      |<span data-ttu-id="b1af2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1af2-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b1af2-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b1af2-120">Authorization</span></span>  | <span data-ttu-id="b1af2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1af2-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b1af2-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1af2-123">Request body</span></span>
<span data-ttu-id="b1af2-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b1af2-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b1af2-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1af2-125">Response</span></span>

<span data-ttu-id="b1af2-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1af2-126">If successful, this method returns a `200 OK` response code and collection of [plannerPlan](../resources/plannerplan.md) objects in the response body.</span></span>

<span data-ttu-id="b1af2-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="b1af2-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>
## <a name="example"></a><span data-ttu-id="b1af2-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1af2-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b1af2-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1af2-131">Request</span></span>
<span data-ttu-id="b1af2-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1af2-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plans"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{group-id}/planner/plans
```
##### <a name="response"></a><span data-ttu-id="b1af2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1af2-133">Response</span></span>
<span data-ttu-id="b1af2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b1af2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 421

{
  "value": [
    {
      "createdBy": {
        "application": {
          "id": "95e27074-6c4a-447a-aa24-9d718a0b86fa"
        },
        "user": {
          "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
        }
      },
      "createdDateTime": "2015-03-30T18:36:49.2407981Z",
      "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
      "title": "title-value",
      "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List plans",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
