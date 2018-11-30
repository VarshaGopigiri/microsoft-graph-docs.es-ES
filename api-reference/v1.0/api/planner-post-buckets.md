---
title: Crear plannerBucket
description: Use esta API para crear un objeto **plannerBucket**.
ms.openlocfilehash: 4e766c33e26fdbca15f957bad66781a90a3a0c8d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029323"
---
# <a name="create-plannerbucket"></a><span data-ttu-id="216da-103">Crear plannerBucket</span><span class="sxs-lookup"><span data-stu-id="216da-103">Create plannerBucket</span></span>

<span data-ttu-id="216da-104">Use esta API para crear un objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="216da-104">Use this API to create a new **plannerBucket**.</span></span>

## <a name="permissions"></a><span data-ttu-id="216da-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="216da-105">Permissions</span></span>
<span data-ttu-id="216da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="216da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="216da-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="216da-108">Permission type</span></span>      | <span data-ttu-id="216da-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="216da-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="216da-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="216da-110">Delegated (work or school account)</span></span> | <span data-ttu-id="216da-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="216da-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="216da-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="216da-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="216da-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="216da-113">Not supported.</span></span>    |
|<span data-ttu-id="216da-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="216da-114">Application</span></span> | <span data-ttu-id="216da-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="216da-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="216da-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="216da-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /planner/buckets

```
## <a name="request-headers"></a><span data-ttu-id="216da-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="216da-117">Request headers</span></span>
| <span data-ttu-id="216da-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="216da-118">Name</span></span>       | <span data-ttu-id="216da-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="216da-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="216da-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="216da-120">Authorization</span></span>  | <span data-ttu-id="216da-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="216da-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="216da-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="216da-123">Request body</span></span>
<span data-ttu-id="216da-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerBucket](../resources/plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="216da-124">In the request body, supply a JSON representation of [plannerBucket](../resources/plannerbucket.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="216da-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="216da-125">Response</span></span>

<span data-ttu-id="216da-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [plannerBucket](../resources/plannerbucket.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="216da-126">If successful, this method returns `201 Created` response code and [plannerBucket](../resources/plannerbucket.md) object in the response body.</span></span>

<span data-ttu-id="216da-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="216da-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="216da-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="216da-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="216da-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="216da-131">Request</span></span>
<span data-ttu-id="216da-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="216da-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_plannerbucket_from_planner"
}-->
```http
POST https://graph.microsoft.com/v1.0/planner/buckets
Content-type: application/json
Content-length: 92

{
  "name": "Advertising",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "orderHint": " !"
}
```
<span data-ttu-id="216da-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerBucket](../resources/plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="216da-133">In the request body, supply a JSON representation of [plannerBucket](../resources/plannerbucket.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="216da-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="216da-134">Response</span></span>
<span data-ttu-id="216da-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="216da-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucket"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 145

{
  "name": "Advertising",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "orderHint": "85752723360752+",
  "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create plannerBucket",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->