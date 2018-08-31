# <a name="update-plannertask"></a><span data-ttu-id="5e276-101">Actualizar plannertask</span><span class="sxs-lookup"><span data-stu-id="5e276-101">Update plannertask</span></span>

<span data-ttu-id="5e276-102">Actualizar las propiedades del objeto **plannertask**.</span><span class="sxs-lookup"><span data-stu-id="5e276-102">Update the properties of **plannertask** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="5e276-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="5e276-103">Permissions</span></span>
<span data-ttu-id="5e276-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5e276-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5e276-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e276-106">Permission type</span></span>      | <span data-ttu-id="5e276-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e276-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5e276-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e276-108">Delegated (work or school account)</span></span> | <span data-ttu-id="5e276-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5e276-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5e276-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e276-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5e276-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e276-111">Not supported.</span></span>    |
|<span data-ttu-id="5e276-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e276-112">Application</span></span> | <span data-ttu-id="5e276-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e276-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5e276-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e276-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="5e276-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="5e276-115">Optional request headers</span></span>
| <span data-ttu-id="5e276-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e276-116">Name</span></span>       | <span data-ttu-id="5e276-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e276-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="5e276-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e276-118">Authorization</span></span>  | <span data-ttu-id="5e276-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e276-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5e276-121">If-Match</span><span class="sxs-lookup"><span data-stu-id="5e276-121">If-Match</span></span>  | <span data-ttu-id="5e276-p103">Último valor ETag conocido para que se actualice **plannerTask**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e276-p103">Last known ETag value for the **plannerTask** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5e276-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e276-124">Request body</span></span>
<span data-ttu-id="5e276-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="5e276-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="5e276-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5e276-128">Property</span></span>     | <span data-ttu-id="5e276-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e276-129">Type</span></span>   |<span data-ttu-id="5e276-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e276-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5e276-131">appliedCategories</span><span class="sxs-lookup"><span data-stu-id="5e276-131">appliedCategories</span></span>|[<span data-ttu-id="5e276-132">plannerAppliedCategories</span><span class="sxs-lookup"><span data-stu-id="5e276-132">plannerAppliedCategories</span></span>](../resources/plannerappliedcategories.md)|<span data-ttu-id="5e276-p105">Categorías a las que se ha aplicado la tarea. Consulte [las categorías aplicadas](../resources/plannerappliedcategories.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="5e276-p105">The categories to which the task has been applied. See [applied Categories](../resources/plannerappliedcategories.md) for possible values.</span></span>|
|<span data-ttu-id="5e276-135">assigneePriority</span><span class="sxs-lookup"><span data-stu-id="5e276-135">assigneePriority</span></span>|<span data-ttu-id="5e276-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e276-136">String</span></span>|<span data-ttu-id="5e276-p106">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define en [Using order hints in Planner](../resources/planner_order_hint_format.md) (Usar sugerencias de orden en Planner).</span><span class="sxs-lookup"><span data-stu-id="5e276-p106">Hint used to order items of this type in a list view. The format is defined in [Using order hints in Planner](../resources/planner_order_hint_format.md).</span></span>|
|<span data-ttu-id="5e276-139">assignments</span><span class="sxs-lookup"><span data-stu-id="5e276-139">assignments</span></span>|[<span data-ttu-id="5e276-140">plannerAssignments</span><span class="sxs-lookup"><span data-stu-id="5e276-140">plannerAssignments</span></span>](../resources/plannerassignments.md)|<span data-ttu-id="5e276-141">Conjunto de usuarios al que se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e276-141">The set of users the task is assigned to.</span></span>|
|<span data-ttu-id="5e276-142">bucketId</span><span class="sxs-lookup"><span data-stu-id="5e276-142">bucketId</span></span>|<span data-ttu-id="5e276-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e276-143">String</span></span>|<span data-ttu-id="5e276-144">Identificador de cubo al que pertenece la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e276-144">Bucket id to which the task belongs.</span></span> <span data-ttu-id="5e276-145">El cubo debe estar en el plan en el que la tarea se encuentra.</span><span class="sxs-lookup"><span data-stu-id="5e276-145">The bucket needs to be in the plan that the task is in.</span></span> <span data-ttu-id="5e276-146">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5e276-146">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="5e276-147">La [validación de formato](../resources/planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e276-147">[Format validation](../resources/planner_identifiers_disclaimer.md) is done on the service.</span></span> |
|<span data-ttu-id="5e276-148">conversationThreadId</span><span class="sxs-lookup"><span data-stu-id="5e276-148">conversationThreadId</span></span>|<span data-ttu-id="5e276-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e276-149">String</span></span>|<span data-ttu-id="5e276-p108">Identificador de subproceso de la conversación en la tarea. Es el identificador del objeto de subproceso de conversación creado en el grupo.</span><span class="sxs-lookup"><span data-stu-id="5e276-p108">Thread id of the conversation on the task. This is the id of the conversation thread object created in the group.</span></span>|
|<span data-ttu-id="5e276-152">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="5e276-152">dueDateTime</span></span>|<span data-ttu-id="5e276-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5e276-153">DateTimeOffset</span></span>|<span data-ttu-id="5e276-p109">Fecha y hora en que vence la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="5e276-p109">Date and time at which the task is due. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="5e276-157">orderHint</span><span class="sxs-lookup"><span data-stu-id="5e276-157">orderHint</span></span>|<span data-ttu-id="5e276-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e276-158">String</span></span>|<span data-ttu-id="5e276-p110">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define en [Using order hints in Planner](../resources/planner_order_hint_format.md) (Usar sugerencias de orden en Planner).</span><span class="sxs-lookup"><span data-stu-id="5e276-p110">Hint used to order items of this type in a list view. The format is defined in [Using order hints in Planner](../resources/planner_order_hint_format.md).</span></span>|
|<span data-ttu-id="5e276-161">percentComplete</span><span class="sxs-lookup"><span data-stu-id="5e276-161">percentComplete</span></span>|<span data-ttu-id="5e276-162">Int32</span><span class="sxs-lookup"><span data-stu-id="5e276-162">Int32</span></span>|<span data-ttu-id="5e276-p111">Porcentaje de finalización de la tarea. Si se establece en `100`, la tarea se considera finalizada.</span><span class="sxs-lookup"><span data-stu-id="5e276-p111">Percentage of task completion. When set to `100`, the task is considered completed.</span></span> |
|<span data-ttu-id="5e276-165">planId</span><span class="sxs-lookup"><span data-stu-id="5e276-165">planId</span></span>|<span data-ttu-id="5e276-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e276-166">String</span></span>|<span data-ttu-id="5e276-167">Id. de plan al que pertenece la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e276-167">Plan id to which the task belongs.</span></span>|
|<span data-ttu-id="5e276-168">startDateTime</span><span class="sxs-lookup"><span data-stu-id="5e276-168">startDateTime</span></span>|<span data-ttu-id="5e276-169">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5e276-169">DateTimeOffset</span></span>|<span data-ttu-id="5e276-p112">Fecha y hora en que comienza la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="5e276-p112">Date and time at which the task starts. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="5e276-173">title</span><span class="sxs-lookup"><span data-stu-id="5e276-173">title</span></span>|<span data-ttu-id="5e276-174">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e276-174">String</span></span>|<span data-ttu-id="5e276-175">Título de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e276-175">Title of the task.</span></span>|

## <a name="response"></a><span data-ttu-id="5e276-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e276-176">Response</span></span>

<span data-ttu-id="5e276-177">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTask](../resources/plannertask.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e276-177">If successful, this method returns a `200 OK` response code and updated [plannerTask](../resources/plannertask.md) object in the response body.</span></span>

<span data-ttu-id="5e276-p113">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="5e276-p113">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="5e276-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e276-181">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5e276-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e276-182">Request</span></span>
<span data-ttu-id="5e276-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e276-183">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannertask"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/{task-id}
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
##### <a name="response"></a><span data-ttu-id="5e276-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e276-184">Response</span></span>
<span data-ttu-id="5e276-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5e276-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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