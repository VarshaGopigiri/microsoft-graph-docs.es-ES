---
title: Enumerar planes
description: Recuperar una lista de objetos **plannerPlan** que pertenecen a un objeto de grupo.
ms.openlocfilehash: fd1dd605952dbc4627e6c87a130e3b478f7f0947
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089610"
---
# <a name="list-plans"></a><span data-ttu-id="23de5-103">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="23de5-103">List plans</span></span>

> <span data-ttu-id="23de5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="23de5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="23de5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="23de5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="23de5-106">Recuperar una lista de objetos **plannerPlan** que pertenecen a un objeto de [grupo](../resources/group.md) .</span><span class="sxs-lookup"><span data-stu-id="23de5-106">Retrieve a list of **plannerPlan** objects owned by a [group](../resources/group.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="23de5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="23de5-107">Permissions</span></span>
<span data-ttu-id="23de5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="23de5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="23de5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="23de5-110">Permission type</span></span>      | <span data-ttu-id="23de5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="23de5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="23de5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="23de5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="23de5-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="23de5-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="23de5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="23de5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="23de5-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23de5-115">Not supported.</span></span>    |
|<span data-ttu-id="23de5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="23de5-116">Application</span></span> | <span data-ttu-id="23de5-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23de5-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="23de5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="23de5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{group-id}/planner/plans
```

## <a name="request-headers"></a><span data-ttu-id="23de5-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="23de5-119">Request headers</span></span>
| <span data-ttu-id="23de5-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="23de5-120">Name</span></span>      |<span data-ttu-id="23de5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="23de5-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="23de5-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="23de5-122">Authorization</span></span>  | <span data-ttu-id="23de5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="23de5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="23de5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="23de5-125">Request body</span></span>
<span data-ttu-id="23de5-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="23de5-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="23de5-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="23de5-127">Response</span></span>

<span data-ttu-id="23de5-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="23de5-128">If successful, this method returns a `200 OK` response code and collection of [plannerPlan](../resources/plannerplan.md) objects in the response body.</span></span>

<span data-ttu-id="23de5-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="23de5-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>
## <a name="example"></a><span data-ttu-id="23de5-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23de5-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="23de5-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="23de5-133">Request</span></span>
<span data-ttu-id="23de5-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="23de5-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plans"
}-->
```http
GET https://graph.microsoft.com/beta/groups/ebf3b108-5234-4e22-b93d-656d7dae5874/planner/plans
```
##### <a name="response"></a><span data-ttu-id="23de5-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="23de5-135">Response</span></span>
<span data-ttu-id="23de5-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="23de5-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 421

{
  "value": [
    {
      "createdBy": {
        "application": {
          "id": "95e27074-6c4a-447a-aa24-9d718a0b86fa"
        },
        "user": {
          "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
        }
      },
      "createdDateTime": "2015-03-30T18:36:49.2407981Z",
      "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
      "title": "title-value",
      "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List plans",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->