---
title: Actualizar accessReview
description: En la característica de revisiones de access Azure AD, actualice un objeto accessReview existente para cambiar una o varias de sus propiedades.
ms.openlocfilehash: 8913377db8acea17023605f85d01c8c9ecea419b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084365"
---
# <a name="update-accessreview"></a><span data-ttu-id="d122d-103">Actualizar accessReview</span><span class="sxs-lookup"><span data-stu-id="d122d-103">Update accessReview</span></span>

> <span data-ttu-id="d122d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d122d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d122d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d122d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d122d-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, actualice un objeto [accessReview](../resources/accessreview.md) existente para cambiar una o varias de sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="d122d-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, update an existing [accessReview](../resources/accessreview.md) object to change one or more of its properties.</span></span>

<span data-ttu-id="d122d-107">Esta API no está pensada para cambiar los revisores o las decisiones de una revisión.</span><span class="sxs-lookup"><span data-stu-id="d122d-107">This API is not intended to change the reviewers or decisions of a review.</span></span>  <span data-ttu-id="d122d-108">Para cambiar los revisores, use el [addReviewer](accessreview-addreviewer.md) o [removeReviewer](accessreview-removereviewer.md) API.</span><span class="sxs-lookup"><span data-stu-id="d122d-108">To change the reviewers, use the [addReviewer](accessreview-addreviewer.md) or [removeReviewer](accessreview-removereviewer.md) APIs.</span></span>  <span data-ttu-id="d122d-109">Para detener una revisión única ya iniciado, o una instancia ya inició de una revisión periódica, pronto, utilice la [detención](accessreview-stop.md) API y para aplicar las decisiones a los derechos de acceso destino grupo o aplicación, use la [Aplicar](accessreview-apply.md) API.</span><span class="sxs-lookup"><span data-stu-id="d122d-109">To stop an already-started one-time review, or an already-started instance of a recurring review, early, use the [stop](accessreview-stop.md) API, and to apply the decisions to the target group or app access rights, use the [apply](accessreview-apply.md) API.</span></span> 


## <a name="permissions"></a><span data-ttu-id="d122d-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="d122d-110">Permissions</span></span>
<span data-ttu-id="d122d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d122d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d122d-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d122d-113">Permission type</span></span>                        | <span data-ttu-id="d122d-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d122d-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="d122d-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d122d-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="d122d-116">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d122d-116">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="d122d-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d122d-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d122d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d122d-118">Not supported.</span></span> |
|<span data-ttu-id="d122d-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d122d-119">Application</span></span>                            | <span data-ttu-id="d122d-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d122d-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d122d-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d122d-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /accessReviews('{reviewId}')
```
## <a name="request-headers"></a><span data-ttu-id="d122d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d122d-122">Request headers</span></span>
| <span data-ttu-id="d122d-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="d122d-123">Name</span></span>         | <span data-ttu-id="d122d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="d122d-124">Type</span></span>        | <span data-ttu-id="d122d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d122d-125">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="d122d-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="d122d-126">Authorization</span></span> | <span data-ttu-id="d122d-127">string</span><span class="sxs-lookup"><span data-stu-id="d122d-127">string</span></span> | <span data-ttu-id="d122d-128">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="d122d-128">Bearer \{token\}.</span></span> <span data-ttu-id="d122d-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d122d-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d122d-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d122d-130">Request body</span></span>
<span data-ttu-id="d122d-131">En el cuerpo de la solicitud, proporcionar una representación JSON de parámetros de un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="d122d-131">In the request body, supply a JSON representation of a parameters of an [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="d122d-132">La siguiente tabla muestran las propiedades que se pueden proporcionar cuando se actualiza un accessReview.</span><span class="sxs-lookup"><span data-stu-id="d122d-132">The following table shows the properties that can be supplied when you update an accessReview.</span></span>

| <span data-ttu-id="d122d-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d122d-133">Property</span></span>     | <span data-ttu-id="d122d-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="d122d-134">Type</span></span>        | <span data-ttu-id="d122d-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="d122d-135">Description</span></span> |
|:-------------|:------------|:------------|
| `displayName`             |`String`                                                        | <span data-ttu-id="d122d-136">Nombre de la revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="d122d-136">The access review name.</span></span>  |
| `startDateTime`           |`DateTimeOffset`                                                | <span data-ttu-id="d122d-137">La fecha y hora cuando la revisión está programada para que se inicie.</span><span class="sxs-lookup"><span data-stu-id="d122d-137">The DateTime when the review is scheduled to be start.</span></span>  <span data-ttu-id="d122d-138">Esto debe ser una fecha en el futuro.</span><span class="sxs-lookup"><span data-stu-id="d122d-138">This must be a date in the future.</span></span>   |
| `endDateTime`             |`DateTimeOffset`                                                | <span data-ttu-id="d122d-139">La fecha y hora cuando la revisión está programada para finalizar.</span><span class="sxs-lookup"><span data-stu-id="d122d-139">The DateTime when the review is scheduled to end.</span></span> <span data-ttu-id="d122d-140">Esto debe ser al menos un día posterior a la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="d122d-140">This must be at least one day later than the start date.</span></span>   |
| `description`             |`String`                                                        | <span data-ttu-id="d122d-141">La descripción, para mostrar a los revisores.</span><span class="sxs-lookup"><span data-stu-id="d122d-141">The description, to show to the reviewers.</span></span> |



## <a name="response"></a><span data-ttu-id="d122d-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d122d-142">Response</span></span>
<span data-ttu-id="d122d-143">Si tiene éxito, este método devuelve una `204, Accepted` código de respuesta y un objeto [accessReview](../resources/accessreview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d122d-143">If successful, this method returns a `204, Accepted` response code and an [accessReview](../resources/accessreview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d122d-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d122d-144">Example</span></span>

<span data-ttu-id="d122d-145">Éste es un ejemplo de actualización de una única revisión de access (no recurrentes).</span><span class="sxs-lookup"><span data-stu-id="d122d-145">This is an example of updating a one-time (not reoccurring) access review.</span></span>

##### <a name="request"></a><span data-ttu-id="d122d-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d122d-146">Request</span></span>
<span data-ttu-id="d122d-147">En el cuerpo de la solicitud, proporcionar una representación JSON de las nuevas propiedades del objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="d122d-147">In the request body, supply a JSON representation of the new properties of the [accessReview](../resources/accessreview.md) object.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_accessReview"
}-->
```http
PATCH https://graph.microsoft.com/beta/accessReviews('006111db-0810-4494-a6df-904d368bd81b')
Content-type: application/json

{
    "displayName":"TestReview new name"
}
```

##### <a name="response"></a><span data-ttu-id="d122d-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d122d-148">Response</span></span>
><span data-ttu-id="d122d-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d122d-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview"
} -->
```http
HTTP/1.1 204 Accepted
Content-type: application/json

{
    "id": "006111db-0810-4494-a6df-904d368bd81b",
    "displayName": "TestReview new name",
    "startDateTime": "2017-02-10T00:35:53.214Z",
    "endDateTime": "2017-03-12T00:35:53.214Z",
    "status": "Initializing",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "reviewerType": "delegate",
    "description": "Sample description"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "Update accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
