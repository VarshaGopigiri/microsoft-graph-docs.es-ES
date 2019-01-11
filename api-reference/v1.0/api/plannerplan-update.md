---
title: Actualizar plannerPlan
description: Actualizar las propiedades del objeto **plannerPlan** .
localization_priority: Normal
ms.openlocfilehash: 55dcc8816489144b43c6dc41500bdee94190883d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856486"
---
# <a name="update-plannerplan"></a><span data-ttu-id="1c9a2-103">Actualizar plannerPlan</span><span class="sxs-lookup"><span data-stu-id="1c9a2-103">Update plannerPlan</span></span>

<span data-ttu-id="1c9a2-104">Actualizar las propiedades del objeto **plannerPlan** .</span><span class="sxs-lookup"><span data-stu-id="1c9a2-104">Update the properties of **plannerPlan** object.</span></span>

## <a name="permissions"></a><span data-ttu-id="1c9a2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1c9a2-105">Permissions</span></span>
<span data-ttu-id="1c9a2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c9a2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1c9a2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c9a2-108">Permission type</span></span>      | <span data-ttu-id="1c9a2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c9a2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1c9a2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c9a2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1c9a2-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1c9a2-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="1c9a2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c9a2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1c9a2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-113">Not supported.</span></span>    |
|<span data-ttu-id="1c9a2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c9a2-114">Application</span></span> | <span data-ttu-id="1c9a2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1c9a2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c9a2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/plans/{id}
```

## <a name="request-headers"></a><span data-ttu-id="1c9a2-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c9a2-117">Request headers</span></span>

| <span data-ttu-id="1c9a2-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c9a2-118">Name</span></span>       | <span data-ttu-id="1c9a2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c9a2-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="1c9a2-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c9a2-120">Authorization</span></span>  | <span data-ttu-id="1c9a2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1c9a2-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="1c9a2-123">If-Match</span></span>  | <span data-ttu-id="1c9a2-p103">Último valor ETag conocido para que se actualice plannerPlan. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-p103">Last known ETag value for the plannerPlan to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1c9a2-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c9a2-126">Request body</span></span>
<span data-ttu-id="1c9a2-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="1c9a2-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1c9a2-130">Property</span></span>     | <span data-ttu-id="1c9a2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c9a2-131">Type</span></span>   |<span data-ttu-id="1c9a2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c9a2-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1c9a2-133">owner</span><span class="sxs-lookup"><span data-stu-id="1c9a2-133">owner</span></span>|<span data-ttu-id="1c9a2-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="1c9a2-134">String</span></span>|<span data-ttu-id="1c9a2-p105">`id` del [group](../resources/group.md) que tiene el plan. Para poder establecer este campo, debe existir un grupo válido. Una vez establecido, solo lo puede actualizar el propietario.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-p105">[Group](../resources/group.md) `id` by which the plan is owned. A valid group must exist before this field can be set. Once set, this can only be updated by the owner.</span></span>|
|<span data-ttu-id="1c9a2-138">title</span><span class="sxs-lookup"><span data-stu-id="1c9a2-138">title</span></span>|<span data-ttu-id="1c9a2-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="1c9a2-139">String</span></span>|<span data-ttu-id="1c9a2-140">Título del plan.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-140">Title of the plan.</span></span>|

## <a name="response"></a><span data-ttu-id="1c9a2-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c9a2-141">Response</span></span>

<span data-ttu-id="1c9a2-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlan](../resources/plannerplan.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-142">If successful, this method returns a `200 OK` response code and updated [plannerPlan](../resources/plannerplan.md) object in the response body.</span></span>

<span data-ttu-id="1c9a2-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="1c9a2-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="1c9a2-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c9a2-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1c9a2-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c9a2-147">Request</span></span>
<span data-ttu-id="1c9a2-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerplan"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/plans/{plan-id}
Content-type: application/json
Content-length: 29
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "title": "title-value"
}
```
##### <a name="response"></a><span data-ttu-id="1c9a2-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c9a2-149">Response</span></span>
<span data-ttu-id="1c9a2-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c9a2-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 357

{
  "createdBy": {
    "application": {
      "id": "95e27074-6c4a-447a-aa24-9d718a0b86fa"
    },
    "user": {
      "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
    }
  },
  "createdDateTime": "2015-03-30T18:36:49.2407981Z",
  "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
  "title": "title-value",
  "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerplan",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
