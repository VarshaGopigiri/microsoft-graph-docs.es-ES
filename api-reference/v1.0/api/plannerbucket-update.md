---
title: Actualizar plannerbucket
description: Actualizar las propiedades del objeto **plannerbucket**.
localization_priority: Normal
ms.openlocfilehash: 84583df95d69f4b7f4beb604cd3cf61270c177ff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814941"
---
# <a name="update-plannerbucket"></a><span data-ttu-id="1f5bb-103">Actualizar plannerbucket</span><span class="sxs-lookup"><span data-stu-id="1f5bb-103">Update plannerbucket</span></span>

<span data-ttu-id="1f5bb-104">Actualizar las propiedades del objeto **plannerbucket**.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-104">Update the properties of **plannerbucket** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="1f5bb-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1f5bb-105">Permissions</span></span>
<span data-ttu-id="1f5bb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1f5bb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1f5bb-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1f5bb-108">Permission type</span></span>      | <span data-ttu-id="1f5bb-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1f5bb-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1f5bb-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1f5bb-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1f5bb-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1f5bb-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="1f5bb-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1f5bb-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1f5bb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-113">Not supported.</span></span>    |
|<span data-ttu-id="1f5bb-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1f5bb-114">Application</span></span> | <span data-ttu-id="1f5bb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1f5bb-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1f5bb-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/buckets/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="1f5bb-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="1f5bb-117">Optional request headers</span></span>
| <span data-ttu-id="1f5bb-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f5bb-118">Name</span></span>       | <span data-ttu-id="1f5bb-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f5bb-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="1f5bb-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1f5bb-120">Authorization</span></span>  | <span data-ttu-id="1f5bb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1f5bb-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="1f5bb-123">If-Match</span></span>  | <span data-ttu-id="1f5bb-p103">Último valor ETag conocido para que se actualice **plannerBucket**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-p103">Last known ETag value for the **plannerBucket** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1f5bb-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1f5bb-126">Request body</span></span>
<span data-ttu-id="1f5bb-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="1f5bb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f5bb-130">Property</span></span>     | <span data-ttu-id="1f5bb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f5bb-131">Type</span></span>   |<span data-ttu-id="1f5bb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f5bb-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1f5bb-133">name</span><span class="sxs-lookup"><span data-stu-id="1f5bb-133">name</span></span>|<span data-ttu-id="1f5bb-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="1f5bb-134">String</span></span>|<span data-ttu-id="1f5bb-135">Nombre del depósito.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-135">Name of the bucket.</span></span>|
|<span data-ttu-id="1f5bb-136">orderHint</span><span class="sxs-lookup"><span data-stu-id="1f5bb-136">orderHint</span></span>|<span data-ttu-id="1f5bb-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="1f5bb-137">String</span></span>|<span data-ttu-id="1f5bb-p105">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](../resources/planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="1f5bb-p105">Hint used to order items of this type in a list view. The format is defined as outlined [here](../resources/planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="1f5bb-140">planId</span><span class="sxs-lookup"><span data-stu-id="1f5bb-140">planId</span></span>|<span data-ttu-id="1f5bb-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="1f5bb-141">String</span></span>|<span data-ttu-id="1f5bb-142">Id. de plan al que pertenece el depósito.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-142">Plan id to which the bucket belongs.</span></span>|

## <a name="response"></a><span data-ttu-id="1f5bb-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f5bb-143">Response</span></span>

<span data-ttu-id="1f5bb-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucket](../resources/plannerbucket.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-144">If successful, this method returns a `200 OK` response code and updated [plannerBucket](../resources/plannerbucket.md) object in the response body.</span></span>

<span data-ttu-id="1f5bb-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="1f5bb-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="1f5bb-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1f5bb-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1f5bb-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1f5bb-149">Request</span></span>
<span data-ttu-id="1f5bb-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerbucket"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/buckets/{bucket-id}
Content-type: application/json
Content-length: 27
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "name": "Development"
}
```
##### <a name="response"></a><span data-ttu-id="1f5bb-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f5bb-151">Response</span></span>
<span data-ttu-id="1f5bb-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1f5bb-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucket"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 245

{
  "name": "Development",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "orderHint": "85752723360752+",
  "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerbucket",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
