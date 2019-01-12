---
title: Eliminar plannerBucket
description: Eliminar **plannerBucket**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: d1c3f0540b3a27a396229fa19dac2bcfe3a231de
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933228"
---
# <a name="delete-plannerbucket"></a><span data-ttu-id="3f192-103">Eliminar plannerBucket</span><span class="sxs-lookup"><span data-stu-id="3f192-103">Delete plannerBucket</span></span>

> <span data-ttu-id="3f192-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f192-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f192-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f192-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3f192-106">Eliminar **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="3f192-106">Delete **plannerBucket**.</span></span>
## <a name="permissions"></a><span data-ttu-id="3f192-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3f192-107">Permissions</span></span>
<span data-ttu-id="3f192-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f192-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f192-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f192-110">Permission type</span></span>      | <span data-ttu-id="3f192-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f192-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3f192-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f192-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3f192-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f192-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="3f192-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f192-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3f192-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f192-115">Not supported.</span></span>    |
|<span data-ttu-id="3f192-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f192-116">Application</span></span> | <span data-ttu-id="3f192-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f192-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3f192-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f192-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /planner/buckets/<id>
```
## <a name="request-headers"></a><span data-ttu-id="3f192-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f192-119">Request headers</span></span>
| <span data-ttu-id="3f192-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f192-120">Name</span></span>       | <span data-ttu-id="3f192-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f192-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3f192-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3f192-122">Authorization</span></span>  | <span data-ttu-id="3f192-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f192-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3f192-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="3f192-125">If-Match</span></span>  | <span data-ttu-id="3f192-p104">Último valor ETag conocido para que se elimine **plannerBucket**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f192-p104">Last known ETag value for the **plannerBucket** to be deleted. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f192-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f192-128">Request body</span></span>
<span data-ttu-id="3f192-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3f192-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3f192-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f192-130">Response</span></span>

<span data-ttu-id="3f192-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f192-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="3f192-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="3f192-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="3f192-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f192-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3f192-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f192-137">Request</span></span>
<span data-ttu-id="3f192-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f192-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_plannerbucket"
}-->
```http
DELETE https://graph.microsoft.com/beta/planner/buckets/<id>
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="
```
##### <a name="response"></a><span data-ttu-id="3f192-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f192-139">Response</span></span>
<span data-ttu-id="3f192-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f192-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete plannerBucket",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
