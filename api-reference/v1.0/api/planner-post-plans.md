---
title: Crear plannerPlan
description: Use esta API para crear un objeto **plannerPlan**.
ms.openlocfilehash: bc432bec9b69b40a41b0529c548b073086b8ffff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029267"
---
# <a name="create-plannerplan"></a><span data-ttu-id="905ad-103">Crear plannerPlan</span><span class="sxs-lookup"><span data-stu-id="905ad-103">Create plannerPlan</span></span>

<span data-ttu-id="905ad-104">Use esta API para crear un objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="905ad-104">Use this API to create a new **plannerPlan**.</span></span>

## <a name="permissions"></a><span data-ttu-id="905ad-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="905ad-105">Permissions</span></span>

<span data-ttu-id="905ad-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="905ad-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="905ad-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="905ad-108">Permission type</span></span>                        | <span data-ttu-id="905ad-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="905ad-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="905ad-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="905ad-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="905ad-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="905ad-111">Group.ReadWrite.All</span></span>                         |
| <span data-ttu-id="905ad-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="905ad-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="905ad-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="905ad-113">Not supported.</span></span>                              |
| <span data-ttu-id="905ad-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="905ad-114">Application</span></span>                            | <span data-ttu-id="905ad-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="905ad-115">Not supported.</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="905ad-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="905ad-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
``` http
POST /planner/plans
```

## <a name="request-headers"></a><span data-ttu-id="905ad-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="905ad-117">Request headers</span></span>

| <span data-ttu-id="905ad-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="905ad-118">Name</span></span>          | <span data-ttu-id="905ad-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="905ad-119">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="905ad-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="905ad-120">Authorization</span></span> | <span data-ttu-id="905ad-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="905ad-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="905ad-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="905ad-123">Request body</span></span>

<span data-ttu-id="905ad-p103">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerPlan](../resources/plannerplan.md). La propiedad de propietario **plannerPlan** se debe establecer en un identificador de un objeto [group](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="905ad-p103">In the request body, supply a JSON representation of [plannerPlan](../resources/plannerplan.md) object. The **plannerPlan** owner property must be set to an id of a [group](../resources/group.md) object.</span></span>

><span data-ttu-id="905ad-126">**Nota:** El usuario que está creando el plan debe ser miembro del grupo que será el propietario del plan.</span><span class="sxs-lookup"><span data-stu-id="905ad-126">**Note:** The user who is creating the plan must be a member of the group that will own the plan.</span></span> <span data-ttu-id="905ad-127">Cuando se crea un nuevo grupo mediante el uso de [Create group](../api/group-post-groups.md), no se agregan al grupo como un miembro.</span><span class="sxs-lookup"><span data-stu-id="905ad-127">When you create a new group by using [Create group](../api/group-post-groups.md), you are not added to the group as a member.</span></span> <span data-ttu-id="905ad-128">Una vez creado el grupo, agregarse como un miembro mediante el uso [grupo post (miembros)](../api/group-post-members.md).</span><span class="sxs-lookup"><span data-stu-id="905ad-128">After the group is created, add yourself as a member by using [group post members](../api/group-post-members.md).</span></span>


## <a name="response"></a><span data-ttu-id="905ad-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="905ad-129">Response</span></span>

<span data-ttu-id="905ad-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="905ad-130">If successful, this method returns `201 Created` response code and [plannerPlan](../resources/plannerplan.md) object in the response body.</span></span>

<span data-ttu-id="905ad-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="905ad-p105">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="905ad-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="905ad-134">Example</span></span>

### <a name="request"></a><span data-ttu-id="905ad-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="905ad-135">Request</span></span>

<span data-ttu-id="905ad-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="905ad-136">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_plannerplan_from_planner"
}-->
``` http
POST https://graph.microsoft.com/v1.0/planner/plans
Content-type: application/json
Content-length: 381

{
  "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
  "title": "title-value"
}
```

<span data-ttu-id="905ad-137">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerPlan](../resources/plannerplan.md).</span><span class="sxs-lookup"><span data-stu-id="905ad-137">In the request body, supply a JSON representation of [plannerPlan](../resources/plannerplan.md) object.</span></span>

### <a name="response"></a><span data-ttu-id="905ad-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="905ad-138">Response</span></span>

<span data-ttu-id="905ad-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="905ad-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan"
} -->
``` http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 357

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create plannerPlan",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->