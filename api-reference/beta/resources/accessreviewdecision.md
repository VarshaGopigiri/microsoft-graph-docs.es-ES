---
title: tipo de recurso accessReviewDecision
description: En el anuncio de Azure access revisa la característica, el `accessReviewDecision` representa una decisión de revisión de Azure AD acceso de acceso de una entidad determinada.  Dentro de una revisión de access, o una instancia de una revisión periódica de acceso, hay una `accessReviewDecision` por usuario revisado.  Por ejemplo, si un grupo tiene dos invitados y que no sean uno Invitado como miembros y una revisión de acceso de los invitados se realiza para dicho grupo, a continuación, habrá dos objetos de toma de decisiones de revisión de access.  Si un revisor cambia su decisión o reemplaza a otro revisor, entonces el `accessReviewDecision` se ha actualizado.
localization_priority: Normal
ms.openlocfilehash: 208337f3427fad65499b400dee769d379c38dcb8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870052"
---
# <a name="accessreviewdecision-resource-type"></a><span data-ttu-id="e28a1-106">tipo de recurso accessReviewDecision</span><span class="sxs-lookup"><span data-stu-id="e28a1-106">accessReviewDecision resource type</span></span>

> <span data-ttu-id="e28a1-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e28a1-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e28a1-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e28a1-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e28a1-109">En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el `accessReviewDecision` representa una decisión de revisión de Azure AD acceso de acceso de una entidad determinada.</span><span class="sxs-lookup"><span data-stu-id="e28a1-109">In the Azure AD [access reviews](accessreviews-root.md) feature, the `accessReviewDecision` represents an Azure AD access review decision of a particular entity's access.</span></span>  <span data-ttu-id="e28a1-110">Dentro de una revisión de access, o una instancia de una revisión periódica de acceso, hay una `accessReviewDecision` por usuario revisado.</span><span class="sxs-lookup"><span data-stu-id="e28a1-110">Within an access review, or an instance of a recurring access review, there is one `accessReviewDecision` per reviewed user.</span></span>  <span data-ttu-id="e28a1-111">Por ejemplo, si un grupo tiene dos invitados y que no sean uno Invitado como miembros y una revisión de acceso de los invitados se realiza para dicho grupo, a continuación, habrá dos objetos de toma de decisiones de revisión de access.</span><span class="sxs-lookup"><span data-stu-id="e28a1-111">For example, if a group has two guests and one non-guest as members, and an access review of guests is performed for that group, then there will be two access review decision objects.</span></span>  <span data-ttu-id="e28a1-112">Si un revisor cambia su decisión o reemplaza a otro revisor, entonces el `accessReviewDecision` se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="e28a1-112">If a reviewer changes their decision, or another reviewer overrides them, then the `accessReviewDecision` is updated.</span></span>


## <a name="methods"></a><span data-ttu-id="e28a1-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="e28a1-113">Methods</span></span>

<span data-ttu-id="e28a1-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e28a1-114">None.</span></span>  <span data-ttu-id="e28a1-115">Objetos de este tipo se crean automáticamente por la característica cuando revise Inicializa un acceso y no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="e28a1-115">Objects of this type are automatically created by the feature when an access review initializes, and cannot be deleted.</span></span>  <span data-ttu-id="e28a1-116">Se pueden recuperar desde una revisión de access con las relaciones de [las decisiones](../api/accessreview-listdecisions.md) y [mydecisions](../api/accessreview-listmydecisions.md) .</span><span class="sxs-lookup"><span data-stu-id="e28a1-116">They can be retrieved from an access review using the [decisions](../api/accessreview-listdecisions.md) and [mydecisions](../api/accessreview-listmydecisions.md) relationships.</span></span>

## <a name="properties"></a><span data-ttu-id="e28a1-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e28a1-117">Properties</span></span>

<span data-ttu-id="e28a1-118">Esta tabla muestra las propiedades de objetos de este tipo de bases.</span><span class="sxs-lookup"><span data-stu-id="e28a1-118">This table illustrates the base properties of objects of this type.</span></span> 

