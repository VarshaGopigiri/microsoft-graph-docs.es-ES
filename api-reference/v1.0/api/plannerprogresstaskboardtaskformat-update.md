---
title: Actualizar plannerProgressTaskBoardTaskFormat
description: Actualizar las propiedades del objeto **plannerProgressTaskBoardTaskFormat**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 2c21e364d292dfa446b4b5441ad9d1f8d3020a64
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987233"
---
# <a name="update-plannerprogresstaskboardtaskformat"></a><span data-ttu-id="ae166-103">Actualizar plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="ae166-103">Update plannerProgressTaskBoardTaskFormat</span></span>

<span data-ttu-id="ae166-104">Actualizar las propiedades del objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="ae166-104">Update the properties of **plannerProgressTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ae166-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ae166-105">Permissions</span></span>
<span data-ttu-id="ae166-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ae166-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ae166-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ae166-108">Permission type</span></span>      | <span data-ttu-id="ae166-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ae166-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ae166-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ae166-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ae166-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ae166-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ae166-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ae166-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ae166-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae166-113">Not supported.</span></span>    |
|<span data-ttu-id="ae166-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ae166-114">Application</span></span> | <span data-ttu-id="ae166-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae166-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ae166-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae166-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/{id}/progressTaskBoardFormat
```
## <a name="optional-request-headers"></a><span data-ttu-id="ae166-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ae166-117">Optional request headers</span></span>
| <span data-ttu-id="ae166-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae166-118">Name</span></span>       | <span data-ttu-id="ae166-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae166-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ae166-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae166-120">Authorization</span></span>  | <span data-ttu-id="ae166-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae166-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ae166-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="ae166-123">If-Match</span></span>  | <span data-ttu-id="ae166-p103">Último valor ETag conocido para que se actualice **plannerProgressTaskBoardTaskFormat**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae166-p103">Last known ETag value for the **plannerProgressTaskBoardTaskFormat** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ae166-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae166-126">Request body</span></span>
<span data-ttu-id="ae166-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ae166-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ae166-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae166-130">Property</span></span>     | <span data-ttu-id="ae166-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae166-131">Type</span></span>   |<span data-ttu-id="ae166-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae166-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ae166-133">orderHint</span><span class="sxs-lookup"><span data-stu-id="ae166-133">orderHint</span></span>|<span data-ttu-id="ae166-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ae166-134">String</span></span>|<span data-ttu-id="ae166-p105">Valor de sugerencia usado para ordenar la tarea en la vista Progreso del panel de tareas. El formato se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="ae166-p105">Hint value used to order the task on the Progress view of the Task Board. The format is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|

## <a name="response"></a><span data-ttu-id="ae166-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae166-137">Response</span></span>

<span data-ttu-id="ae166-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerProgressTaskBoardTaskFormat](../resources/plannerprogresstaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae166-138">If successful, this method returns a `200 OK` response code and updated [plannerProgressTaskBoardTaskFormat](../resources/plannerprogresstaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="ae166-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="ae166-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="ae166-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae166-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ae166-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae166-143">Request</span></span>
<span data-ttu-id="ae166-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae166-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerprogresstaskboardtaskformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/progressTaskBoardFormat
Content-type: application/json
Content-length: 34
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "orderHint": "A6673H Ejkl!"
}
```
##### <a name="response"></a><span data-ttu-id="ae166-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae166-145">Response</span></span>
<span data-ttu-id="ae166-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ae166-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerProgressTaskBoardTaskFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 68

{
  "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
  "orderHint": "C3665D"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerprogresstaskboardtaskformat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
