---
title: Revisores accessReview de lista
description: En el anuncio de Azure access revisa la característica, recuperar los revisores de un objeto accessReview.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 8dca759f71f13af18c291f1af9843da6729ef701
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946815"
---
# <a name="list-accessreview-reviewers"></a><span data-ttu-id="cc4e3-103">Revisores accessReview de lista</span><span class="sxs-lookup"><span data-stu-id="cc4e3-103">List accessReview reviewers</span></span>

> <span data-ttu-id="cc4e3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cc4e3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cc4e3-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, recuperar los revisores de un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="cc4e3-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, retrieve the reviewers of an [accessReview](../resources/accessreview.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="cc4e3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cc4e3-107">Permissions</span></span>
<span data-ttu-id="cc4e3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc4e3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc4e3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc4e3-110">Permission type</span></span>                        | <span data-ttu-id="cc4e3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc4e3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc4e3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc4e3-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="cc4e3-113">`AccessReview.Read.All`, `AccessReview.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-113"></span></span>  <span data-ttu-id="cc4e3-114">También debe ser el usuario iniciado en un rol de Active directory que le permita leer una revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-114">The signed in user must also be in a directory role which permits them to read an access review.</span></span> |
|<span data-ttu-id="cc4e3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc4e3-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc4e3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-116">Not supported.</span></span> |
|<span data-ttu-id="cc4e3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc4e3-117">Application</span></span>                            | <span data-ttu-id="cc4e3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc4e3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc4e3-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')/reviewers
```
## <a name="request-headers"></a><span data-ttu-id="cc4e3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc4e3-120">Request headers</span></span>
| <span data-ttu-id="cc4e3-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc4e3-121">Name</span></span>         | <span data-ttu-id="cc4e3-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc4e3-122">Type</span></span>        | <span data-ttu-id="cc4e3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc4e3-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="cc4e3-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc4e3-124">Authorization</span></span> | <span data-ttu-id="cc4e3-125">string</span><span class="sxs-lookup"><span data-stu-id="cc4e3-125">string</span></span> | <span data-ttu-id="cc4e3-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-126">Bearer \{token\}.</span></span> <span data-ttu-id="cc4e3-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cc4e3-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc4e3-128">Request body</span></span>
<span data-ttu-id="cc4e3-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="cc4e3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc4e3-130">Response</span></span>
<span data-ttu-id="cc4e3-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [IdentidadDeUsuario](../resources/useridentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-131">If successful, this method returns a `200, OK` response code and an array of [userIdentity](../resources/useridentity.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc4e3-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc4e3-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cc4e3-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc4e3-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_accessReview_reviewers"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/reviewers
```

##### <a name="response"></a><span data-ttu-id="cc4e3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc4e3-134">Response</span></span>
><span data-ttu-id="cc4e3-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.userIdentity",
  "isCollection": "true"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value":[
    {
       "id":"006111db-0810-4494-a6df-904d368bd81b"
    }
    ]
}
```

## <a name="see-also"></a><span data-ttu-id="cc4e3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc4e3-137">See also</span></span>

| <span data-ttu-id="cc4e3-138">Método</span><span class="sxs-lookup"><span data-stu-id="cc4e3-138">Method</span></span>           | <span data-ttu-id="cc4e3-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc4e3-139">Return Type</span></span>    |<span data-ttu-id="cc4e3-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc4e3-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="cc4e3-141">Obtener accessReview</span><span class="sxs-lookup"><span data-stu-id="cc4e3-141">Get accessReview</span></span>](accessreview-get.md) |  [<span data-ttu-id="cc4e3-142">accessReview</span><span class="sxs-lookup"><span data-stu-id="cc4e3-142">accessReview</span></span>](../resources/accessreview.md) |  <span data-ttu-id="cc4e3-143">Recuperar una revisión de access.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-143">Retrieve an access review.</span></span> |
|[<span data-ttu-id="cc4e3-144">Agregar revisor accessReview</span><span class="sxs-lookup"><span data-stu-id="cc4e3-144">Add accessReview reviewer</span></span>](accessreview-addreviewer.md) |     <span data-ttu-id="cc4e3-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-145">None.</span></span>   |   <span data-ttu-id="cc4e3-146">Agregar un revisor a una accessReview.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-146">Add a reviewer to an accessReview.</span></span> |
|[<span data-ttu-id="cc4e3-147">Quitar accessReview revisor</span><span class="sxs-lookup"><span data-stu-id="cc4e3-147">Remove accessReview reviewer</span></span>](accessreview-removereviewer.md) | <span data-ttu-id="cc4e3-148">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-148">None.</span></span> |   <span data-ttu-id="cc4e3-149">Quitar un revisor de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="cc4e3-149">Remove a reviewer from an accessReview.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview reviewers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
