---
title: Eliminar plannerTask
description: Eliminar **plannerTask**.
ms.openlocfilehash: e78dbd5c540d1c1ab16b1c009309b8aeb58def88
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030513"
---
# <a name="delete-plannertask"></a><span data-ttu-id="0e35b-103">Eliminar plannerTask</span><span class="sxs-lookup"><span data-stu-id="0e35b-103">Delete plannerTask</span></span>

<span data-ttu-id="0e35b-104">Eliminar **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="0e35b-104">Delete **plannerTask**.</span></span>
## <a name="permissions"></a><span data-ttu-id="0e35b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e35b-105">Permissions</span></span>
<span data-ttu-id="0e35b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e35b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e35b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e35b-108">Permission type</span></span>      | <span data-ttu-id="0e35b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e35b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0e35b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e35b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0e35b-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e35b-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="0e35b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e35b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0e35b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e35b-113">Not supported.</span></span>    |
|<span data-ttu-id="0e35b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e35b-114">Application</span></span> | <span data-ttu-id="0e35b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e35b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0e35b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e35b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /planner/tasks/{id}
```
## <a name="request-headers"></a><span data-ttu-id="0e35b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e35b-117">Request headers</span></span>
| <span data-ttu-id="0e35b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e35b-118">Name</span></span>       | <span data-ttu-id="0e35b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e35b-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0e35b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e35b-120">Authorization</span></span>  | <span data-ttu-id="0e35b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e35b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0e35b-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="0e35b-123">If-Match</span></span>  | <span data-ttu-id="0e35b-p103">Último valor ETag conocido para que se elimine **plannerTask**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e35b-p103">Last known ETag value for the **plannerTask** to be deleted. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0e35b-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e35b-126">Request body</span></span>
<span data-ttu-id="0e35b-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0e35b-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0e35b-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e35b-128">Response</span></span>

<span data-ttu-id="0e35b-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e35b-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="0e35b-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="0e35b-p105">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="0e35b-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e35b-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0e35b-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e35b-135">Request</span></span>
<span data-ttu-id="0e35b-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e35b-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_plannertask"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/planner/tasks/{id}
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="
```
##### <a name="response"></a><span data-ttu-id="0e35b-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e35b-137">Response</span></span>
<span data-ttu-id="0e35b-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e35b-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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