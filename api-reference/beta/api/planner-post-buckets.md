---
title: Crear plannerBucket
description: Use esta API para crear un objeto **plannerBucket**.
ms.openlocfilehash: 259f24fa82699f4591ad8a30d305cb3a5a7f2b59
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085932"
---
# <a name="create-plannerbucket"></a><span data-ttu-id="77c69-103">Crear plannerBucket</span><span class="sxs-lookup"><span data-stu-id="77c69-103">Create plannerBucket</span></span>

> <span data-ttu-id="77c69-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77c69-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77c69-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77c69-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="77c69-106">Use esta API para crear un objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="77c69-106">Use this API to create a new **plannerBucket**.</span></span>

## <a name="permissions"></a><span data-ttu-id="77c69-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="77c69-107">Permissions</span></span>
<span data-ttu-id="77c69-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77c69-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="77c69-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77c69-110">Permission type</span></span>      | <span data-ttu-id="77c69-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77c69-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="77c69-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77c69-112">Delegated (work or school account)</span></span> | <span data-ttu-id="77c69-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="77c69-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="77c69-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77c69-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77c69-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77c69-115">Not supported.</span></span>    |
|<span data-ttu-id="77c69-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77c69-116">Application</span></span> | <span data-ttu-id="77c69-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77c69-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="77c69-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77c69-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /planner/buckets

```
## <a name="request-headers"></a><span data-ttu-id="77c69-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77c69-119">Request headers</span></span>
| <span data-ttu-id="77c69-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="77c69-120">Name</span></span>       | <span data-ttu-id="77c69-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="77c69-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="77c69-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="77c69-122">Authorization</span></span>  | <span data-ttu-id="77c69-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77c69-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="77c69-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77c69-125">Request body</span></span>
<span data-ttu-id="77c69-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerBucket](../resources/plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="77c69-126">In the request body, supply a JSON representation of [plannerBucket](../resources/plannerbucket.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="77c69-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77c69-127">Response</span></span>

<span data-ttu-id="77c69-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [plannerBucket](../resources/plannerbucket.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77c69-128">If successful, this method returns `201 Created` response code and [plannerBucket](../resources/plannerbucket.md) object in the response body.</span></span>

<span data-ttu-id="77c69-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="77c69-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="77c69-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77c69-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="77c69-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77c69-133">Request</span></span>
<span data-ttu-id="77c69-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77c69-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_plannerbucket_from_planner"
}-->
```http
POST https://graph.microsoft.com/beta/planner/buckets
Content-type: application/json
Content-length: 92

{
  "name": "Advertising",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "orderHint": " !"
}
```
<span data-ttu-id="77c69-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerBucket](../resources/plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="77c69-135">In the request body, supply a JSON representation of [plannerBucket](../resources/plannerbucket.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="77c69-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77c69-136">Response</span></span>
<span data-ttu-id="77c69-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77c69-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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