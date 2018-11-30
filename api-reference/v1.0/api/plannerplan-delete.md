---
title: Eliminar plannerPlan
description: Eliminar **plannerPlan**.
ms.openlocfilehash: 2f263996ef43acc09f9776a8f9ccd9cd70d70e77
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030983"
---
# <a name="delete-plannerplan"></a><span data-ttu-id="fa296-103">Eliminar plannerPlan</span><span class="sxs-lookup"><span data-stu-id="fa296-103">Delete plannerPlan</span></span>

<span data-ttu-id="fa296-104">Eliminar **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="fa296-104">Delete **plannerPlan**.</span></span>
## <a name="permissions"></a><span data-ttu-id="fa296-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fa296-105">Permissions</span></span>
<span data-ttu-id="fa296-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fa296-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fa296-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fa296-108">Permission type</span></span>      | <span data-ttu-id="fa296-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fa296-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fa296-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fa296-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fa296-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fa296-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="fa296-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fa296-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fa296-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa296-113">Not supported.</span></span>    |
|<span data-ttu-id="fa296-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fa296-114">Application</span></span> | <span data-ttu-id="fa296-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa296-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fa296-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fa296-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /planner/plans/{id}

```
## <a name="request-headers"></a><span data-ttu-id="fa296-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fa296-117">Request headers</span></span>
| <span data-ttu-id="fa296-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="fa296-118">Name</span></span>       | <span data-ttu-id="fa296-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa296-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fa296-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="fa296-120">Authorization</span></span>  | <span data-ttu-id="fa296-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fa296-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fa296-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="fa296-123">If-Match</span></span>  | <span data-ttu-id="fa296-p103">Último valor ETag conocido para que se elimine **plannerPlan**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fa296-p103">Last known ETag value for the **plannerPlan** to be deleted. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fa296-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="fa296-126">Request body</span></span>
<span data-ttu-id="fa296-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fa296-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fa296-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa296-128">Response</span></span>

<span data-ttu-id="fa296-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa296-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="fa296-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="fa296-p105">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="fa296-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa296-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fa296-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fa296-135">Request</span></span>
<span data-ttu-id="fa296-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa296-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_plannerplan"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/planner/plans/{id}
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="
```
##### <a name="response"></a><span data-ttu-id="fa296-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa296-137">Response</span></span>
<span data-ttu-id="fa296-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fa296-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete plannerPlan",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->