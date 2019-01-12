---
title: Crear plannerTask
description: Use esta API para crear un objeto **plannerTask**.
localization_priority: Priority
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: f628dcf4aed87f896f9a6a97682c10ecef7fec31
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990547"
---
# <a name="create-plannertask"></a><span data-ttu-id="9b0dd-103">Crear plannerTask</span><span class="sxs-lookup"><span data-stu-id="9b0dd-103">Create plannerTask</span></span>

<span data-ttu-id="9b0dd-104">Use esta API para crear un objeto **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-104">Use this API to create a new **plannerTask**.</span></span>
## <a name="permissions"></a><span data-ttu-id="9b0dd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b0dd-105">Permissions</span></span>
<span data-ttu-id="9b0dd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b0dd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b0dd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b0dd-108">Permission type</span></span>      | <span data-ttu-id="9b0dd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b0dd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b0dd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b0dd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9b0dd-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b0dd-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="9b0dd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b0dd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b0dd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-113">Not supported.</span></span>    |
|<span data-ttu-id="9b0dd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b0dd-114">Application</span></span> | <span data-ttu-id="9b0dd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b0dd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b0dd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /planner/tasks

```
## <a name="request-headers"></a><span data-ttu-id="9b0dd-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0dd-117">Request headers</span></span>
| <span data-ttu-id="9b0dd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b0dd-118">Name</span></span>       | <span data-ttu-id="9b0dd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b0dd-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9b0dd-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b0dd-120">Authorization</span></span>  | <span data-ttu-id="9b0dd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9b0dd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0dd-123">Request body</span></span>
<span data-ttu-id="9b0dd-p103">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerTask](../resources/plannertask.md). La propiedad planId de **plannerTask** se debe establecer en el id. de un objeto [plannerPlan](../resources/plannerplan.md) existente.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-p103">In the request body, supply a JSON representation of [plannerTask](../resources/plannertask.md) object. The **plannerTask** planId property must be set to an existing [plannerPlan](../resources/plannerplan.md) object's id.</span></span>

## <a name="response"></a><span data-ttu-id="9b0dd-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b0dd-126">Response</span></span>

<span data-ttu-id="9b0dd-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [plannerTask](../resources/plannertask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-127">If successful, this method returns `201 Created` response code and [plannerTask](../resources/plannertask.md) object in the response body.</span></span>

<span data-ttu-id="9b0dd-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="9b0dd-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="9b0dd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b0dd-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9b0dd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0dd-132">Request</span></span>
<span data-ttu-id="9b0dd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_plannertask_from_planner"
}-->
```http
POST https://graph.microsoft.com/v1.0/planner/tasks
Content-type: application/json
Content-length: 285

{
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "bucketId": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
  "title": "Update client list",
  "assignments": {
    "fbab97d0-4932-4511-b675-204639209557": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "orderHint": " !"
    }
  },
}
```
<span data-ttu-id="9b0dd-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerTask](../resources/plannertask.md).</span><span class="sxs-lookup"><span data-stu-id="9b0dd-134">In the request body, supply a JSON representation of [plannerTask](../resources/plannertask.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9b0dd-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b0dd-135">Response</span></span>
<span data-ttu-id="9b0dd-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b0dd-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 677

{
  "createdBy": {
    "user": {
      "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
    }
  },
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "bucketId": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
  "title": "Update client list",
  "orderHint": "85752723360752+",
  "createdDateTime": "2015-03-25T18:36:49.2407981Z",
  "assignments": {
    "fbab97d0-4932-4511-b675-204639209557": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "assignedBy": {
        "user": {
          "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
        }
      },
      "assignedDateTime": "2015-03-25T18:36:49.2407981Z",
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
  "description": "Create plannerTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
