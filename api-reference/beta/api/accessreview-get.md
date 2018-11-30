---
title: Obtener accessReview
description: 'En el anuncio de Azure access revisa la característica, recuperar un objeto accessReview.  '
ms.openlocfilehash: ecd802613e6ab36816800197c00595c90426fb2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084670"
---
# <a name="get-accessreview"></a><span data-ttu-id="dd8fa-103">Obtener accessReview</span><span class="sxs-lookup"><span data-stu-id="dd8fa-103">Get accessReview</span></span>

> <span data-ttu-id="dd8fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dd8fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dd8fa-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, recuperar un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="dd8fa-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, retrieve an [accessReview](../resources/accessreview.md) object.</span></span>  

<span data-ttu-id="dd8fa-107">Para recuperar los revisores de la revisión de access, utilice la [lista de revisores accessReview](accessreview-listreviewers.md) API.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-107">To retrieve the reviewers of the access review, use the [list accessReview reviewers](accessreview-listreviewers.md) API.</span></span> <span data-ttu-id="dd8fa-108">Para recuperar las decisiones de la revisión de access, utilice la API de [decisiones de accessReview de lista](accessreview-listdecisions.md) o la API de [Mis decisiones accessReview de lista](accessreview-listmydecisions.md) .</span><span class="sxs-lookup"><span data-stu-id="dd8fa-108">To retrieve the decisions of the access review, use the [list accessReview decisions](accessreview-listdecisions.md) API, or the [list my accessReview decisions](accessreview-listmydecisions.md) API.</span></span>

<span data-ttu-id="dd8fa-109">Si se trata de una revisión periódica de acceso, a continuación, use la `instances` relación para recuperar una colección de [accessReview](../resources/accessreview.md) de los últimos, instancias actuales y futuros de la revisión de access.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-109">If this is a recurring access review, then use the `instances` relationship to retrieve an [accessReview](../resources/accessreview.md) collection of the past, current and future instances of the access review.</span></span>

## <a name="permissions"></a><span data-ttu-id="dd8fa-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd8fa-110">Permissions</span></span>
<span data-ttu-id="dd8fa-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dd8fa-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dd8fa-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd8fa-113">Permission type</span></span>                        | <span data-ttu-id="dd8fa-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd8fa-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd8fa-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd8fa-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="dd8fa-116">`AccessReview.Read.All`, `AccessReview.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-116"></span></span>  <span data-ttu-id="dd8fa-117">También debe ser el usuario iniciado en un rol de Active directory que le permita leer una revisión de acceso o asignado como un revisor de la revisión de access.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-117">The signed in user must also be in a directory role which permits them to read an access review, or assigned as a reviewer on the access review.</span></span> |
|<span data-ttu-id="dd8fa-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd8fa-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd8fa-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-119">Not supported.</span></span> |
|<span data-ttu-id="dd8fa-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd8fa-120">Application</span></span>                            | <span data-ttu-id="dd8fa-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dd8fa-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd8fa-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')
```
## <a name="request-headers"></a><span data-ttu-id="dd8fa-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd8fa-123">Request headers</span></span>
| <span data-ttu-id="dd8fa-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd8fa-124">Name</span></span>         | <span data-ttu-id="dd8fa-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd8fa-125">Type</span></span>        | <span data-ttu-id="dd8fa-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd8fa-126">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="dd8fa-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="dd8fa-127">Authorization</span></span> | <span data-ttu-id="dd8fa-128">string</span><span class="sxs-lookup"><span data-stu-id="dd8fa-128">string</span></span> | <span data-ttu-id="dd8fa-129">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-129">Bearer \{token\}.</span></span> <span data-ttu-id="dd8fa-130">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-130">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dd8fa-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dd8fa-131">Request body</span></span>
<span data-ttu-id="dd8fa-132">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-132">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="dd8fa-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd8fa-133">Response</span></span>
<span data-ttu-id="dd8fa-134">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y un objeto [accessReview](../resources/accessreview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-134">If successful, this method returns a `200, OK` response code and an [accessReview](../resources/accessreview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dd8fa-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd8fa-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dd8fa-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd8fa-136">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_accessReview"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')
```