| <span data-ttu-id="e28a1-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e28a1-119">Property</span></span>                        | <span data-ttu-id="e28a1-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="e28a1-120">Type</span></span>                         | <span data-ttu-id="e28a1-121">Description</span><span class="sxs-lookup"><span data-stu-id="e28a1-121">Description</span></span>                                                                                            |
| :------------------------------ | :-----------------------     | :----------------------------------------------------------------------------------------------------- |
| `id`                            |`String`                      | <span data-ttu-id="e28a1-122">El identificador de la decisión dentro de la revisión de access.</span><span class="sxs-lookup"><span data-stu-id="e28a1-122">The id of the decision within the access review.</span></span>                                                                                     |
| `accessReviewId`                |`String`                      | <span data-ttu-id="e28a1-123">El identificador generado por la característica de la revisión de access.</span><span class="sxs-lookup"><span data-stu-id="e28a1-123">The feature-generated id of the access review.</span></span>                                                                                       |
| `reviewedBy`                    |[<span data-ttu-id="e28a1-124">IdentidadDeUsuario</span><span class="sxs-lookup"><span data-stu-id="e28a1-124">userIdentity</span></span>](useridentity.md)| <span data-ttu-id="e28a1-125">La identidad del revisor.</span><span class="sxs-lookup"><span data-stu-id="e28a1-125">The identity of the reviewer.</span></span>                                                                                       |
| `reviewedDate`                  |`DateTimeOffset`              | <span data-ttu-id="e28a1-126">Se ha proporcionado la fecha y hora de la revisión más reciente de este derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="e28a1-126">The date and time the most recent review for this access right was supplied.</span></span>                                                                         |
| `reviewResult`                  |`String`                      | <span data-ttu-id="e28a1-127">El resultado de la revisión.</span><span class="sxs-lookup"><span data-stu-id="e28a1-127">The result of the review.</span></span>                                                                                    |
| `justification`                 |`String`                      | <span data-ttu-id="e28a1-128">Justificación del negocio del revisor, si proporciona.</span><span class="sxs-lookup"><span data-stu-id="e28a1-128">The reviewer's business justification, if supplied.</span></span>                                                                         |
| `appliedBy`                     |[<span data-ttu-id="e28a1-129">IdentidadDeUsuario</span><span class="sxs-lookup"><span data-stu-id="e28a1-129">userIdentity</span></span>](useridentity.md)| <span data-ttu-id="e28a1-130">Cuando se completa la revisión, si los resultados se han aplicado manualmente, la identidad de usuario del usuario que se aplica la decisión.</span><span class="sxs-lookup"><span data-stu-id="e28a1-130">When the review completes, if the results were manually applied, the user identity of the user who applied the decision.</span></span>                                                           |
| `appliedDateTime`               |`DateTimeOffset`              | <span data-ttu-id="e28a1-131">La fecha y la hora cuando se aplicó la decisión de revisión.</span><span class="sxs-lookup"><span data-stu-id="e28a1-131">The date and time when the review decision was applied.</span></span>                                                          |
| `applyResult`                   |`String`                      | <span data-ttu-id="e28a1-132">El resultado de la aplicación de la decisión, uno de `NotApplied`, `Success`, `Failed`, `NotFound` o `NotSupported`.</span><span class="sxs-lookup"><span data-stu-id="e28a1-132">The outcome of applying the decision, one of `NotApplied`, `Success`, `Failed`, `NotFound` or `NotSupported`.</span></span>                      |
| `accessRecommendation`          |`String`                      | <span data-ttu-id="e28a1-133">La recomendación de característica-generado se muestra para el revisor, uno de `Approve`, `Deny` o `NotAvailable`.</span><span class="sxs-lookup"><span data-stu-id="e28a1-133">The feature- generated recommendation shown to the reviewer, one of `Approve`, `Deny` or `NotAvailable`.</span></span> |


<span data-ttu-id="e28a1-134">Además, las propiedades adicionales pueden estar presentes según el tipo de objeto del objeto que poseen el acceso a la que se ha decidido.</span><span class="sxs-lookup"><span data-stu-id="e28a1-134">In addition, additional properties may be present depending on the object type of the object possessing the access that was decided upon.</span></span>  <span data-ttu-id="e28a1-135">Por ejemplo, si la decisión de revisión de acceso es la pertenencia a grupos de un usuario en particular o acceso a la aplicación, el usuario que potencialmente se va a tener su acceso se ha quitado se identifica a través de estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="e28a1-135">For example, if the access review decision is a particular user's group membership or application access, the user who is potentially going to have their access be removed is identified through these properties:</span></span>

