# <a name="update-plannerplandetails"></a><span data-ttu-id="fdd31-101">Actualizar plannerplandetails</span><span class="sxs-lookup"><span data-stu-id="fdd31-101">Update plannerplandetails</span></span>

<span data-ttu-id="fdd31-102">Actualizar las propiedades del objeto **plannerplandetails**.</span><span class="sxs-lookup"><span data-stu-id="fdd31-102">Update the properties of **plannerplandetails** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="fdd31-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="fdd31-103">Permissions</span></span>
<span data-ttu-id="fdd31-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fdd31-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fdd31-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fdd31-106">Permission type</span></span>      | <span data-ttu-id="fdd31-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fdd31-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fdd31-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fdd31-108">Delegated (work or school account)</span></span> | <span data-ttu-id="fdd31-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fdd31-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="fdd31-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fdd31-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fdd31-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdd31-111">Not supported.</span></span>    |
|<span data-ttu-id="fdd31-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fdd31-112">Application</span></span> | <span data-ttu-id="fdd31-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdd31-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fdd31-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fdd31-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/plans/{id}/details
```
## <a name="optional-request-headers"></a><span data-ttu-id="fdd31-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="fdd31-115">Optional request headers</span></span>
| <span data-ttu-id="fdd31-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="fdd31-116">Name</span></span>       | <span data-ttu-id="fdd31-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdd31-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="fdd31-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="fdd31-118">Authorization</span></span>  | <span data-ttu-id="fdd31-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fdd31-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fdd31-121">If-Match</span><span class="sxs-lookup"><span data-stu-id="fdd31-121">If-Match</span></span>  | <span data-ttu-id="fdd31-p103">Último valor ETag conocido para que se actualice plannerPlanDetails. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fdd31-p103">Last known ETag value for the plannerPlanDetails to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fdd31-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fdd31-124">Request body</span></span>
<span data-ttu-id="fdd31-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="fdd31-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="fdd31-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fdd31-128">Property</span></span>     | <span data-ttu-id="fdd31-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdd31-129">Type</span></span>   |<span data-ttu-id="fdd31-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdd31-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fdd31-131">categoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="fdd31-131">categoryDescriptions</span></span>|[<span data-ttu-id="fdd31-132">plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="fdd31-132">plannerCategoryDescriptions</span></span>](../resources/plannercategorydescriptions.md)|<span data-ttu-id="fdd31-133">Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan</span><span class="sxs-lookup"><span data-stu-id="fdd31-133">An object that specifies the descriptions of the six categories that can be associated with tasks in the plan</span></span>|
|<span data-ttu-id="fdd31-134">sharedWith</span><span class="sxs-lookup"><span data-stu-id="fdd31-134">sharedWith</span></span>|[<span data-ttu-id="fdd31-135">plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="fdd31-135">plannerUserIds</span></span>](../resources/planneruserids.md)|<span data-ttu-id="fdd31-p105">Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](../resources/group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="fdd31-p105">Set of user ids that this plan is shared with. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](../resources/group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span>|

## <a name="response"></a><span data-ttu-id="fdd31-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdd31-139">Response</span></span>

<span data-ttu-id="fdd31-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlanDetails](../resources/plannerplandetails.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fdd31-140">If successful, this method returns a `200 OK` response code and updated [plannerPlanDetails](../resources/plannerplandetails.md) object in the response body.</span></span>

<span data-ttu-id="fdd31-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="fdd31-p106">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="fdd31-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdd31-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fdd31-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fdd31-145">Request</span></span>
<span data-ttu-id="fdd31-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fdd31-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerplandetails"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/plans/{plan-id}/details
Content-type: application/json
Content-length: 212
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "sharedWith": {
    "6463a5ce-2119-4198-9f2a-628761df4a62" : true,
    "d95e6152-f683-4d78-9ff5-67ad180fea4a" : false,
  },
  "categoryDescriptions": {
    "category1": "Indoors",
    "category3": null,
  }
}
```
##### <a name="response"></a><span data-ttu-id="fdd31-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdd31-147">Response</span></span>
<span data-ttu-id="fdd31-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fdd31-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlanDetails"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 373

{
  "sharedWith": {
    "aaa27244-1db4-476a-a5cb-004607466324" : true,
    "6463a5ce-2119-4198-9f2a-628761df4a62" : true
  },
  "categoryDescriptions": {
    "category1": "Indoors",
    "category2": "Outdoors",
    "category3": null,
    "category4": null,
    "category5": "Needs materials",
    "category6": "Needs equipment"
  },
  "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerplandetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->