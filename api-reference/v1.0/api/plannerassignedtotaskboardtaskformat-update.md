---
title: Actualizar plannerAssignedToTaskBoardTaskFormat
description: Actualizar las propiedades del objeto **plannerAssignedToTaskBoardTaskFormat**.
localization_priority: Normal
ms.openlocfilehash: 9efb07bd8bda108497f77d4f982b42eb3c8e53b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855639"
---
# <a name="update-plannerassignedtotaskboardtaskformat"></a><span data-ttu-id="01752-103">Actualizar plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="01752-103">Update plannerAssignedToTaskBoardTaskFormat</span></span>

<span data-ttu-id="01752-104">Actualizar las propiedades del objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="01752-104">Update the properties of **plannerAssignedToTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="01752-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="01752-105">Permissions</span></span>
<span data-ttu-id="01752-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01752-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01752-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01752-108">Permission type</span></span>      | <span data-ttu-id="01752-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01752-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01752-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01752-110">Delegated (work or school account)</span></span> | <span data-ttu-id="01752-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01752-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="01752-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01752-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01752-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01752-113">Not supported.</span></span>    |
|<span data-ttu-id="01752-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01752-114">Application</span></span> | <span data-ttu-id="01752-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01752-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="01752-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01752-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/{id}/assignedToTaskBoardFormat
```
## <a name="optional-request-headers"></a><span data-ttu-id="01752-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="01752-117">Optional request headers</span></span>
| <span data-ttu-id="01752-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="01752-118">Name</span></span>       | <span data-ttu-id="01752-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="01752-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="01752-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="01752-120">Authorization</span></span>  | <span data-ttu-id="01752-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01752-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="01752-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="01752-123">If-Match</span></span>  | <span data-ttu-id="01752-p103">Último valor ETag conocido para que se actualice **plannerAssignedToTaskBoardTaskFormat**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01752-p103">Last known ETag value for **plannerAssignedToTaskBoardTaskFormat** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="01752-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01752-126">Request body</span></span>
<span data-ttu-id="01752-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="01752-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="01752-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01752-130">Property</span></span>     | <span data-ttu-id="01752-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="01752-131">Type</span></span>   |<span data-ttu-id="01752-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="01752-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01752-133">orderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="01752-133">orderHintsByAssignee</span></span>|[<span data-ttu-id="01752-134">plannerOrderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="01752-134">plannerOrderHintsByAssignee</span></span>](../resources/plannerorderhintsbyassignee.md)|<span data-ttu-id="01752-p105">Diccionario de sugerencias usadas para ordenar las tareas en la vista AsignadoA del panel de tareas. La clave de cada entrada es uno de los usuarios a los que se ha asignado la tarea, mientras que el valor es la sugerencia de orden. El formato de cada valor se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="01752-p105">Dictionary of hints used to order tasks on the AssignedTo view of the Task Board. The key of each entry is one of the users the task is assigned to and the value is the order hint. The format of each value is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="01752-138">unassignedOrderHint</span><span class="sxs-lookup"><span data-stu-id="01752-138">unassignedOrderHint</span></span>|<span data-ttu-id="01752-139">String</span><span class="sxs-lookup"><span data-stu-id="01752-139">String</span></span>|<span data-ttu-id="01752-p106">Valor de sugerencia usado para ordenar la tarea en la vista AsignadoA del panel de tareas si la tarea no está asignada a nadie, o si el diccionario orderHintsByAssignee no proporciona ninguna sugerencia de orden para el usuario al que se ha asignado la tarea. El formato se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="01752-p106">Hint value used to order the task on the AssignedTo view of the Task Board when the task is not assigned to anyone, or if the orderHintsByAssignee dictionary does not provide an order hint for the user the task is assigned to. The format is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|

## <a name="response"></a><span data-ttu-id="01752-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01752-142">Response</span></span>

<span data-ttu-id="01752-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01752-143">If successful, this method returns a `200 OK` response code and updated [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="01752-p107">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="01752-p107">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="01752-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01752-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="01752-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01752-148">Request</span></span>
<span data-ttu-id="01752-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01752-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerassignedtotaskboardtaskformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/assignedToTaskBoardFormat
Content-type: application/json
Content-length: 96
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "orderHintsByAssignee": {
    "aaa27244-1db4-476a-a5cb-004607466324": "8566473P 957764Jk!"
  }
}
```
##### <a name="response"></a><span data-ttu-id="01752-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01752-150">Response</span></span>
<span data-ttu-id="01752-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01752-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Update plannerassignedtotaskboardtaskformat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
