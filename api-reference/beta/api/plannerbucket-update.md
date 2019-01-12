---
title: Actualizar plannerbucket
description: Actualizar las propiedades del objeto **plannerbucket**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 193b6ee4fcb26d0b4933a4458aa4c8c3891882b1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940641"
---
# <a name="update-plannerbucket"></a><span data-ttu-id="09f16-103">Actualizar plannerbucket</span><span class="sxs-lookup"><span data-stu-id="09f16-103">Update plannerbucket</span></span>

> <span data-ttu-id="09f16-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="09f16-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="09f16-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="09f16-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="09f16-106">Actualizar las propiedades del objeto **plannerbucket**.</span><span class="sxs-lookup"><span data-stu-id="09f16-106">Update the properties of **plannerbucket** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="09f16-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="09f16-107">Permissions</span></span>
<span data-ttu-id="09f16-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="09f16-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="09f16-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="09f16-110">Permission type</span></span>      | <span data-ttu-id="09f16-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="09f16-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="09f16-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="09f16-112">Delegated (work or school account)</span></span> | <span data-ttu-id="09f16-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09f16-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="09f16-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="09f16-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="09f16-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09f16-115">Not supported.</span></span>    |
|<span data-ttu-id="09f16-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="09f16-116">Application</span></span> | <span data-ttu-id="09f16-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09f16-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="09f16-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09f16-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/buckets/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="09f16-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="09f16-119">Optional request headers</span></span>
| <span data-ttu-id="09f16-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="09f16-120">Name</span></span>       | <span data-ttu-id="09f16-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="09f16-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="09f16-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="09f16-122">Authorization</span></span>  | <span data-ttu-id="09f16-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09f16-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="09f16-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="09f16-125">If-Match</span></span>  | <span data-ttu-id="09f16-p104">Último valor ETag conocido para que se actualice **plannerBucket**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09f16-p104">Last known ETag value for the **plannerBucket** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="09f16-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09f16-128">Request body</span></span>
<span data-ttu-id="09f16-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="09f16-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="09f16-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09f16-132">Property</span></span>     | <span data-ttu-id="09f16-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="09f16-133">Type</span></span>   |<span data-ttu-id="09f16-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="09f16-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="09f16-135">name</span><span class="sxs-lookup"><span data-stu-id="09f16-135">name</span></span>|<span data-ttu-id="09f16-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="09f16-136">String</span></span>|<span data-ttu-id="09f16-137">Nombre del depósito.</span><span class="sxs-lookup"><span data-stu-id="09f16-137">Name of the bucket.</span></span>|
|<span data-ttu-id="09f16-138">orderHint</span><span class="sxs-lookup"><span data-stu-id="09f16-138">orderHint</span></span>|<span data-ttu-id="09f16-139">String</span><span class="sxs-lookup"><span data-stu-id="09f16-139">String</span></span>|<span data-ttu-id="09f16-p106">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define en [Using order hints in Planner](../resources/planner-order-hint-format.md) (Usar sugerencias de orden en Planner).</span><span class="sxs-lookup"><span data-stu-id="09f16-p106">Hint used to order items of this type in a list view. The format is defined in [Using order hints in Planner](../resources/planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="09f16-142">planId</span><span class="sxs-lookup"><span data-stu-id="09f16-142">planId</span></span>|<span data-ttu-id="09f16-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="09f16-143">String</span></span>|<span data-ttu-id="09f16-144">Id. de plan al que pertenece el depósito.</span><span class="sxs-lookup"><span data-stu-id="09f16-144">Plan id to which the bucket belongs.</span></span>|

## <a name="response"></a><span data-ttu-id="09f16-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09f16-145">Response</span></span>

<span data-ttu-id="09f16-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucket](../resources/plannerbucket.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09f16-146">If successful, this method returns a `200 OK` response code and updated [plannerBucket](../resources/plannerbucket.md) object in the response body.</span></span>

<span data-ttu-id="09f16-p107">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="09f16-p107">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="09f16-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09f16-150">Example</span></span>
##### <a name="request"></a><span data-ttu-id="09f16-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="09f16-151">Request</span></span>
<span data-ttu-id="09f16-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09f16-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerbucket"
}-->
```http
PATCH https://graph.microsoft.com/beta/planner/buckets/hsOf2dhOJkqyYYZEtdzDe2QAIUCR
Content-type: application/json
Content-length: 27
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "name": "Development"
}
```
##### <a name="response"></a><span data-ttu-id="09f16-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09f16-153">Response</span></span>
<span data-ttu-id="09f16-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="09f16-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
