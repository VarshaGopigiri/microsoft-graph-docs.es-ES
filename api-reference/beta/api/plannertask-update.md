---
title: Actualizar plannertask
description: Actualizar las propiedades del objeto **plannertask**.
ms.openlocfilehash: aea85ef7a5e463153c84149c815f8e6dbd74075f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083700"
---
# <a name="update-plannertask"></a><span data-ttu-id="01b00-103">Actualizar plannertask</span><span class="sxs-lookup"><span data-stu-id="01b00-103">Update plannertask</span></span>

> <span data-ttu-id="01b00-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01b00-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01b00-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01b00-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="01b00-106">Actualizar las propiedades del objeto **plannertask**.</span><span class="sxs-lookup"><span data-stu-id="01b00-106">Update the properties of **plannertask** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="01b00-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="01b00-107">Permissions</span></span>
<span data-ttu-id="01b00-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01b00-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01b00-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01b00-110">Permission type</span></span>      | <span data-ttu-id="01b00-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01b00-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01b00-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01b00-112">Delegated (work or school account)</span></span> | <span data-ttu-id="01b00-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01b00-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="01b00-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01b00-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01b00-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01b00-115">Not supported.</span></span>    |
|<span data-ttu-id="01b00-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01b00-116">Application</span></span> | <span data-ttu-id="01b00-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01b00-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="01b00-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01b00-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="01b00-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="01b00-119">Optional request headers</span></span>
| <span data-ttu-id="01b00-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="01b00-120">Name</span></span>       | <span data-ttu-id="01b00-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="01b00-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="01b00-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="01b00-122">Authorization</span></span>  | <span data-ttu-id="01b00-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01b00-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="01b00-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="01b00-125">If-Match</span></span>  | <span data-ttu-id="01b00-p104">Último valor ETag conocido para que se actualice **plannerTask**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01b00-p104">Last known ETag value for the **plannerTask** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="01b00-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01b00-128">Request body</span></span>
<span data-ttu-id="01b00-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="01b00-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="01b00-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01b00-132">Property</span></span>     | <span data-ttu-id="01b00-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="01b00-133">Type</span></span>   |<span data-ttu-id="01b00-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="01b00-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01b00-135">appliedCategories</span><span class="sxs-lookup"><span data-stu-id="01b00-135">appliedCategories</span></span>|[<span data-ttu-id="01b00-136">plannerAppliedCategories</span><span class="sxs-lookup"><span data-stu-id="01b00-136">plannerAppliedCategories</span></span>](../resources/plannerappliedcategories.md)|<span data-ttu-id="01b00-p106">Categorías a las que se ha aplicado la tarea. Consulte [las categorías aplicadas](../resources/plannerappliedcategories.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="01b00-p106">The categories to which the task has been applied. See [applied Categories](../resources/plannerappliedcategories.md) for possible values.</span></span>|
|<span data-ttu-id="01b00-139">assigneePriority</span><span class="sxs-lookup"><span data-stu-id="01b00-139">assigneePriority</span></span>|<span data-ttu-id="01b00-140">String</span><span class="sxs-lookup"><span data-stu-id="01b00-140">String</span></span>|<span data-ttu-id="01b00-p107">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="01b00-p107">Hint used to order items of this type in a list view. The format is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="01b00-143">assignments</span><span class="sxs-lookup"><span data-stu-id="01b00-143">assignments</span></span>|[<span data-ttu-id="01b00-144">plannerAssignments</span><span class="sxs-lookup"><span data-stu-id="01b00-144">plannerAssignments</span></span>](../resources/plannerassignments.md)|<span data-ttu-id="01b00-145">Conjunto de usuarios al que se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="01b00-145">The set of users the task is assigned to.</span></span>|
|<span data-ttu-id="01b00-146">bucketId</span><span class="sxs-lookup"><span data-stu-id="01b00-146">bucketId</span></span>|<span data-ttu-id="01b00-147">String</span><span class="sxs-lookup"><span data-stu-id="01b00-147">String</span></span>|<span data-ttu-id="01b00-148">Identificador de cubo al que pertenece la tarea.</span><span class="sxs-lookup"><span data-stu-id="01b00-148">Bucket id to which the task belongs.</span></span> <span data-ttu-id="01b00-149">Debe estar en el plan de que la tarea se encuentra en el cubo.</span><span class="sxs-lookup"><span data-stu-id="01b00-149">The bucket needs to be in the plan that the task is in.</span></span> <span data-ttu-id="01b00-150">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="01b00-150">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="01b00-151">[Validación de formato](../resources/tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="01b00-151">[Format validation](../resources/tasks-identifiers-disclaimer.md) is done on the service.</span></span> |
|<span data-ttu-id="01b00-152">conversationThreadId</span><span class="sxs-lookup"><span data-stu-id="01b00-152">conversationThreadId</span></span>|<span data-ttu-id="01b00-153">String</span><span class="sxs-lookup"><span data-stu-id="01b00-153">String</span></span>|<span data-ttu-id="01b00-p109">Identificador de subproceso de la conversación en la tarea. Es el identificador del objeto de subproceso de conversación creado en el grupo.</span><span class="sxs-lookup"><span data-stu-id="01b00-p109">Thread id of the conversation on the task. This is the id of the conversation thread object created in the group.</span></span>|
|<span data-ttu-id="01b00-156">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="01b00-156">dueDateTime</span></span>|<span data-ttu-id="01b00-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01b00-157">DateTimeOffset</span></span>|<span data-ttu-id="01b00-p110">Fecha y hora en que vence la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="01b00-p110">Date and time at which the task is due. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="01b00-161">orderHint</span><span class="sxs-lookup"><span data-stu-id="01b00-161">orderHint</span></span>|<span data-ttu-id="01b00-162">String</span><span class="sxs-lookup"><span data-stu-id="01b00-162">String</span></span>|<span data-ttu-id="01b00-p111">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="01b00-p111">Hint used to order items of this type in a list view. The format is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="01b00-165">percentComplete</span><span class="sxs-lookup"><span data-stu-id="01b00-165">percentComplete</span></span>|<span data-ttu-id="01b00-166">Int32</span><span class="sxs-lookup"><span data-stu-id="01b00-166">Int32</span></span>|<span data-ttu-id="01b00-p112">Porcentaje de finalización de la tarea. Si se establece en `100`, la tarea se considera finalizada.</span><span class="sxs-lookup"><span data-stu-id="01b00-p112">Percentage of task completion. When set to `100`, the task is considered completed.</span></span> |
|<span data-ttu-id="01b00-169">planId</span><span class="sxs-lookup"><span data-stu-id="01b00-169">planId</span></span>|<span data-ttu-id="01b00-170">String</span><span class="sxs-lookup"><span data-stu-id="01b00-170">String</span></span>|<span data-ttu-id="01b00-171">Id. de plan al que pertenece la tarea.</span><span class="sxs-lookup"><span data-stu-id="01b00-171">Plan id to which the task belongs.</span></span>|
|<span data-ttu-id="01b00-172">startDateTime</span><span class="sxs-lookup"><span data-stu-id="01b00-172">startDateTime</span></span>|<span data-ttu-id="01b00-173">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01b00-173">DateTimeOffset</span></span>|<span data-ttu-id="01b00-p113">Fecha y hora en que comienza la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="01b00-p113">Date and time at which the task starts. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="01b00-177">title</span><span class="sxs-lookup"><span data-stu-id="01b00-177">title</span></span>|<span data-ttu-id="01b00-178">String</span><span class="sxs-lookup"><span data-stu-id="01b00-178">String</span></span>|<span data-ttu-id="01b00-179">Título de la tarea.</span><span class="sxs-lookup"><span data-stu-id="01b00-179">Title of the task.</span></span>|

## <a name="response"></a><span data-ttu-id="01b00-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01b00-180">Response</span></span>

<span data-ttu-id="01b00-181">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTask](../resources/plannertask.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01b00-181">If successful, this method returns a `200 OK` response code and updated [plannerTask](../resources/plannertask.md) object in the response body.</span></span>

<span data-ttu-id="01b00-p114">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="01b00-p114">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="01b00-185">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01b00-185">Example</span></span>
##### <a name="request"></a><span data-ttu-id="01b00-186">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01b00-186">Request</span></span>
<span data-ttu-id="01b00-187">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01b00-187">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannertask"
}-->
```http
PATCH https://graph.microsoft.com/beta/planner/tasks/01gzSlKkIUSUl6DF_EilrmQAKDhh
Content-type: application/json
Content-length: 247
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "assignments": {
    "fbab97d0-4932-4511-b675-204639209557": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "orderHint": "N9917 U2883!"
    }
  },
  "appliedCategories": {
    "category3": true,
    "category4": false
  }
}
```
##### <a name="response"></a><span data-ttu-id="01b00-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01b00-188">Response</span></span>
<span data-ttu-id="01b00-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01b00-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1423

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
  "createdDateTime": "2015-03-24T18:36:49.2407981Z",
  "assignments": {
    "6463a5ce-2119-4198-9f2a-628761df4a62": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "assignedBy": {
        "user": {
          "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
        }
      },
      "assignedDateTime": "2015-03-25T18:38:21.956Z",
      "orderHint": "N9917"
    },
    "fbab97d0-4932-4511-b675-204639209557": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "assignedBy": {
        "user": {
          "id": "1e9955d2-6acd-45bf-86d3-b546fdc795eb"
        }
      },
      "assignedDateTime": "2017-04-24T22:40:44.5665917",
      "orderHint": "RWk1"
    },
    "aaa27244-1db4-476a-a5cb-004607466324": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "assignedBy": {
        "user": {
          "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
        }
      },
      "assignedDateTime": "2015-03-25T18:38:21.956Z",
      "orderHint": "U2883"
    }
  },
  "appliedCategories": {
    "category3": true,
    "category5": true,
    "category6": true,
  },
  "id":"01gzSlKkIUSUl6DF_EilrmQAKDhh"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannertask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->