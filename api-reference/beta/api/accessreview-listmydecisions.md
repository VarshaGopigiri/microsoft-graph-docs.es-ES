---
title: Mis decisiones accessReview de lista
description: En la característica de revisiones de access Azure AD, recuperar las decisiones de un objeto accessReview para el usuario que realiza la llamada como revisor.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 037b916bca45c74d1918b45e4e9e21b685bd8ae0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941502"
---
# <a name="list-my-accessreview-decisions"></a><span data-ttu-id="0cc6b-103">Mis decisiones accessReview de lista</span><span class="sxs-lookup"><span data-stu-id="0cc6b-103">List my accessReview decisions</span></span>

> <span data-ttu-id="0cc6b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0cc6b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0cc6b-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, recuperar las decisiones de un objeto [accessReview](../resources/accessreview.md) para el usuario que realiza la llamada como revisor.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, retrieve the decisions of an [accessReview](../resources/accessreview.md) object for the calling user as reviewer.</span></span>
## <a name="permissions"></a><span data-ttu-id="0cc6b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0cc6b-107">Permissions</span></span>
<span data-ttu-id="0cc6b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0cc6b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0cc6b-110">Permission type</span></span>                        | <span data-ttu-id="0cc6b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0cc6b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="0cc6b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0cc6b-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="0cc6b-113">`AccessReview.Read.All`, `AccessReview.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-113"></span></span>  <span data-ttu-id="0cc6b-114">El usuario iniciado también debe tener permiso para leer esta revisión de acceso determinado.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-114">The signed in user must also be permitted to read this particular access review.</span></span> |
|<span data-ttu-id="0cc6b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0cc6b-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0cc6b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-116">Not supported.</span></span> |
|<span data-ttu-id="0cc6b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0cc6b-117">Application</span></span>                            | <span data-ttu-id="0cc6b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0cc6b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0cc6b-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')/myDecisions
```
## <a name="request-headers"></a><span data-ttu-id="0cc6b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0cc6b-120">Request headers</span></span>
| <span data-ttu-id="0cc6b-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="0cc6b-121">Name</span></span>         | <span data-ttu-id="0cc6b-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cc6b-122">Type</span></span>        | <span data-ttu-id="0cc6b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cc6b-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="0cc6b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="0cc6b-124">Authorization</span></span> | <span data-ttu-id="0cc6b-125">string</span><span class="sxs-lookup"><span data-stu-id="0cc6b-125">string</span></span> | <span data-ttu-id="0cc6b-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-126">Bearer \{token\}.</span></span> <span data-ttu-id="0cc6b-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0cc6b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0cc6b-128">Request body</span></span>
<span data-ttu-id="0cc6b-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="0cc6b-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cc6b-130">Response</span></span>
<span data-ttu-id="0cc6b-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [accessReviewDecision](../resources/accessreviewdecision.md) en el cuerpo de la respuesta, para que el usuario realiza la llamada es un revisor asignado.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-131">If successful, this method returns a `200, OK` response code and an array of [accessReviewDecision](../resources/accessreviewdecision.md) objects in the response body, for which the calling user is an assigned reviewer.</span></span>

## <a name="example"></a><span data-ttu-id="0cc6b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0cc6b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0cc6b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0cc6b-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_accessReview_decisions"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/myDecisions
```

##### <a name="response"></a><span data-ttu-id="0cc6b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cc6b-134">Response</span></span>
><span data-ttu-id="0cc6b-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReviewDecision",
  "isCollection": "true"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value":[
    {
            "id": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
            "accessReviewId": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
            "reviewResult": "Approve",
            "userPrincipalName": "alice@litware.com",
            "userId": "Alice Smith"
    }
    ]
}
```

## <a name="see-also"></a><span data-ttu-id="0cc6b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cc6b-137">See also</span></span>

| <span data-ttu-id="0cc6b-138">Método</span><span class="sxs-lookup"><span data-stu-id="0cc6b-138">Method</span></span>           | <span data-ttu-id="0cc6b-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cc6b-139">Return Type</span></span>    |<span data-ttu-id="0cc6b-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cc6b-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0cc6b-141">Obtener accessReview</span><span class="sxs-lookup"><span data-stu-id="0cc6b-141">Get accessReview</span></span>](accessreview-get.md) |  [<span data-ttu-id="0cc6b-142">accessReview</span><span class="sxs-lookup"><span data-stu-id="0cc6b-142">accessReview</span></span>](../resources/accessreview.md) |  <span data-ttu-id="0cc6b-143">Recuperar una revisión de access.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-143">Retrieve an access review.</span></span> |
|[<span data-ttu-id="0cc6b-144">Lista decisiones de accessReview</span><span class="sxs-lookup"><span data-stu-id="0cc6b-144">List accessReview decisions</span></span>](accessreview-listdecisions.md) |     <span data-ttu-id="0cc6b-145">colección de [accessReviewDecision](../resources/accessreviewdecision.md)</span><span class="sxs-lookup"><span data-stu-id="0cc6b-145">[accessReviewDecision](../resources/accessreviewdecision.md) collection</span></span>|    <span data-ttu-id="0cc6b-146">Recuperar todas las decisiones de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-146">Retrieve all the decisions of an accessReview.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview decisions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
