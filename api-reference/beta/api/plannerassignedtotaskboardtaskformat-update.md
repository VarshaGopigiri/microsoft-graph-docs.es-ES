---
title: Actualizar plannerAssignedToTaskBoardTaskFormat
description: Actualizar las propiedades del objeto **plannerAssignedToTaskBoardTaskFormat**.
ms.openlocfilehash: 7bf559b5962c895c1ce7b5d3192ab743bca3acb2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085672"
---
# <a name="update-plannerassignedtotaskboardtaskformat"></a><span data-ttu-id="3f053-103">Actualizar plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="3f053-103">Update plannerAssignedToTaskBoardTaskFormat</span></span>

> <span data-ttu-id="3f053-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f053-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f053-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f053-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3f053-106">Actualizar las propiedades del objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="3f053-106">Update the properties of **plannerAssignedToTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="3f053-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3f053-107">Permissions</span></span>
<span data-ttu-id="3f053-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f053-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f053-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f053-110">Permission type</span></span>      | <span data-ttu-id="3f053-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f053-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3f053-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f053-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3f053-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f053-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="3f053-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f053-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3f053-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f053-115">Not supported.</span></span>    |
|<span data-ttu-id="3f053-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f053-116">Application</span></span> | <span data-ttu-id="3f053-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f053-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3f053-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f053-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>/assignedToTaskBoardFormat
```
## <a name="optional-request-headers"></a><span data-ttu-id="3f053-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="3f053-119">Optional request headers</span></span>
| <span data-ttu-id="3f053-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f053-120">Name</span></span>       | <span data-ttu-id="3f053-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f053-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="3f053-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3f053-122">Authorization</span></span>  | <span data-ttu-id="3f053-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f053-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3f053-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="3f053-125">If-Match</span></span>  | <span data-ttu-id="3f053-p104">Último valor ETag conocido para que se actualice **plannerAssignedToTaskBoardTaskFormat**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f053-p104">Last known ETag value for **plannerAssignedToTaskBoardTaskFormat** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f053-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f053-128">Request body</span></span>
<span data-ttu-id="3f053-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="3f053-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="3f053-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f053-132">Property</span></span>     | <span data-ttu-id="3f053-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f053-133">Type</span></span>   |<span data-ttu-id="3f053-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f053-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f053-135">orderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="3f053-135">orderHintsByAssignee</span></span>|[<span data-ttu-id="3f053-136">plannerOrderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="3f053-136">plannerOrderHintsByAssignee</span></span>](../resources/plannerorderhintsbyassignee.md)|<span data-ttu-id="3f053-137">Diccionario de sugerencias de utilizadas en las tareas de orden en la vista AssignedTo del panel de tareas de.</span><span class="sxs-lookup"><span data-stu-id="3f053-137">Dictionary of hints used to order tasks on the AssignedTo view of the Task Board.</span></span> <span data-ttu-id="3f053-138">La clave de cada entrada es uno de los usuarios a que se asigna la tarea y el valor es la sugerencia de orden.</span><span class="sxs-lookup"><span data-stu-id="3f053-138">The key of each entry is one of the users the task is assigned to and the value is the order hint.</span></span> <span data-ttu-id="3f053-139">El formato de cada valor se define en [con sugerencias de orden en Organizador (.. / resources/planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="3f053-139">The format of each value is defined in [Using order hints in Planner(../resources/planner_order_hint_format.md).</span></span>|
|<span data-ttu-id="3f053-140">unassignedOrderHint</span><span class="sxs-lookup"><span data-stu-id="3f053-140">unassignedOrderHint</span></span>|<span data-ttu-id="3f053-141">String</span><span class="sxs-lookup"><span data-stu-id="3f053-141">String</span></span>|<span data-ttu-id="3f053-142">Valor de sugerencia que se utiliza para pedir la tarea en la vista AssignedTo del panel de tareas cuando la tarea no se asigna a cualquier persona, o si el diccionario orderHintsByAssignee no proporciona una sugerencia de orden para el usuario de la tarea se asigna a.</span><span class="sxs-lookup"><span data-stu-id="3f053-142">Hint value used to order the task on the AssignedTo view of the Task Board when the task is not assigned to anyone, or if the orderHintsByAssignee dictionary does not provide an order hint for the user the task is assigned to.</span></span> <span data-ttu-id="3f053-143">El formato se define en las [sugerencias de orden de uso en el organizador](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="3f053-143">The format is defined in [Using order hints in Planner](../resources/planner-order-hint-format.md).</span></span>|

## <a name="response"></a><span data-ttu-id="3f053-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f053-144">Response</span></span>

<span data-ttu-id="3f053-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f053-145">If successful, this method returns a `200 OK` response code and updated [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="3f053-p108">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="3f053-p108">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="3f053-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f053-149">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3f053-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f053-150">Request</span></span>
<span data-ttu-id="3f053-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f053-151">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerassignedtotaskboardtaskformat"
}-->
```http
PATCH https://graph.microsoft.com/beta/planner/tasks/01gzSlKkIUSUl6DF_EilrmQAKDhh/assignedToTaskBoardFormat
Content-type: application/json
Content-length: 96
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "orderHintsByAssignee": {
    "aaa27244-1db4-476a-a5cb-004607466324": "8566473P 957764Jk!"
  }
}
```
##### <a name="response"></a><span data-ttu-id="3f053-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f053-152">Response</span></span>
<span data-ttu-id="3f053-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f053-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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