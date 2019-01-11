---
title: Obtener plannerUser
description: 'Recuperar las propiedades y relaciones de un objeto plannerUser. Las propiedades devueltas incluyen planes favoritos del usuario y planes de visto recientemente. '
localization_priority: Normal
ms.openlocfilehash: 1abffddb2ddbefdcd0aaeddedffe94ae8ad605d8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810643"
---
# <a name="get-planneruser"></a><span data-ttu-id="255ff-104">Obtener plannerUser</span><span class="sxs-lookup"><span data-stu-id="255ff-104">Get plannerUser</span></span>

> <span data-ttu-id="255ff-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="255ff-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="255ff-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="255ff-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="255ff-107">Recuperar las propiedades y relaciones de un objeto [plannerUser](../resources/planneruser.md) .</span><span class="sxs-lookup"><span data-stu-id="255ff-107">Retrieve the properties and relationships of a [plannerUser](../resources/planneruser.md) object.</span></span> <span data-ttu-id="255ff-108">Las propiedades devueltas incluyen planes favoritos del usuario y planes de visto recientemente.</span><span class="sxs-lookup"><span data-stu-id="255ff-108">The returned properties include the user's favorite plans and recently viewed plans.</span></span> 
## <a name="permissions"></a><span data-ttu-id="255ff-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="255ff-109">Permissions</span></span>
<span data-ttu-id="255ff-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="255ff-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="255ff-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="255ff-112">Permission type</span></span>      | <span data-ttu-id="255ff-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="255ff-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="255ff-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="255ff-114">Delegated (work or school account)</span></span> | <span data-ttu-id="255ff-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="255ff-115">Group.Read.All</span></span>    |
|<span data-ttu-id="255ff-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="255ff-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="255ff-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="255ff-117">Not supported.</span></span>    |
|<span data-ttu-id="255ff-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="255ff-118">Application</span></span> | <span data-ttu-id="255ff-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="255ff-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="255ff-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="255ff-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/planner
GET /users/<id>/planner
```

## <a name="request-headers"></a><span data-ttu-id="255ff-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="255ff-121">Request headers</span></span>
| <span data-ttu-id="255ff-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="255ff-122">Name</span></span>      |<span data-ttu-id="255ff-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="255ff-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="255ff-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="255ff-124">Authorization</span></span>  | <span data-ttu-id="255ff-p105">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="255ff-p105">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="255ff-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="255ff-127">Request body</span></span>
<span data-ttu-id="255ff-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="255ff-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="255ff-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="255ff-129">Response</span></span>
<span data-ttu-id="255ff-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [plannerUser](../resources/planneruser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="255ff-130">If successful, this method returns a `200 OK` response code and a [plannerUser](../resources/planneruser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="255ff-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="255ff-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="255ff-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="255ff-132">Request</span></span>
<span data-ttu-id="255ff-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="255ff-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_planneruser"
}-->
```http
GET https://graph.microsoft.com/beta/me/planner
```
##### <a name="response"></a><span data-ttu-id="255ff-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="255ff-134">Response</span></span>
<span data-ttu-id="255ff-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="255ff-135">The following is an example of the response.</span></span> 

><span data-ttu-id="255ff-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="255ff-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
