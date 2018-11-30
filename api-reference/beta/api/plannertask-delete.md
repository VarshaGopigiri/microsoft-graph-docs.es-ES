---
title: Eliminar plannerTask
description: Eliminar **plannerTask**.
ms.openlocfilehash: c196f7d0683552f22f8089c7191eb7d25cc56f34
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087387"
---
# <a name="delete-plannertask"></a><span data-ttu-id="bf1d9-103">Eliminar plannerTask</span><span class="sxs-lookup"><span data-stu-id="bf1d9-103">Delete plannerTask</span></span>

> <span data-ttu-id="bf1d9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf1d9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bf1d9-106">Eliminar **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-106">Delete **plannerTask**.</span></span>
## <a name="permissions"></a><span data-ttu-id="bf1d9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf1d9-107">Permissions</span></span>
<span data-ttu-id="bf1d9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf1d9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf1d9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf1d9-110">Permission type</span></span>      | <span data-ttu-id="bf1d9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf1d9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bf1d9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf1d9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bf1d9-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf1d9-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="bf1d9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf1d9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bf1d9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-115">Not supported.</span></span>    |
|<span data-ttu-id="bf1d9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf1d9-116">Application</span></span> | <span data-ttu-id="bf1d9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bf1d9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf1d9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /planner/tasks/<id>
```
## <a name="request-headers"></a><span data-ttu-id="bf1d9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf1d9-119">Request headers</span></span>
| <span data-ttu-id="bf1d9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf1d9-120">Name</span></span>       | <span data-ttu-id="bf1d9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf1d9-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bf1d9-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf1d9-122">Authorization</span></span>  | <span data-ttu-id="bf1d9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bf1d9-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="bf1d9-125">If-Match</span></span>  | <span data-ttu-id="bf1d9-p104">Último valor ETag conocido para que se elimine **plannerTask**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-p104">Last known ETag value for the **plannerTask** to be deleted. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bf1d9-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf1d9-128">Request body</span></span>
<span data-ttu-id="bf1d9-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bf1d9-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf1d9-130">Response</span></span>

<span data-ttu-id="bf1d9-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="bf1d9-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="bf1d9-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="bf1d9-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf1d9-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bf1d9-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf1d9-137">Request</span></span>
<span data-ttu-id="bf1d9-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_plannertask"
}-->
```http
DELETE https://graph.microsoft.com/beta/planner/tasks/<id>
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="
```
##### <a name="response"></a><span data-ttu-id="bf1d9-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf1d9-139">Response</span></span>
<span data-ttu-id="bf1d9-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf1d9-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete plannerTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->