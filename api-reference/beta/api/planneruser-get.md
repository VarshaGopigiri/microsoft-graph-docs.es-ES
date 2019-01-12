---
title: Obtener plannerUser
description: 'Recuperar las propiedades y relaciones de un objeto plannerUser. Las propiedades devueltas incluyen planes favoritos del usuario y planes de visto recientemente. '
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 742d29d65c5d80db96c8cff199e25465f7a80dd7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915994"
---
# <a name="get-planneruser"></a><span data-ttu-id="31ddc-104">Obtener plannerUser</span><span class="sxs-lookup"><span data-stu-id="31ddc-104">Get plannerUser</span></span>

> <span data-ttu-id="31ddc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31ddc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31ddc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31ddc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="31ddc-107">Recuperar las propiedades y relaciones de un objeto [plannerUser](../resources/planneruser.md) .</span><span class="sxs-lookup"><span data-stu-id="31ddc-107">Retrieve the properties and relationships of a [plannerUser](../resources/planneruser.md) object.</span></span> <span data-ttu-id="31ddc-108">Las propiedades devueltas incluyen planes favoritos del usuario y planes de visto recientemente.</span><span class="sxs-lookup"><span data-stu-id="31ddc-108">The returned properties include the user's favorite plans and recently viewed plans.</span></span> 
## <a name="permissions"></a><span data-ttu-id="31ddc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="31ddc-109">Permissions</span></span>
<span data-ttu-id="31ddc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31ddc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="31ddc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31ddc-112">Permission type</span></span>      | <span data-ttu-id="31ddc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31ddc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="31ddc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31ddc-114">Delegated (work or school account)</span></span> | <span data-ttu-id="31ddc-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="31ddc-115">Group.Read.All</span></span>    |
|<span data-ttu-id="31ddc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31ddc-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="31ddc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31ddc-117">Not supported.</span></span>    |
|<span data-ttu-id="31ddc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31ddc-118">Application</span></span> | <span data-ttu-id="31ddc-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31ddc-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="31ddc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31ddc-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/planner
GET /users/<id>/planner
```

## <a name="request-headers"></a><span data-ttu-id="31ddc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31ddc-121">Request headers</span></span>
| <span data-ttu-id="31ddc-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="31ddc-122">Name</span></span>      |<span data-ttu-id="31ddc-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="31ddc-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="31ddc-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="31ddc-124">Authorization</span></span>  | <span data-ttu-id="31ddc-p105">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="31ddc-p105">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="31ddc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31ddc-127">Request body</span></span>
<span data-ttu-id="31ddc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="31ddc-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="31ddc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31ddc-129">Response</span></span>
<span data-ttu-id="31ddc-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [plannerUser](../resources/planneruser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31ddc-130">If successful, this method returns a `200 OK` response code and a [plannerUser](../resources/planneruser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="31ddc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31ddc-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="31ddc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31ddc-132">Request</span></span>
<span data-ttu-id="31ddc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31ddc-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_planneruser"
}-->
```http
GET https://graph.microsoft.com/beta/me/planner
```
##### <a name="response"></a><span data-ttu-id="31ddc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31ddc-134">Response</span></span>
<span data-ttu-id="31ddc-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31ddc-135">The following is an example of the response.</span></span> 

><span data-ttu-id="31ddc-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31ddc-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerUser"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 979

{
  "favoritePlanReferences": {
    "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
      "@odata.type": "#microsoft.graph.plannerFavoritePlanReference",
      "orderHint": "8586866870001551087",
      "planTitle": "Next Release Discussion"
    },
    "uZWtCtli30CGoWLIWSat1mQAC0ai": {
      "@odata.type": "#microsoft.graph.plannerFavoritePlanReference",
      "orderHint": "8586888705198093378",
      "planTitle": "Product Support"
    }
  },
  "recentPlanReferences": {
    "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
      "@odata.type": "#microsoft.graph.plannerRecentPlanReference",
      "lastAccessedDateTime": "2018-01-02T22:49:46.155Z",
      "planTitle": "Next Release Discussion"
    },
    "XYE5pqNJu0uuRC2PM4ZQrmQAF2Pn": {
      "@odata.type": "#microsoft.graph.plannerRecentPlanReference",
      "lastAccessedDateTime": "2018-01-01T19:39:17.57Z",
      "planTitle": "Success Metrics"
    }
  },
  "id": "-YPnMJRiIUSKFyaVjYEkBWQAAc47"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
