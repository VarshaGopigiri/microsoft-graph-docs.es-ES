---
title: Actualizar plannerPlan
description: Actualizar las propiedades del objeto **plannerPlan** .
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 46c4c5707d4e602b75e48a989e6e67136c12387a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945233"
---
# <a name="update-plannerplan"></a><span data-ttu-id="9fd4b-103">Actualizar plannerPlan</span><span class="sxs-lookup"><span data-stu-id="9fd4b-103">Update plannerPlan</span></span>

> <span data-ttu-id="9fd4b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9fd4b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9fd4b-106">Actualizar las propiedades del objeto **plannerPlan** .</span><span class="sxs-lookup"><span data-stu-id="9fd4b-106">Update the properties of **plannerPlan** object.</span></span>

## <a name="permissions"></a><span data-ttu-id="9fd4b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9fd4b-107">Permissions</span></span>
<span data-ttu-id="9fd4b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9fd4b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9fd4b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9fd4b-110">Permission type</span></span>      | <span data-ttu-id="9fd4b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9fd4b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9fd4b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9fd4b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9fd4b-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9fd4b-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="9fd4b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9fd4b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9fd4b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-115">Not supported.</span></span>    |
|<span data-ttu-id="9fd4b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9fd4b-116">Application</span></span> | <span data-ttu-id="9fd4b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9fd4b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9fd4b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/plans/<id>
```

## <a name="request-headers"></a><span data-ttu-id="9fd4b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9fd4b-119">Request headers</span></span>

| <span data-ttu-id="9fd4b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9fd4b-120">Name</span></span>       | <span data-ttu-id="9fd4b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fd4b-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="9fd4b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="9fd4b-122">Authorization</span></span>  | <span data-ttu-id="9fd4b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9fd4b-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="9fd4b-125">If-Match</span></span>  | <span data-ttu-id="9fd4b-p104">Último valor ETag conocido para que se actualice plannerPlan. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-p104">Last known ETag value for the plannerPlan to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9fd4b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9fd4b-128">Request body</span></span>
<span data-ttu-id="9fd4b-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9fd4b-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9fd4b-132">Property</span></span>     | <span data-ttu-id="9fd4b-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fd4b-133">Type</span></span>   |<span data-ttu-id="9fd4b-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fd4b-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9fd4b-135">owner</span><span class="sxs-lookup"><span data-stu-id="9fd4b-135">owner</span></span>|<span data-ttu-id="9fd4b-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fd4b-136">String</span></span>|<span data-ttu-id="9fd4b-p106">`id` del [group](../resources/group.md) que tiene el plan. Para poder establecer este campo, debe existir un grupo válido. Una vez establecido, solo lo puede actualizar el propietario.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-p106">[Group](../resources/group.md) `id` by which the plan is owned. A valid group must exist before this field can be set. Once set, this can only be updated by the owner.</span></span>|
|<span data-ttu-id="9fd4b-140">title</span><span class="sxs-lookup"><span data-stu-id="9fd4b-140">title</span></span>|<span data-ttu-id="9fd4b-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fd4b-141">String</span></span>|<span data-ttu-id="9fd4b-142">Título del plan.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-142">Title of the plan.</span></span>|

## <a name="response"></a><span data-ttu-id="9fd4b-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fd4b-143">Response</span></span>

<span data-ttu-id="9fd4b-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlan](../resources/plannerplan.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-144">If successful, this method returns a `200 OK` response code and updated [plannerPlan](../resources/plannerplan.md) object in the response body.</span></span>

<span data-ttu-id="9fd4b-p107">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="9fd4b-p107">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="9fd4b-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fd4b-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9fd4b-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9fd4b-149">Request</span></span>
<span data-ttu-id="9fd4b-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerplan"
}-->
```http
PATCH https://graph.microsoft.com/beta/planner/plans/<id>
Content-type: application/json
Content-length: 29
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "title": "title-value"
}
```
##### <a name="response"></a><span data-ttu-id="9fd4b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fd4b-151">Response</span></span>
<span data-ttu-id="9fd4b-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9fd4b-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