| <span data-ttu-id="e28a1-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e28a1-136">Property</span></span>                        | <span data-ttu-id="e28a1-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="e28a1-137">Type</span></span>                         | <span data-ttu-id="e28a1-138">Description</span><span class="sxs-lookup"><span data-stu-id="e28a1-138">Description</span></span>                                                                                            |
| :------------------------------ | :-----------------------     | :----------------------------------------------------------------------------------------------------- |
| `userId`                            |`String`                      | <span data-ttu-id="e28a1-139">El identificador de usuario cuyo acceso se ha revisado.</span><span class="sxs-lookup"><span data-stu-id="e28a1-139">The id of user whose access was reviewed.</span></span>                                                                                    |
| `userDisplayName`                            |`String`                      | <span data-ttu-id="e28a1-140">El nombre para mostrar del usuario cuyo acceso se ha revisado.</span><span class="sxs-lookup"><span data-stu-id="e28a1-140">The display name of the user whose access was reviewed.</span></span>                                                                                     |
| `userPrincipalName`                            |`String`                      | <span data-ttu-id="e28a1-141">El nombre principal de usuario del usuario cuyo acceso se ha revisado.</span><span class="sxs-lookup"><span data-stu-id="e28a1-141">The user principal name of the user whose access was reviewed.</span></span>                                                                                     |



## <a name="relationships"></a><span data-ttu-id="e28a1-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e28a1-142">Relationships</span></span>

<span data-ttu-id="e28a1-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e28a1-143">None.</span></span>  <span data-ttu-id="e28a1-144">Objetos de este tipo se pueden recuperar desde una revisión de access con las relaciones de [las decisiones](../api/accessreview-listdecisions.md) y [mydecisions](../api/accessreview-listmydecisions.md) del objeto [accessReview](accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="e28a1-144">Objects of this type can be retrieved from an access review using the [decisions](../api/accessreview-listdecisions.md) and [mydecisions](../api/accessreview-listmydecisions.md) relationships of the [accessReview](accessreview.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="e28a1-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="e28a1-145">See also</span></span>

| <span data-ttu-id="e28a1-146">Método</span><span class="sxs-lookup"><span data-stu-id="e28a1-146">Method</span></span>           | <span data-ttu-id="e28a1-147">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e28a1-147">Return Type</span></span>    |<span data-ttu-id="e28a1-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="e28a1-148">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e28a1-149">Lista decisiones de accessReview</span><span class="sxs-lookup"><span data-stu-id="e28a1-149">List accessReview decisions</span></span>](../api/accessreview-listdecisions.md) |      <span data-ttu-id="e28a1-150">colección de [accessReviewDecision](accessreviewdecision.md)</span><span class="sxs-lookup"><span data-stu-id="e28a1-150">[accessReviewDecision](accessreviewdecision.md) collection</span></span>| <span data-ttu-id="e28a1-151">Obtenga las decisiones de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="e28a1-151">Get the decisions of an accessReview.</span></span>|
|[<span data-ttu-id="e28a1-152">Mis decisiones accessReview de lista</span><span class="sxs-lookup"><span data-stu-id="e28a1-152">List my accessReview decisions</span></span>](../api/accessreview-listmydecisions.md) |     <span data-ttu-id="e28a1-153">colección de [accessReviewDecision](accessreviewdecision.md)</span><span class="sxs-lookup"><span data-stu-id="e28a1-153">[accessReviewDecision](accessreviewdecision.md) collection</span></span>| <span data-ttu-id="e28a1-154">Como revisor, obtener Mis decisiones de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="e28a1-154">As a reviewer, get my decisions of an accessReview.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e28a1-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e28a1-155">JSON representation</span></span>

<span data-ttu-id="e28a1-156">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e28a1-156">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessReviewDecision"
}-->

```json
{
"id": "string (identifier)",
"accessReviewId": "string (identifier)",
"reviewedBy": "microsoft.graph.userIdentity",
"reviewedDate": "string (timestamp)",
"reviewResult": "string",
"justification": "string",
"appliedBy": "microsoft.graph.userIdentity",
"appliedDateTime": "string (timestamp)",
"applyResult": "string",
"accessRecommendation": "string",
"userId": "string",
"userDisplayName": "string",
"userPrincipalName": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "accessReviewDecision resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
