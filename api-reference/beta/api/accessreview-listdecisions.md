---
title: Lista decisiones de accessReview
description: En el anuncio de Azure access revisa la característica, recuperar las decisiones de un objeto accessReview.
ms.openlocfilehash: d8cf89706f053dfee6e98cdf23d2539874ac6997
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084353"
---
# <a name="list-accessreview-decisions"></a><span data-ttu-id="a70e5-103">Lista decisiones de accessReview</span><span class="sxs-lookup"><span data-stu-id="a70e5-103">List accessReview decisions</span></span>

> <span data-ttu-id="a70e5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a70e5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a70e5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a70e5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a70e5-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, recuperar las decisiones de un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a70e5-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, retrieve the decisions of an [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="a70e5-107">Tenga en cuenta que una revisión periódica de acceso no tendrá un `decisions` relación.</span><span class="sxs-lookup"><span data-stu-id="a70e5-107">Note that a recurring access review will not have a `decisions` relationship.</span></span>  <span data-ttu-id="a70e5-108">En su lugar, debe navegar el autor de la llamada la `instance` relación para buscar un `accessReview` objeto para una instancia actual o pasada de la revisión de access.</span><span class="sxs-lookup"><span data-stu-id="a70e5-108">Instead, the caller must navigate the `instance` relationship to find an `accessReview` object for a current or past instance of the access review.</span></span>

## <a name="permissions"></a><span data-ttu-id="a70e5-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="a70e5-109">Permissions</span></span>
<span data-ttu-id="a70e5-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a70e5-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a70e5-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a70e5-112">Permission type</span></span>                        | <span data-ttu-id="a70e5-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a70e5-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="a70e5-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a70e5-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="a70e5-115">`AccessReview.Read.All`, `AccessReview.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="a70e5-115"></span></span>  <span data-ttu-id="a70e5-116">También debe ser el usuario iniciado en un rol de Active directory que le permita leer una revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="a70e5-116">The signed in user must also be in a directory role which permits them to read an access review.</span></span> |
|<span data-ttu-id="a70e5-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a70e5-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a70e5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a70e5-118">Not supported.</span></span> |
|<span data-ttu-id="a70e5-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a70e5-119">Application</span></span>                            | <span data-ttu-id="a70e5-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a70e5-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a70e5-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a70e5-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')/decisions
```
## <a name="request-headers"></a><span data-ttu-id="a70e5-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a70e5-122">Request headers</span></span>
| <span data-ttu-id="a70e5-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="a70e5-123">Name</span></span>         | <span data-ttu-id="a70e5-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="a70e5-124">Type</span></span>        | <span data-ttu-id="a70e5-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70e5-125">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="a70e5-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="a70e5-126">Authorization</span></span> | <span data-ttu-id="a70e5-127">string</span><span class="sxs-lookup"><span data-stu-id="a70e5-127">string</span></span> | <span data-ttu-id="a70e5-128">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="a70e5-128">Bearer \{token\}.</span></span> <span data-ttu-id="a70e5-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a70e5-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a70e5-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a70e5-130">Request body</span></span>
<span data-ttu-id="a70e5-131">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a70e5-131">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="a70e5-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a70e5-132">Response</span></span>
<span data-ttu-id="a70e5-133">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [accessReviewDecision](../resources/accessreviewdecision.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a70e5-133">If successful, this method returns a `200, OK` response code and an array of [accessReviewDecision](../resources/accessreviewdecision.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a70e5-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a70e5-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a70e5-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a70e5-135">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_accessReview_decisions"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/decisions
```

##### <a name="response"></a><span data-ttu-id="a70e5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a70e5-136">Response</span></span>
><span data-ttu-id="a70e5-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a70e5-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="a70e5-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a70e5-139">See also</span></span>

| <span data-ttu-id="a70e5-140">Método</span><span class="sxs-lookup"><span data-stu-id="a70e5-140">Method</span></span>           | <span data-ttu-id="a70e5-141">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a70e5-141">Return Type</span></span>    |<span data-ttu-id="a70e5-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70e5-142">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a70e5-143">Obtener accessReview</span><span class="sxs-lookup"><span data-stu-id="a70e5-143">Get accessReview</span></span>](accessreview-get.md) |  [<span data-ttu-id="a70e5-144">accessReview</span><span class="sxs-lookup"><span data-stu-id="a70e5-144">accessReview</span></span>](../resources/accessreview.md) |  <span data-ttu-id="a70e5-145">Recuperar una revisión de access.</span><span class="sxs-lookup"><span data-stu-id="a70e5-145">Retrieve an access review.</span></span> |
|[<span data-ttu-id="a70e5-146">Mis decisiones accessReview de lista</span><span class="sxs-lookup"><span data-stu-id="a70e5-146">List my accessReview decisions</span></span>](accessreview-listmydecisions.md) |        <span data-ttu-id="a70e5-147">colección de [accessReviewDecision](../resources/accessreviewdecision.md)</span><span class="sxs-lookup"><span data-stu-id="a70e5-147">[accessReviewDecision](../resources/accessreviewdecision.md) collection</span></span>|    <span data-ttu-id="a70e5-148">Como revisor, obtener Mis decisiones de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="a70e5-148">As a reviewer, get my decisions of an accessReview.</span></span>|
|[<span data-ttu-id="a70e5-149">Enviar aviso de accessReview</span><span class="sxs-lookup"><span data-stu-id="a70e5-149">Send accessReview reminder</span></span>](accessreview-sendreminder.md) |       <span data-ttu-id="a70e5-150">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a70e5-150">None.</span></span>   |   <span data-ttu-id="a70e5-151">Enviar un aviso a los revisores de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="a70e5-151">Send a reminder to the reviewers of an accessReview.</span></span> |
|[<span data-ttu-id="a70e5-152">Detener accessReview</span><span class="sxs-lookup"><span data-stu-id="a70e5-152">Stop accessReview</span></span>](accessreview-stop.md) |        <span data-ttu-id="a70e5-153">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a70e5-153">None.</span></span>   |   <span data-ttu-id="a70e5-154">Detener una accessReview.</span><span class="sxs-lookup"><span data-stu-id="a70e5-154">Stop an accessReview.</span></span> |
|[<span data-ttu-id="a70e5-155">Restablecer las decisiones de accessReview</span><span class="sxs-lookup"><span data-stu-id="a70e5-155">Reset accessReview decisions</span></span>](accessreview-reset.md) |        <span data-ttu-id="a70e5-156">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a70e5-156">None.</span></span>   |   <span data-ttu-id="a70e5-157">Restablecer las decisiones en un accessReview en curso.</span><span class="sxs-lookup"><span data-stu-id="a70e5-157">Reset the decisions in an in-progress accessReview.</span></span>|
|[<span data-ttu-id="a70e5-158">Aplicar decisiones accessReview</span><span class="sxs-lookup"><span data-stu-id="a70e5-158">Apply accessReview decisions</span></span>](accessreview-apply.md) |        <span data-ttu-id="a70e5-159">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a70e5-159">None.</span></span>   |   <span data-ttu-id="a70e5-160">Se aplican las decisiones de un accessReview completado.</span><span class="sxs-lookup"><span data-stu-id="a70e5-160">Apply the decisions from a completed accessReview.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview decisions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
