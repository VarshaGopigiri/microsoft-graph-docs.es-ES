---
title: Actualizar plannerUser
description: Actualizar las propiedades de un objeto plannerUser. Puede usar esta operación para agregar o quitar los planes de lista de favoritos de los planes de un usuario e indicar que los planes del usuario ha visto recientemente.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 733743ffee8e29d66f2ebe411d127161e7e8eb2a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925892"
---
# <a name="update-planneruser"></a><span data-ttu-id="8e452-104">Actualizar plannerUser</span><span class="sxs-lookup"><span data-stu-id="8e452-104">Update plannerUser</span></span>

> <span data-ttu-id="8e452-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8e452-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8e452-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8e452-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8e452-107">Actualizar las propiedades de un objeto [plannerUser](../resources/planneruser.md) .</span><span class="sxs-lookup"><span data-stu-id="8e452-107">Update the properties of a [plannerUser](../resources/planneruser.md) object.</span></span> <span data-ttu-id="8e452-108">Puede usar esta operación para agregar o quitar los planes de lista de favoritos de los planes de un usuario e indicar que los planes del usuario ha visto recientemente.</span><span class="sxs-lookup"><span data-stu-id="8e452-108">You can use this operation to add or remove plans from a user's favorite plans list, and to indicate which plans the user has recently viewed.</span></span>

