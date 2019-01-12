---
title: Quitar accessReview revisor
description: 'En la característica de revisiones de access Azure AD, actualice un objeto accessReview existente para quitar un usuario como un revisor.  Esta operación sólo se permite para una revisión de acceso que no se ha completado y solo para una revisión de acceso donde se especifican explícitamente los revisores. Esta operación no es permitida para una revisión de access en la que los usuarios revisión su propio acceso y no está pensada para una revisión de access en la que se asignan los propietarios del grupo como los revisores. '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 84bf3d973820067e0d4561e9647f688c025d957f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956693"
---
# <a name="remove-accessreview-reviewer"></a><span data-ttu-id="ab588-105">Quitar accessReview revisor</span><span class="sxs-lookup"><span data-stu-id="ab588-105">Remove accessReview reviewer</span></span>

> <span data-ttu-id="ab588-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab588-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab588-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab588-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ab588-108">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, actualice un objeto [accessReview](../resources/accessreview.md) existente para quitar un usuario como un revisor.</span><span class="sxs-lookup"><span data-stu-id="ab588-108">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, update an existing [accessReview](../resources/accessreview.md) object to remove a user as a reviewer.</span></span>  <span data-ttu-id="ab588-109">Esta operación sólo se permite para una revisión de acceso que no se ha completado y solo para una revisión de acceso donde se especifican explícitamente los revisores.</span><span class="sxs-lookup"><span data-stu-id="ab588-109">This operation is only permitted for an access review that is not yet completed, and only for an access review where the reviewers are explicitly specified.</span></span> <span data-ttu-id="ab588-110">Esta operación no es permitida para una revisión de access en la que los usuarios revisión su propio acceso y no está pensada para una revisión de access en la que se asignan los propietarios del grupo como los revisores.</span><span class="sxs-lookup"><span data-stu-id="ab588-110">This operation is not permitted for an access review in which users review their own access, and not intended for an access review in which the group owners are assigned as the reviewers.</span></span> 


## <a name="permissions"></a><span data-ttu-id="ab588-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="ab588-111">Permissions</span></span>
<span data-ttu-id="ab588-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab588-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ab588-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab588-114">Permission type</span></span>                        | <span data-ttu-id="ab588-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab588-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="ab588-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab588-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="ab588-117">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab588-117">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="ab588-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab588-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ab588-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab588-119">Not supported.</span></span> |
|<span data-ttu-id="ab588-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab588-120">Application</span></span>                            | <span data-ttu-id="ab588-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab588-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ab588-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab588-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /accessReviews('{reviewId}')/reviewers('{userId'})
```
## <a name="request-headers"></a><span data-ttu-id="ab588-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab588-123">Request headers</span></span>
| <span data-ttu-id="ab588-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab588-124">Name</span></span>         | <span data-ttu-id="ab588-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab588-125">Type</span></span>        | <span data-ttu-id="ab588-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab588-126">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="ab588-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="ab588-127">Authorization</span></span> | <span data-ttu-id="ab588-128">string</span><span class="sxs-lookup"><span data-stu-id="ab588-128">string</span></span> | <span data-ttu-id="ab588-129">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="ab588-129">Bearer \{token\}.</span></span> <span data-ttu-id="ab588-130">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab588-130">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ab588-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ab588-131">Request body</span></span>
<span data-ttu-id="ab588-132">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab588-132">No request body should be supplied.</span></span>


## <a name="response"></a><span data-ttu-id="ab588-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab588-133">Response</span></span>
<span data-ttu-id="ab588-134">Si se realiza correctamente, este método devuelve un código de respuesta de la serie de 200.</span><span class="sxs-lookup"><span data-stu-id="ab588-134">If successful, this method returns a 200-series response code.</span></span>

## <a name="example"></a><span data-ttu-id="ab588-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab588-135">Example</span></span>

<span data-ttu-id="ab588-136">Éste es un ejemplo de actualización de una única revisión de access (no recurrentes) para quitar un revisor innecesario.</span><span class="sxs-lookup"><span data-stu-id="ab588-136">This is an example of updating a one-time (not reoccurring) access review to remove an unnecessary reviewer.</span></span>


##### <a name="request"></a><span data-ttu-id="ab588-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab588-137">Request</span></span>
<span data-ttu-id="ab588-138">En la dirección URL de la solicitud, proporcione el identificador del objeto accessReview y, a continuación, el identificador del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="ab588-138">In the request URL, supply the id of the accessReview object and then the id of the user object.</span></span>

<!-- {
  "blockType": "request",
  "name": "remove_accessReview_reviewer"
}-->
```http
DELETE https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/reviewers('006111db-0810-4494-a6df-904d368bd81b')

```

##### <a name="response"></a><span data-ttu-id="ab588-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab588-139">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No content
```

<!-- {
  "type": "#page.annotation",
  "description": "Remove accessReview reviewer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
