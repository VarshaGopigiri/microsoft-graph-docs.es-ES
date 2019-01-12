---
title: Agregar revisor accessReview
description: 'En la característica de revisiones de access Azure AD, actualice un objeto accessReview existente para agregar otro usuario como un revisor.  Esta operación sólo se permite para una revisión de acceso que no se ha completado y solo para una revisión de acceso donde se especifican explícitamente los revisores. Esta operación no es permitida para una revisión de access en la que los usuarios revisión su propio acceso y no está pensada para una revisión de access en la que se asignan los propietarios del grupo como los revisores. '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: a7745cf6424f3aa8b9bca16f4db961801d203431
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956867"
---
# <a name="add-accessreview-reviewer"></a><span data-ttu-id="39396-105">Agregar revisor accessReview</span><span class="sxs-lookup"><span data-stu-id="39396-105">Add accessReview reviewer</span></span>

> <span data-ttu-id="39396-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="39396-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="39396-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="39396-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="39396-108">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, actualice un objeto [accessReview](../resources/accessreview.md) existente para agregar otro usuario como un revisor.</span><span class="sxs-lookup"><span data-stu-id="39396-108">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, update an existing [accessReview](../resources/accessreview.md) object to add another user as a reviewer.</span></span>  <span data-ttu-id="39396-109">Esta operación sólo se permite para una revisión de acceso que no se ha completado y solo para una revisión de acceso donde se especifican explícitamente los revisores.</span><span class="sxs-lookup"><span data-stu-id="39396-109">This operation is only permitted for an access review that is not yet completed, and only for an access review where the reviewers are explicitly specified.</span></span> <span data-ttu-id="39396-110">Esta operación no es permitida para una revisión de access en la que los usuarios revisión su propio acceso y no está pensada para una revisión de access en la que se asignan los propietarios del grupo como los revisores.</span><span class="sxs-lookup"><span data-stu-id="39396-110">This operation is not permitted for an access review in which users review their own access, and not intended for an access review in which the group owners are assigned as the reviewers.</span></span> 


## <a name="permissions"></a><span data-ttu-id="39396-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="39396-111">Permissions</span></span>
<span data-ttu-id="39396-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39396-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39396-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39396-114">Permission type</span></span>                        | <span data-ttu-id="39396-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39396-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="39396-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39396-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="39396-117">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39396-117">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="39396-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39396-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="39396-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39396-119">Not supported.</span></span> |
|<span data-ttu-id="39396-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39396-120">Application</span></span>                            | <span data-ttu-id="39396-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39396-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="39396-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39396-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews('{reviewId}')/reviewers
```
## <a name="request-headers"></a><span data-ttu-id="39396-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39396-123">Request headers</span></span>
| <span data-ttu-id="39396-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="39396-124">Name</span></span>         | <span data-ttu-id="39396-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="39396-125">Type</span></span>        | <span data-ttu-id="39396-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="39396-126">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="39396-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="39396-127">Authorization</span></span> | <span data-ttu-id="39396-128">string</span><span class="sxs-lookup"><span data-stu-id="39396-128">string</span></span> | <span data-ttu-id="39396-129">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="39396-129">Bearer \{token\}.</span></span> <span data-ttu-id="39396-130">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="39396-130">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="39396-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39396-131">Request body</span></span>
<span data-ttu-id="39396-132">En el cuerpo de la solicitud, proporcionar una representación JSON del identificador de un usuario que será un revisor.</span><span class="sxs-lookup"><span data-stu-id="39396-132">In the request body, supply a JSON representation of the ID of a user who will be a reviewer.</span></span>

<span data-ttu-id="39396-133">La siguiente tabla muestran las propiedades que se pueden proporcionar cuando se actualiza un accessReview.</span><span class="sxs-lookup"><span data-stu-id="39396-133">The following table shows the properties that can be supplied when you update an accessReview.</span></span>

| <span data-ttu-id="39396-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39396-134">Property</span></span>     | <span data-ttu-id="39396-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="39396-135">Type</span></span>        | <span data-ttu-id="39396-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="39396-136">Description</span></span> |
|:-------------|:------------|:------------|
| `id`             |`String`                                                        | <span data-ttu-id="39396-137">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="39396-137">The user ID.</span></span>  |


## <a name="response"></a><span data-ttu-id="39396-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39396-138">Response</span></span>
<span data-ttu-id="39396-139">Si tiene éxito, este método devuelve una `201, Created` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="39396-139">If successful, this method returns a `201, Created` response code .</span></span>

## <a name="example"></a><span data-ttu-id="39396-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39396-140">Example</span></span>

<span data-ttu-id="39396-141">Éste es un ejemplo de actualización de una única revisión de access (no recurrentes) con un revisor adicional.</span><span class="sxs-lookup"><span data-stu-id="39396-141">This is an example of updating a one-time (not reoccurring) access review with an additional reviewer.</span></span>

##### <a name="request"></a><span data-ttu-id="39396-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39396-142">Request</span></span>
<span data-ttu-id="39396-143">En el cuerpo de la solicitud, proporcionar una representación JSON del identificador del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="39396-143">In the request body, supply a JSON representation of the id of the user object.</span></span>

<!-- {
  "blockType": "request",
  "name": "add_accessReview_reviewer"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/reviewers
Content-type: application/json

{
    "id":"006111db-0810-4494-a6df-904d368bd81b"
}
```

##### <a name="response"></a><span data-ttu-id="39396-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39396-144">Response</span></span>
><span data-ttu-id="39396-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39396-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 201 Created

```

<!-- {
  "type": "#page.annotation",
  "description": "Add accessReview reviewer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