##### <a name="response"></a><span data-ttu-id="dd8fa-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd8fa-137">Response</span></span>
><span data-ttu-id="dd8fa-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview",
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
    "displayName": "review",
    "startDateTime": "2017-11-14T01:14:54.89Z",
    "endDateTime": "2017-12-14T01:14:54.89Z",
    "status": "InProgress",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "reviewerType": "self",
    "description": "",
    "settings": {
        "reviewId": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
        "mailNotificationsEnabled": true,
        "remindersEnabled": true,
        "justificationRequiredOnApproval": true,
        "recurrenceSettings": {
            "recurrenceType": "onetime",
            "recurrenceEndType": "endBy",
            "durationInDays": 0,
            "recurrenceCount": 0
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dd8fa-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd8fa-140">See also</span></span>

| <span data-ttu-id="dd8fa-141">Método</span><span class="sxs-lookup"><span data-stu-id="dd8fa-141">Method</span></span>           | <span data-ttu-id="dd8fa-142">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd8fa-142">Return Type</span></span>    |<span data-ttu-id="dd8fa-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd8fa-143">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="dd8fa-144">Crear accessReview</span><span class="sxs-lookup"><span data-stu-id="dd8fa-144">Create accessReview</span></span>](accessreview-create.md) |    [<span data-ttu-id="dd8fa-145">accessReview</span><span class="sxs-lookup"><span data-stu-id="dd8fa-145">accessReview</span></span>](../resources/accessreview.md) |  <span data-ttu-id="dd8fa-146">Crear un nuevo accessReview.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-146">Create a new accessReview.</span></span> |
|[<span data-ttu-id="dd8fa-147">Lista programControls</span><span class="sxs-lookup"><span data-stu-id="dd8fa-147">List programControls</span></span>](programcontrol-list.md) | <span data-ttu-id="dd8fa-148">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="dd8fa-148">[programControl](../resources/programcontrol.md) collection</span></span> | <span data-ttu-id="dd8fa-149">ProgramControls de lista en un inquilino.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-149">List programControls in a tenant.</span></span> |
|[<span data-ttu-id="dd8fa-150">Revisores accessReview de lista</span><span class="sxs-lookup"><span data-stu-id="dd8fa-150">List accessReview reviewers</span></span>](accessreview-listreviewers.md) |     <span data-ttu-id="dd8fa-151">colección de [IdentidadDeUsuario](../resources/useridentity.md)</span><span class="sxs-lookup"><span data-stu-id="dd8fa-151">[userIdentity](../resources/useridentity.md) collection</span></span>|    <span data-ttu-id="dd8fa-152">Obtenga los revisores de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-152">Get the reviewers of an accessReview.</span></span> |
|[<span data-ttu-id="dd8fa-153">Lista decisiones de accessReview</span><span class="sxs-lookup"><span data-stu-id="dd8fa-153">List accessReview decisions</span></span>](accessreview-listdecisions.md) |     <span data-ttu-id="dd8fa-154">colección de [accessReviewDecision](../resources/accessreviewdecision.md)</span><span class="sxs-lookup"><span data-stu-id="dd8fa-154">[accessReviewDecision](../resources/accessreviewdecision.md) collection</span></span>|    <span data-ttu-id="dd8fa-155">Obtenga las decisiones de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-155">Get the decisions of an accessReview.</span></span>|
|[<span data-ttu-id="dd8fa-156">Mis decisiones accessReview de lista</span><span class="sxs-lookup"><span data-stu-id="dd8fa-156">List my accessReview decisions</span></span>](accessreview-listmydecisions.md) |        <span data-ttu-id="dd8fa-157">colección de [accessReviewDecision](../resources/accessreviewdecision.md)</span><span class="sxs-lookup"><span data-stu-id="dd8fa-157">[accessReviewDecision](../resources/accessreviewdecision.md) collection</span></span>|    <span data-ttu-id="dd8fa-158">Como revisor, obtener Mis decisiones de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="dd8fa-158">As a reviewer, get my decisions of an accessReview.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->