# <a name="update-plannerplandetails"></a><span data-ttu-id="54af8-101">Actualizar plannerplandetails</span><span class="sxs-lookup"><span data-stu-id="54af8-101">Update plannerplandetails</span></span>

<span data-ttu-id="54af8-102">Actualizar las propiedades del objeto **plannerplandetails**.</span><span class="sxs-lookup"><span data-stu-id="54af8-102">Update the properties of **plannerplandetails** object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54af8-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54af8-103">Prerequisites</span></span>
<span data-ttu-id="54af8-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="54af8-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="54af8-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="54af8-105">*Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="54af8-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54af8-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/plans/<id>/details
```
## <a name="optional-request-headers"></a><span data-ttu-id="54af8-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="54af8-107">Optional request headers</span></span>
| <span data-ttu-id="54af8-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="54af8-108">Name</span></span>       | <span data-ttu-id="54af8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="54af8-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="54af8-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="54af8-110">Authorization</span></span>  | <span data-ttu-id="54af8-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54af8-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="54af8-113">If-Match</span><span class="sxs-lookup"><span data-stu-id="54af8-113">If-Match</span></span>  | <span data-ttu-id="54af8-p102">Último valor ETag conocido para que se actualice plannerPlanDetails. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54af8-p102">Last known ETag value for the plannerPlanDetails to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="54af8-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="54af8-116">Request body</span></span>
<span data-ttu-id="54af8-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="54af8-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="54af8-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54af8-120">Property</span></span>     | <span data-ttu-id="54af8-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="54af8-121">Type</span></span>   |<span data-ttu-id="54af8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="54af8-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="54af8-123">categoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="54af8-123">categoryDescriptions</span></span>|[<span data-ttu-id="54af8-124">plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="54af8-124">plannerCategoryDescriptions</span></span>](../resources/plannercategorydescriptions.md)|<span data-ttu-id="54af8-125">Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan</span><span class="sxs-lookup"><span data-stu-id="54af8-125">An object that specifies the descriptions of the six categories that can be associated with tasks in the plan</span></span>|
|<span data-ttu-id="54af8-126">sharedWith</span><span class="sxs-lookup"><span data-stu-id="54af8-126">sharedWith</span></span>|[<span data-ttu-id="54af8-127">plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="54af8-127">plannerUserIds</span></span>](../resources/planneruserids.md)|<span data-ttu-id="54af8-p104">Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](../resources/group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="54af8-p104">Set of user ids that this plan is shared with. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](../resources/group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span>|

## <a name="response"></a><span data-ttu-id="54af8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54af8-131">Response</span></span>

<span data-ttu-id="54af8-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlanDetails](../resources/plannerplandetails.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54af8-132">If successful, this method returns a `200 OK` response code and updated [plannerPlanDetails](../resources/plannerplandetails.md) object in the response body.</span></span>

<span data-ttu-id="54af8-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="54af8-p105">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="54af8-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54af8-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="54af8-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54af8-137">Request</span></span>
<span data-ttu-id="54af8-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54af8-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerplandetails"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/plans/xqQg5FS2LkCp935s-FIFm2QAFkHM/details
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
##### <a name="response"></a><span data-ttu-id="54af8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54af8-139">Response</span></span>
<span data-ttu-id="54af8-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54af8-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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