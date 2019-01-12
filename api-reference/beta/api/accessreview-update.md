---
title: Actualizar accessReview
description: En la característica de revisiones de access Azure AD, actualice un objeto accessReview existente para cambiar una o varias de sus propiedades.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e09219c1979f974b62f17c52163fc93b5d2d3c2a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941362"
---
# <a name="update-accessreview"></a><span data-ttu-id="37304-103">Actualizar accessReview</span><span class="sxs-lookup"><span data-stu-id="37304-103">Update accessReview</span></span>

> <span data-ttu-id="37304-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37304-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37304-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37304-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="37304-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, actualice un objeto [accessReview](../resources/accessreview.md) existente para cambiar una o varias de sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="37304-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, update an existing [accessReview](../resources/accessreview.md) object to change one or more of its properties.</span></span>

<span data-ttu-id="37304-107">Esta API no está pensada para cambiar los revisores o las decisiones de una revisión.</span><span class="sxs-lookup"><span data-stu-id="37304-107">This API is not intended to change the reviewers or decisions of a review.</span></span>  <span data-ttu-id="37304-108">Para cambiar los revisores, use el [addReviewer](accessreview-addreviewer.md) o [removeReviewer](accessreview-removereviewer.md) API.</span><span class="sxs-lookup"><span data-stu-id="37304-108">To change the reviewers, use the [addReviewer](accessreview-addreviewer.md) or [removeReviewer](accessreview-removereviewer.md) APIs.</span></span>  <span data-ttu-id="37304-109">Para detener una revisión única ya iniciado, o una instancia ya inició de una revisión periódica, pronto, utilice la [detención](accessreview-stop.md) API y para aplicar las decisiones a los derechos de acceso destino grupo o aplicación, use la [Aplicar](accessreview-apply.md) API.</span><span class="sxs-lookup"><span data-stu-id="37304-109">To stop an already-started one-time review, or an already-started instance of a recurring review, early, use the [stop](accessreview-stop.md) API, and to apply the decisions to the target group or app access rights, use the [apply](accessreview-apply.md) API.</span></span> 


## <a name="permissions"></a><span data-ttu-id="37304-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="37304-110">Permissions</span></span>
<span data-ttu-id="37304-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37304-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37304-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37304-113">Permission type</span></span>                        | <span data-ttu-id="37304-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37304-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="37304-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37304-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="37304-116">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="37304-116">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="37304-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37304-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="37304-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37304-118">Not supported.</span></span> |
|<span data-ttu-id="37304-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37304-119">Application</span></span>                            | <span data-ttu-id="37304-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37304-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="37304-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37304-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /accessReviews('{reviewId}')
```
## <a name="request-headers"></a><span data-ttu-id="37304-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37304-122">Request headers</span></span>
| <span data-ttu-id="37304-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="37304-123">Name</span></span>         | <span data-ttu-id="37304-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="37304-124">Type</span></span>        | <span data-ttu-id="37304-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="37304-125">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="37304-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="37304-126">Authorization</span></span> | <span data-ttu-id="37304-127">string</span><span class="sxs-lookup"><span data-stu-id="37304-127">string</span></span> | <span data-ttu-id="37304-128">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="37304-128">Bearer \{token\}.</span></span> <span data-ttu-id="37304-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37304-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="37304-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37304-130">Request body</span></span>
<span data-ttu-id="37304-131">En el cuerpo de la solicitud, proporcionar una representación JSON de parámetros de un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="37304-131">In the request body, supply a JSON representation of a parameters of an [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="37304-132">La siguiente tabla muestran las propiedades que se pueden proporcionar cuando se actualiza un accessReview.</span><span class="sxs-lookup"><span data-stu-id="37304-132">The following table shows the properties that can be supplied when you update an accessReview.</span></span>

| <span data-ttu-id="37304-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37304-133">Property</span></span>     | <span data-ttu-id="37304-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="37304-134">Type</span></span>        | <span data-ttu-id="37304-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="37304-135">Description</span></span> |
|:-------------|:------------|:------------|
| `displayName`             |`String`                                                        | <span data-ttu-id="37304-136">Nombre de la revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="37304-136">The access review name.</span></span>  |
| `startDateTime`           |`DateTimeOffset`                                                | <span data-ttu-id="37304-137">La fecha y hora cuando la revisión está programada para que se inicie.</span><span class="sxs-lookup"><span data-stu-id="37304-137">The DateTime when the review is scheduled to be start.</span></span>  <span data-ttu-id="37304-138">Esto debe ser una fecha en el futuro.</span><span class="sxs-lookup"><span data-stu-id="37304-138">This must be a date in the future.</span></span>   |
| `endDateTime`             |`DateTimeOffset`                                                | <span data-ttu-id="37304-139">La fecha y hora cuando la revisión está programada para finalizar.</span><span class="sxs-lookup"><span data-stu-id="37304-139">The DateTime when the review is scheduled to end.</span></span> <span data-ttu-id="37304-140">Esto debe ser al menos un día posterior a la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="37304-140">This must be at least one day later than the start date.</span></span>   |
| `description`             |`String`                                                        | <span data-ttu-id="37304-141">La descripción, para mostrar a los revisores.</span><span class="sxs-lookup"><span data-stu-id="37304-141">The description, to show to the reviewers.</span></span> |



## <a name="response"></a><span data-ttu-id="37304-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37304-142">Response</span></span>
<span data-ttu-id="37304-143">Si tiene éxito, este método devuelve una `204, Accepted` código de respuesta y un objeto [accessReview](../resources/accessreview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37304-143">If successful, this method returns a `204, Accepted` response code and an [accessReview](../resources/accessreview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37304-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37304-144">Example</span></span>

<span data-ttu-id="37304-145">Éste es un ejemplo de actualización de una única revisión de access (no recurrentes).</span><span class="sxs-lookup"><span data-stu-id="37304-145">This is an example of updating a one-time (not reoccurring) access review.</span></span>

##### <a name="request"></a><span data-ttu-id="37304-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37304-146">Request</span></span>
<span data-ttu-id="37304-147">En el cuerpo de la solicitud, proporcionar una representación JSON de las nuevas propiedades del objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="37304-147">In the request body, supply a JSON representation of the new properties of the [accessReview](../resources/accessreview.md) object.</span></span>

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

##### <a name="response"></a><span data-ttu-id="37304-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37304-148">Response</span></span>
><span data-ttu-id="37304-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37304-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
