---
title: Actualizar plannerBucketTaskBoardTaskFormat
description: Actualizar las propiedades del objeto **plannerBucketTaskBoardTaskFormat**.
ms.openlocfilehash: 3931492f1bafafaa269fb926afbc2cc431ba3b3f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030518"
---
# <a name="update-plannerbuckettaskboardtaskformat"></a><span data-ttu-id="ab062-103">Actualizar plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="ab062-103">Update plannerBucketTaskBoardTaskFormat</span></span>

<span data-ttu-id="ab062-104">Actualizar las propiedades del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="ab062-104">Update the properties of **plannerBucketTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ab062-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ab062-105">Permissions</span></span>
<span data-ttu-id="ab062-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab062-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ab062-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab062-108">Permission type</span></span>      | <span data-ttu-id="ab062-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab062-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ab062-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab062-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ab062-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab062-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ab062-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab062-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ab062-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab062-113">Not supported.</span></span>    |
|<span data-ttu-id="ab062-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab062-114">Application</span></span> | <span data-ttu-id="ab062-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab062-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ab062-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab062-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/{id}/bucketTaskBoardFormat
```
## <a name="optional-request-headers"></a><span data-ttu-id="ab062-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ab062-117">Optional request headers</span></span>
| <span data-ttu-id="ab062-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab062-118">Name</span></span>       | <span data-ttu-id="ab062-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab062-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ab062-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ab062-120">Authorization</span></span>  | <span data-ttu-id="ab062-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab062-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ab062-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="ab062-123">If-Match</span></span>  | <span data-ttu-id="ab062-p103">Último valor ETag conocido para que se actualice **plannerBucketTaskBoardTaskFormat**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab062-p103">Last known ETag value for the **plannerBucketTaskBoardTaskFormat** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ab062-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ab062-126">Request body</span></span>
<span data-ttu-id="ab062-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ab062-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ab062-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab062-130">Property</span></span>     | <span data-ttu-id="ab062-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab062-131">Type</span></span>   |<span data-ttu-id="ab062-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab062-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ab062-133">orderHint</span><span class="sxs-lookup"><span data-stu-id="ab062-133">orderHint</span></span>|<span data-ttu-id="ab062-134">String</span><span class="sxs-lookup"><span data-stu-id="ab062-134">String</span></span>|<span data-ttu-id="ab062-p105">Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="ab062-p105">Hint used to order tasks in the Bucket view of the Task Board. The format is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|

## <a name="response"></a><span data-ttu-id="ab062-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab062-137">Response</span></span>

<span data-ttu-id="ab062-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab062-138">If successful, this method returns a `200 OK` response code and updated [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="ab062-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="ab062-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="ab062-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab062-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ab062-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab062-143">Request</span></span>
<span data-ttu-id="ab062-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab062-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerbuckettaskboardtaskformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/bucketTaskBoardFormat
Content-type: application/json
Content-length: 34
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "orderHint": "A6673H Ejkl!"
}
```
##### <a name="response"></a><span data-ttu-id="ab062-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab062-145">Response</span></span>
<span data-ttu-id="ab062-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab062-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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