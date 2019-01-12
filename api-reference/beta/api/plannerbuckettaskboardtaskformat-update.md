---
title: Actualizar plannerBucketTaskBoardTaskFormat
description: Actualizar las propiedades del objeto **plannerBucketTaskBoardTaskFormat**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 7dad7a639ce8243fe6138d813a1de0bde2da11e5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936042"
---
# <a name="update-plannerbuckettaskboardtaskformat"></a><span data-ttu-id="b4532-103">Actualizar plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="b4532-103">Update plannerBucketTaskBoardTaskFormat</span></span>

> <span data-ttu-id="b4532-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b4532-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b4532-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b4532-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b4532-106">Actualizar las propiedades del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="b4532-106">Update the properties of **plannerBucketTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="b4532-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b4532-107">Permissions</span></span>
<span data-ttu-id="b4532-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4532-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b4532-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4532-110">Permission type</span></span>      | <span data-ttu-id="b4532-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4532-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b4532-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4532-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b4532-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4532-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b4532-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4532-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b4532-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4532-115">Not supported.</span></span>    |
|<span data-ttu-id="b4532-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4532-116">Application</span></span> | <span data-ttu-id="b4532-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4532-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b4532-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4532-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>/bucketTaskBoardFormat
```
## <a name="optional-request-headers"></a><span data-ttu-id="b4532-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="b4532-119">Optional request headers</span></span>
| <span data-ttu-id="b4532-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b4532-120">Name</span></span>       | <span data-ttu-id="b4532-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4532-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="b4532-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b4532-122">Authorization</span></span>  | <span data-ttu-id="b4532-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b4532-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b4532-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="b4532-125">If-Match</span></span>  | <span data-ttu-id="b4532-p104">Último valor ETag conocido para que se actualice **plannerBucketTaskBoardTaskFormat**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b4532-p104">Last known ETag value for the **plannerBucketTaskBoardTaskFormat** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b4532-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4532-128">Request body</span></span>
<span data-ttu-id="b4532-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b4532-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b4532-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4532-132">Property</span></span>     | <span data-ttu-id="b4532-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4532-133">Type</span></span>   |<span data-ttu-id="b4532-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4532-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b4532-135">orderHint</span><span class="sxs-lookup"><span data-stu-id="b4532-135">orderHint</span></span>|<span data-ttu-id="b4532-136">String</span><span class="sxs-lookup"><span data-stu-id="b4532-136">String</span></span>|<span data-ttu-id="b4532-p106">Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="b4532-p106">Hint used to order tasks in the Bucket view of the Task Board. The format is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|

## <a name="response"></a><span data-ttu-id="b4532-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4532-139">Response</span></span>

<span data-ttu-id="b4532-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4532-140">If successful, this method returns a `200 OK` response code and updated [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="b4532-p107">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="b4532-p107">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="b4532-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4532-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b4532-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4532-145">Request</span></span>
<span data-ttu-id="b4532-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4532-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerbuckettaskboardtaskformat"
}-->
```http
PATCH https://graph.microsoft.com/beta/planner/tasks/hsOf2dhOJkqyYYZEtdzDe2QAIUCR/bucketTaskBoardFormat
Content-type: application/json
Content-length: 34
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "orderHint": "A6673H Ejkl!"
}
```
##### <a name="response"></a><span data-ttu-id="b4532-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4532-147">Response</span></span>
<span data-ttu-id="b4532-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4532-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
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
  "description": "Update plannerbuckettaskboardtaskformat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
