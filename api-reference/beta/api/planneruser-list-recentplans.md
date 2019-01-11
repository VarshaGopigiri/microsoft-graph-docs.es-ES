---
title: Lista recentPlans
description: Recuperar una lista de plannerPlans visto recientemente por un usuario. Puede actualizar planes vistos recientemente mediante la actualización de los recursos de plannerUser.
author: TarkanSevilmis
localization_priority: Normal
ms.openlocfilehash: bfc2ffff15db55c289a95223ced6cb15af0535cc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884493"
---
# <a name="list-recentplans"></a><span data-ttu-id="a26c6-104">Lista recentPlans</span><span class="sxs-lookup"><span data-stu-id="a26c6-104">List recentPlans</span></span>

> <span data-ttu-id="a26c6-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a26c6-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a26c6-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a26c6-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a26c6-107">Recuperar una lista de [plannerPlans](../resources/plannerplan.md) visto recientemente por un usuario.</span><span class="sxs-lookup"><span data-stu-id="a26c6-107">Retrieve a list of [plannerPlans](../resources/plannerplan.md) recently viewed by a user.</span></span> <span data-ttu-id="a26c6-108">Puede actualizar planes vistos recientemente mediante la [actualización de los recursos de plannerUser](planneruser-update.md).</span><span class="sxs-lookup"><span data-stu-id="a26c6-108">You can update recently viewed plans by [updating the plannerUser resource](planneruser-update.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="a26c6-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="a26c6-109">Permissions</span></span>
<span data-ttu-id="a26c6-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a26c6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a26c6-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a26c6-112">Permission type</span></span>      | <span data-ttu-id="a26c6-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a26c6-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a26c6-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a26c6-114">Delegated (work or school account)</span></span> | <span data-ttu-id="a26c6-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a26c6-115">Group.Read.All</span></span>    |
|<span data-ttu-id="a26c6-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a26c6-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a26c6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a26c6-117">Not supported.</span></span>    |
|<span data-ttu-id="a26c6-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a26c6-118">Application</span></span> | <span data-ttu-id="a26c6-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a26c6-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a26c6-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a26c6-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/planner/recentPlans
GET /users/<id>/planner/recentPlans
```

## <a name="request-headers"></a><span data-ttu-id="a26c6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a26c6-121">Request headers</span></span>
| <span data-ttu-id="a26c6-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="a26c6-122">Name</span></span>      |<span data-ttu-id="a26c6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a26c6-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a26c6-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="a26c6-124">Authorization</span></span>  | <span data-ttu-id="a26c6-p105">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a26c6-p105">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a26c6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a26c6-127">Request body</span></span>
<span data-ttu-id="a26c6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a26c6-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="a26c6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a26c6-129">Response</span></span>
<span data-ttu-id="a26c6-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a26c6-130">If successful, this method returns a `200 OK` response code and a collection of [plannerPlan](../resources/plannerplan.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a26c6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a26c6-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a26c6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a26c6-132">Request</span></span>
<span data-ttu-id="a26c6-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a26c6-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_recentplans"
}-->
```http
GET https://graph.microsoft.com/beta/me/planner/recentPlans
```
##### <a name="response"></a><span data-ttu-id="a26c6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a26c6-134">Response</span></span>
<span data-ttu-id="a26c6-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a26c6-135">The following is an example of the response.</span></span> 

><span data-ttu-id="a26c6-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a26c6-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 979

{
  "value": [
    {
      "@odata.etag": "W/\"JzEtUGxhbiAgQEBAQEBAQEBAQEBAQEBDXCc=\"",
      "createdBy": {
        "user": {
          "id": "dd8a8379-1ac1-4eee-861d-ec15f6fa3611"
        },
        "application": {
          "id": "09abbdfd-ed23-44ee-a2d9-a627aa1c90f3"
        }
      },
      "createdDateTime": "2015-10-14T00:57:28.4698344Z",
      "owner": "eacd01dd-84cc-4c12-bd8a-9a33e5aeed11",
      "title": "Budget Planning (2016)",
      "id": "uZWtCtli30CGoWLIWSat1mQAC0ai"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List recentPlans",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
