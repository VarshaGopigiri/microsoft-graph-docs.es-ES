---
title: Lista decisiones de accessReview
description: En el anuncio de Azure access revisa la característica, recuperar las decisiones de un objeto accessReview.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 4f89fdbce1c87ce9ef8a6ba8c5b7f9b7be410617
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927012"
---
# <a name="list-accessreview-decisions"></a><span data-ttu-id="9862b-103">Lista decisiones de accessReview</span><span class="sxs-lookup"><span data-stu-id="9862b-103">List accessReview decisions</span></span>

> <span data-ttu-id="9862b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9862b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9862b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9862b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9862b-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, recuperar las decisiones de un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="9862b-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, retrieve the decisions of an [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="9862b-107">Tenga en cuenta que una revisión periódica de acceso no tendrá un `decisions` relación.</span><span class="sxs-lookup"><span data-stu-id="9862b-107">Note that a recurring access review will not have a `decisions` relationship.</span></span>  <span data-ttu-id="9862b-108">En su lugar, debe navegar el autor de la llamada la `instance` relación para buscar un `accessReview` objeto para una instancia actual o pasada de la revisión de access.</span><span class="sxs-lookup"><span data-stu-id="9862b-108">Instead, the caller must navigate the `instance` relationship to find an `accessReview` object for a current or past instance of the access review.</span></span>

## <a name="permissions"></a><span data-ttu-id="9862b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="9862b-109">Permissions</span></span>
<span data-ttu-id="9862b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9862b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9862b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9862b-112">Permission type</span></span>                        | <span data-ttu-id="9862b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9862b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="9862b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9862b-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="9862b-115">`AccessReview.Read.All`, `AccessReview.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="9862b-115"></span></span>  <span data-ttu-id="9862b-116">También debe ser el usuario iniciado en un rol de Active directory que le permita leer una revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="9862b-116">The signed in user must also be in a directory role which permits them to read an access review.</span></span> |
|<span data-ttu-id="9862b-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9862b-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9862b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9862b-118">Not supported.</span></span> |
|<span data-ttu-id="9862b-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9862b-119">Application</span></span>                            | <span data-ttu-id="9862b-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9862b-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9862b-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9862b-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')/decisions
```
## <a name="request-headers"></a><span data-ttu-id="9862b-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9862b-122">Request headers</span></span>
| <span data-ttu-id="9862b-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9862b-123">Name</span></span>         | <span data-ttu-id="9862b-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="9862b-124">Type</span></span>        | <span data-ttu-id="9862b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9862b-125">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="9862b-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="9862b-126">Authorization</span></span> | <span data-ttu-id="9862b-127">string</span><span class="sxs-lookup"><span data-stu-id="9862b-127">string</span></span> | <span data-ttu-id="9862b-128">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="9862b-128">Bearer \{token\}.</span></span> <span data-ttu-id="9862b-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9862b-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9862b-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9862b-130">Request body</span></span>
<span data-ttu-id="9862b-131">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9862b-131">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="9862b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9862b-132">Response</span></span>
<span data-ttu-id="9862b-133">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [accessReviewDecision](../resources/accessreviewdecision.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9862b-133">If successful, this method returns a `200, OK` response code and an array of [accessReviewDecision](../resources/accessreviewdecision.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9862b-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9862b-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9862b-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9862b-135">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_accessReview_decisions"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/decisions
```

##### <a name="response"></a><span data-ttu-id="9862b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9862b-136">Response</span></span>
><span data-ttu-id="9862b-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9862b-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="9862b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9862b-139">See also</span></span>

| <span data-ttu-id="9862b-140">Método</span><span class="sxs-lookup"><span data-stu-id="9862b-140">Method</span></span>           | <span data-ttu-id="9862b-141">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9862b-141">Return Type</span></span>    |<span data-ttu-id="9862b-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="9862b-142">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9862b-143">Obtener accessReview</span><span class="sxs-lookup"><span data-stu-id="9862b-143">Get accessReview</span></span>](accessreview-get.md) |  [<span data-ttu-id="9862b-144">accessReview</span><span class="sxs-lookup"><span data-stu-id="9862b-144">accessReview</span></span>](../resources/accessreview.md) |  <span data-ttu-id="9862b-145">Recuperar una revisión de access.</span><span class="sxs-lookup"><span data-stu-id="9862b-145">Retrieve an access review.</span></span> |
|[<span data-ttu-id="9862b-146">Mis decisiones accessReview de lista</span><span class="sxs-lookup"><span data-stu-id="9862b-146">List my accessReview decisions</span></span>](accessreview-listmydecisions.md) |        <span data-ttu-id="9862b-147">colección de [accessReviewDecision](../resources/accessreviewdecision.md)</span><span class="sxs-lookup"><span data-stu-id="9862b-147">[accessReviewDecision](../resources/accessreviewdecision.md) collection</span></span>|    <span data-ttu-id="9862b-148">Como revisor, obtener Mis decisiones de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="9862b-148">As a reviewer, get my decisions of an accessReview.</span></span>|
|[<span data-ttu-id="9862b-149">Enviar aviso de accessReview</span><span class="sxs-lookup"><span data-stu-id="9862b-149">Send accessReview reminder</span></span>](accessreview-sendreminder.md) |       <span data-ttu-id="9862b-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9862b-150">None.</span></span>   |   <span data-ttu-id="9862b-151">Enviar un aviso a los revisores de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="9862b-151">Send a reminder to the reviewers of an accessReview.</span></span> |
|[<span data-ttu-id="9862b-152">Detener accessReview</span><span class="sxs-lookup"><span data-stu-id="9862b-152">Stop accessReview</span></span>](accessreview-stop.md) |        <span data-ttu-id="9862b-153">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9862b-153">None.</span></span>   |   <span data-ttu-id="9862b-154">Detener una accessReview.</span><span class="sxs-lookup"><span data-stu-id="9862b-154">Stop an accessReview.</span></span> |
|[<span data-ttu-id="9862b-155">Restablecer las decisiones de accessReview</span><span class="sxs-lookup"><span data-stu-id="9862b-155">Reset accessReview decisions</span></span>](accessreview-reset.md) |        <span data-ttu-id="9862b-156">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9862b-156">None.</span></span>   |   <span data-ttu-id="9862b-157">Restablecer las decisiones en un accessReview en curso.</span><span class="sxs-lookup"><span data-stu-id="9862b-157">Reset the decisions in an in-progress accessReview.</span></span>|
|[<span data-ttu-id="9862b-158">Aplicar decisiones accessReview</span><span class="sxs-lookup"><span data-stu-id="9862b-158">Apply accessReview decisions</span></span>](accessreview-apply.md) |        <span data-ttu-id="9862b-159">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9862b-159">None.</span></span>   |   <span data-ttu-id="9862b-160">Se aplican las decisiones de un accessReview completado.</span><span class="sxs-lookup"><span data-stu-id="9862b-160">Apply the decisions from a completed accessReview.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview decisions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
