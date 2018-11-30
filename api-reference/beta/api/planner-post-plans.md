---
title: Crear plannerPlan
description: Use esta API para crear un objeto **plannerPlan**.
ms.openlocfilehash: 685b05cc271aaebfdb198eace416883c52ad28a0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088689"
---
# <a name="create-plannerplan"></a><span data-ttu-id="5959e-103">Crear plannerPlan</span><span class="sxs-lookup"><span data-stu-id="5959e-103">Create plannerPlan</span></span>

> <span data-ttu-id="5959e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5959e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5959e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5959e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5959e-106">Use esta API para crear un objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="5959e-106">Use this API to create a new **plannerPlan**.</span></span>

## <a name="permissions"></a><span data-ttu-id="5959e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5959e-107">Permissions</span></span>

<span data-ttu-id="5959e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5959e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5959e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5959e-110">Permission type</span></span>                        | <span data-ttu-id="5959e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5959e-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="5959e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5959e-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="5959e-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5959e-113">Group.ReadWrite.All</span></span>                         |
| <span data-ttu-id="5959e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5959e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5959e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5959e-115">Not supported.</span></span>                              |
| <span data-ttu-id="5959e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5959e-116">Application</span></span>                            | <span data-ttu-id="5959e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5959e-117">Not supported.</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="5959e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5959e-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
``` http
POST /planner/plans
```

## <a name="request-headers"></a><span data-ttu-id="5959e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5959e-119">Request headers</span></span>

| <span data-ttu-id="5959e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5959e-120">Name</span></span>          | <span data-ttu-id="5959e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5959e-121">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="5959e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5959e-122">Authorization</span></span> | <span data-ttu-id="5959e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5959e-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5959e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5959e-125">Request body</span></span>

<span data-ttu-id="5959e-p104">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerPlan](../resources/plannerplan.md). La propiedad de propietario **plannerPlan** se debe establecer en un identificador de un objeto [group](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="5959e-p104">In the request body, supply a JSON representation of [plannerPlan](../resources/plannerplan.md) object. The **plannerPlan** owner property must be set to an id of a [group](../resources/group.md) object.</span></span>

><span data-ttu-id="5959e-128">**Nota:** El usuario que está creando el plan debe ser miembro del grupo que será el propietario del plan.</span><span class="sxs-lookup"><span data-stu-id="5959e-128">**Note:** The user who is creating the plan must be a member of the group that will own the plan.</span></span> <span data-ttu-id="5959e-129">Cuando se crea un nuevo grupo mediante el uso de [Create group](../api/group-post-groups.md), no se agregan al grupo como un miembro.</span><span class="sxs-lookup"><span data-stu-id="5959e-129">When you create a new group by using [Create group](../api/group-post-groups.md), you are not added to the group as a member.</span></span> <span data-ttu-id="5959e-130">Una vez creado el grupo, agregarse como un miembro mediante el uso [grupo post (miembros)](../api/group-post-members.md).</span><span class="sxs-lookup"><span data-stu-id="5959e-130">After the group is created, add yourself as a member by using [group post members](../api/group-post-members.md).</span></span>

## <a name="response"></a><span data-ttu-id="5959e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5959e-131">Response</span></span>

<span data-ttu-id="5959e-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5959e-132">If successful, this method returns `201 Created` response code and [plannerPlan](../resources/plannerplan.md) object in the response body.</span></span>

<span data-ttu-id="5959e-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="5959e-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="5959e-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5959e-136">Example</span></span>

### <a name="request"></a><span data-ttu-id="5959e-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5959e-137">Request</span></span>

<span data-ttu-id="5959e-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5959e-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_plannerplan_from_planner"
}-->
``` http
POST https://graph.microsoft.com/beta/planner/plans
Content-type: application/json
Content-length: 381

{
  "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
  "title": "title-value"
}
```

<span data-ttu-id="5959e-139">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerPlan](../resources/plannerplan.md).</span><span class="sxs-lookup"><span data-stu-id="5959e-139">In the request body, supply a JSON representation of [plannerPlan](../resources/plannerplan.md) object.</span></span>

### <a name="response"></a><span data-ttu-id="5959e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5959e-140">Response</span></span>

<span data-ttu-id="5959e-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5959e-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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