## <a name="permissions"></a><span data-ttu-id="8e452-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="8e452-109">Permissions</span></span>
<span data-ttu-id="8e452-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8e452-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8e452-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8e452-112">Permission type</span></span>      | <span data-ttu-id="8e452-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8e452-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8e452-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8e452-114">Delegated (work or school account)</span></span> | <span data-ttu-id="8e452-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8e452-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="8e452-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8e452-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8e452-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e452-117">Not supported.</span></span>    |
|<span data-ttu-id="8e452-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8e452-118">Application</span></span> | <span data-ttu-id="8e452-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e452-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8e452-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8e452-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/planner
```
## <a name="optional-request-headers"></a><span data-ttu-id="8e452-121">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="8e452-121">Optional request headers</span></span>
| <span data-ttu-id="8e452-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="8e452-122">Name</span></span>       | <span data-ttu-id="8e452-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e452-123">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="8e452-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="8e452-124">Authorization</span></span>  | <span data-ttu-id="8e452-p105">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="8e452-p105">Bearer {code}. Required.</span></span>|
| <span data-ttu-id="8e452-127">If-Match</span><span class="sxs-lookup"><span data-stu-id="8e452-127">If-Match</span></span>  | <span data-ttu-id="8e452-128">El último valor de ETag conocido para el **plannerUser** van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="8e452-128">Last known ETag value for the **plannerUser** to be updated.</span></span> <span data-ttu-id="8e452-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8e452-129">Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8e452-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8e452-130">Request body</span></span>
<span data-ttu-id="8e452-131">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="8e452-131">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="8e452-132">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8e452-132">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="8e452-133">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8e452-133">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8e452-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8e452-134">Property</span></span>     | <span data-ttu-id="8e452-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e452-135">Type</span></span>   |<span data-ttu-id="8e452-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e452-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8e452-137">favoritePlanReferences</span><span class="sxs-lookup"><span data-stu-id="8e452-137">favoritePlanReferences</span></span>|[<span data-ttu-id="8e452-138">plannerFavoritePlanReferenceCollection</span><span class="sxs-lookup"><span data-stu-id="8e452-138">plannerFavoritePlanReferenceCollection</span></span>](../resources/plannerfavoriteplanreferencecollection.md)|<span data-ttu-id="8e452-139">Cambios realizados en la colección que contiene las referencias a los planes de que el usuario ha marcado como favorito.</span><span class="sxs-lookup"><span data-stu-id="8e452-139">Changes to the collection containing the references to the plans that the user has marked as a favorite.</span></span>|
|<span data-ttu-id="8e452-140">recentPlanReferences</span><span class="sxs-lookup"><span data-stu-id="8e452-140">recentPlanReferences</span></span>|[<span data-ttu-id="8e452-141">plannerRecentPlanReferenceCollection</span><span class="sxs-lookup"><span data-stu-id="8e452-141">plannerRecentPlanReferenceCollection</span></span>](../resources/plannerrecentplanreferencecollection.md)|<span data-ttu-id="8e452-142">Cambios realizados en la colección que contiene las referencias a los planes de que el usuario ha visto recientemente.</span><span class="sxs-lookup"><span data-stu-id="8e452-142">Changes to the collection containing the references to the plans that the user has recently viewed.</span></span>|

## <a name="response"></a><span data-ttu-id="8e452-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e452-143">Response</span></span>
<span data-ttu-id="8e452-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [plannerUser](../resources/planneruser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e452-144">If successful, this method returns a `200 OK` response code and an updated [plannerUser](../resources/planneruser.md) object in the response body.</span></span>

<span data-ttu-id="8e452-p108">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="8e452-p108">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>
## <a name="example"></a><span data-ttu-id="8e452-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e452-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8e452-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8e452-149">Request</span></span>
<span data-ttu-id="8e452-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8e452-150">The following is an example of the request.</span></span> <span data-ttu-id="8e452-151">Esta solicitud agrega el plan "Discusión de la versión siguiente" con el identificador "jd8S5gOaFk2S8aWCIAJz42QAAxtD" como un favorito para el usuario y quita plan con el identificador "7oTB5aMIAE2rVo-1N-L7RmQAGX2q" de la lista de favoritos de planes.</span><span class="sxs-lookup"><span data-stu-id="8e452-151">This request adds the plan "Next Release Discussion" with ID "jd8S5gOaFk2S8aWCIAJz42QAAxtD" as a favorite for the user, and removes plan with ID "7oTB5aMIAE2rVo-1N-L7RmQAGX2q" from the favorite plans list.</span></span>
<span data-ttu-id="8e452-152">También se actualiza la última vez que la vista del plan "jd8S5gOaFk2S8aWCIAJz42QAAxtD".</span><span class="sxs-lookup"><span data-stu-id="8e452-152">It also updates the last view time of the plan "jd8S5gOaFk2S8aWCIAJz42QAAxtD".</span></span>
<!-- {
  "blockType": "ignored",
  "name": "update_planneruser"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/planner
Content-type: application/json
Content-length: 504
If-Match: W/"JzEtVXNlckRldGFpbHMgQEBAQEBAQEBAQEBAQEBIWCc="

{
  "favoritePlanReferences": {
    "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
      "@odata.type": "#microsoft.graph.plannerFavoritePlanReference",
      "orderHint": " !",
      "planTitle": "Next Release Discussion"
    },
    "7oTB5aMIAE2rVo-1N-L7RmQAGX2q": null
  },
  "recentPlanReferences": {
    "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
      "@odata.type": "#microsoft.graph.plannerRecentPlanReference",
      "lastAccessedDateTime": "2018-01-02T22:49:46.155Z",
      "planTitle": "Next Release Discussion"
    }
  }
}
```
##### <a name="response"></a><span data-ttu-id="8e452-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e452-153">Response</span></span>
<span data-ttu-id="8e452-154">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e452-154">The following is an example of the response.</span></span> 

><span data-ttu-id="8e452-p110">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8e452-p110">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerUser"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 979

{
  "favoritePlanReferences": {
    "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
      "@odata.type": "#microsoft.graph.plannerFavoritePlanReference",
      "orderHint": "8586866870001551087",
      "planTitle": "Next Release Discussion"
    },
    "uZWtCtli30CGoWLIWSat1mQAC0ai": {
      "@odata.type": "#microsoft.graph.plannerFavoritePlanReference",
      "orderHint": "8586888705198093378",
      "planTitle": "Product Support"
    }
  },
  "recentPlanReferences": {
    "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
      "@odata.type": "#microsoft.graph.plannerRecentPlanReference",
      "lastAccessedDateTime": "2018-01-02T22:49:46.155Z",
      "planTitle": "Next Release Discussion"
    },
    "XYE5pqNJu0uuRC2PM4ZQrmQAF2Pn": {
      "@odata.type": "#microsoft.graph.plannerRecentPlanReference",
      "lastAccessedDateTime": "2018-01-01T19:39:17.57Z",
      "planTitle": "Success Metrics"
    }
  },
  "id": "-YPnMJRiIUSKFyaVjYEkBWQAAc47"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update planneruser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
