---
title: Eliminar plannerTask
description: Eliminar **plannerTask**.
localization_priority: Normal
ms.openlocfilehash: bf33164bf1cc97838af8dc0d8ef28395ccd03b5a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820933"
---
# <a name="delete-plannertask"></a><span data-ttu-id="4d5b1-103">Eliminar plannerTask</span><span class="sxs-lookup"><span data-stu-id="4d5b1-103">Delete plannerTask</span></span>

<span data-ttu-id="4d5b1-104">Eliminar **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-104">Delete **plannerTask**.</span></span>
## <a name="permissions"></a><span data-ttu-id="4d5b1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d5b1-105">Permissions</span></span>
<span data-ttu-id="4d5b1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d5b1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4d5b1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d5b1-108">Permission type</span></span>      | <span data-ttu-id="4d5b1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d5b1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4d5b1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d5b1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4d5b1-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d5b1-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="4d5b1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d5b1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d5b1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-113">Not supported.</span></span>    |
|<span data-ttu-id="4d5b1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d5b1-114">Application</span></span> | <span data-ttu-id="4d5b1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d5b1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d5b1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /planner/tasks/{id}
```
## <a name="request-headers"></a><span data-ttu-id="4d5b1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d5b1-117">Request headers</span></span>
| <span data-ttu-id="4d5b1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d5b1-118">Name</span></span>       | <span data-ttu-id="4d5b1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d5b1-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4d5b1-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d5b1-120">Authorization</span></span>  | <span data-ttu-id="4d5b1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4d5b1-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="4d5b1-123">If-Match</span></span>  | <span data-ttu-id="4d5b1-p103">Último valor ETag conocido para que se elimine **plannerTask**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-p103">Last known ETag value for the **plannerTask** to be deleted. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4d5b1-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d5b1-126">Request body</span></span>
<span data-ttu-id="4d5b1-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4d5b1-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d5b1-128">Response</span></span>

<span data-ttu-id="4d5b1-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="4d5b1-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="4d5b1-p105">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="4d5b1-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d5b1-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4d5b1-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d5b1-135">Request</span></span>
<span data-ttu-id="4d5b1-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_plannertask"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/planner/tasks/{id}
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="
```
##### <a name="response"></a><span data-ttu-id="4d5b1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d5b1-137">Response</span></span>
<span data-ttu-id="4d5b1-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d5b1-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
