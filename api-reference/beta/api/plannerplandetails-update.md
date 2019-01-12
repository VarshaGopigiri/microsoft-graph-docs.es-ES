---
title: Actualizar plannerplandetails
description: Actualizar las propiedades del objeto **plannerplandetails**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: fd42196238fb103021debf8a4fee2f658053a255
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950140"
---
# <a name="update-plannerplandetails"></a><span data-ttu-id="1da51-103">Actualizar plannerplandetails</span><span class="sxs-lookup"><span data-stu-id="1da51-103">Update plannerplandetails</span></span>

> <span data-ttu-id="1da51-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1da51-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1da51-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1da51-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1da51-106">Actualizar las propiedades del objeto **plannerplandetails**.</span><span class="sxs-lookup"><span data-stu-id="1da51-106">Update the properties of **plannerplandetails** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="1da51-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1da51-107">Permissions</span></span>
<span data-ttu-id="1da51-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1da51-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1da51-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1da51-110">Permission type</span></span>      | <span data-ttu-id="1da51-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1da51-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1da51-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1da51-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1da51-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1da51-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="1da51-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1da51-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1da51-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1da51-115">Not supported.</span></span>    |
|<span data-ttu-id="1da51-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1da51-116">Application</span></span> | <span data-ttu-id="1da51-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1da51-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1da51-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1da51-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/plans/<id>/details
```
## <a name="optional-request-headers"></a><span data-ttu-id="1da51-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="1da51-119">Optional request headers</span></span>
| <span data-ttu-id="1da51-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1da51-120">Name</span></span>       | <span data-ttu-id="1da51-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1da51-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="1da51-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1da51-122">Authorization</span></span>  | <span data-ttu-id="1da51-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1da51-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1da51-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="1da51-125">If-Match</span></span>  | <span data-ttu-id="1da51-p104">Último valor ETag conocido para que se actualice plannerPlanDetails. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1da51-p104">Last known ETag value for the plannerPlanDetails to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1da51-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1da51-128">Request body</span></span>
<span data-ttu-id="1da51-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="1da51-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="1da51-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1da51-132">Property</span></span>     | <span data-ttu-id="1da51-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="1da51-133">Type</span></span>   |<span data-ttu-id="1da51-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="1da51-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1da51-135">categoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="1da51-135">categoryDescriptions</span></span>|[<span data-ttu-id="1da51-136">plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="1da51-136">plannerCategoryDescriptions</span></span>](../resources/plannercategorydescriptions.md)|<span data-ttu-id="1da51-137">Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan</span><span class="sxs-lookup"><span data-stu-id="1da51-137">An object that specifies the descriptions of the six categories that can be associated with tasks in the plan</span></span>|
|<span data-ttu-id="1da51-138">sharedWith</span><span class="sxs-lookup"><span data-stu-id="1da51-138">sharedWith</span></span>|[<span data-ttu-id="1da51-139">plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="1da51-139">plannerUserIds</span></span>](../resources/planneruserids.md)|<span data-ttu-id="1da51-p106">Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](../resources/group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="1da51-p106">Set of user ids that this plan is shared with. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](../resources/group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span>|

## <a name="response"></a><span data-ttu-id="1da51-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1da51-143">Response</span></span>

<span data-ttu-id="1da51-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlanDetails](../resources/plannerplandetails.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1da51-144">If successful, this method returns a `200 OK` response code and updated [plannerPlanDetails](../resources/plannerplandetails.md) object in the response body.</span></span>

<span data-ttu-id="1da51-p107">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="1da51-p107">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="1da51-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1da51-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1da51-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1da51-149">Request</span></span>
<span data-ttu-id="1da51-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1da51-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerplandetails"
}-->
```http
PATCH https://graph.microsoft.com/beta/planner/plans/xqQg5FS2LkCp935s-FIFm2QAFkHM/details
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
##### <a name="response"></a><span data-ttu-id="1da51-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1da51-151">Response</span></span>
<span data-ttu-id="1da51-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1da51-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
