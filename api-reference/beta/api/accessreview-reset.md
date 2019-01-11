---
title: Restablecer accessReview
description: En la característica de revisiones de access Azure AD, restablecer las decisiones de un accessReview actualmente activa.  El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.  Ya no se registran las decisiones anteriores, pero pueden continuar revisores actualizar las decisiones.
localization_priority: Normal
ms.openlocfilehash: 750b9e4da130a087350b7b78c53e71c835d12be1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809579"
---
# <a name="reset-accessreview"></a><span data-ttu-id="b8aea-105">Restablecer accessReview</span><span class="sxs-lookup"><span data-stu-id="b8aea-105">Reset accessReview</span></span>

> <span data-ttu-id="b8aea-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b8aea-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b8aea-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b8aea-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b8aea-108">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, restablecer las decisiones de un activo actualmente [accessReview](../resources/accessreview.md).</span><span class="sxs-lookup"><span data-stu-id="b8aea-108">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, reset the decisions of a currently active [accessReview](../resources/accessreview.md).</span></span>  <span data-ttu-id="b8aea-109">El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.</span><span class="sxs-lookup"><span data-stu-id="b8aea-109">The target object can be either a one-time access review, or an instance of a recurring access review.</span></span>  <span data-ttu-id="b8aea-110">Ya no se registran las decisiones anteriores, pero pueden continuar revisores actualizar las decisiones.</span><span class="sxs-lookup"><span data-stu-id="b8aea-110">Previous decisions are no longer recorded, but reviewers can continue to update decisions.</span></span>

## <a name="permissions"></a><span data-ttu-id="b8aea-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="b8aea-111">Permissions</span></span>
<span data-ttu-id="b8aea-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8aea-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8aea-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8aea-114">Permission type</span></span>                        | <span data-ttu-id="b8aea-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8aea-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="b8aea-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8aea-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="b8aea-117">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8aea-117">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="b8aea-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8aea-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b8aea-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8aea-119">Not supported.</span></span> |
|<span data-ttu-id="b8aea-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8aea-120">Application</span></span>                            | <span data-ttu-id="b8aea-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8aea-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b8aea-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8aea-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews('<id>')/resetDecisions()
```
## <a name="request-headers"></a><span data-ttu-id="b8aea-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8aea-123">Request headers</span></span>
| <span data-ttu-id="b8aea-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="b8aea-124">Name</span></span>         | <span data-ttu-id="b8aea-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8aea-125">Type</span></span>        | <span data-ttu-id="b8aea-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8aea-126">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="b8aea-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="b8aea-127">Authorization</span></span> | <span data-ttu-id="b8aea-128">string</span><span class="sxs-lookup"><span data-stu-id="b8aea-128">string</span></span> | <span data-ttu-id="b8aea-129">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="b8aea-129">Bearer \{token\}.</span></span> <span data-ttu-id="b8aea-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="b8aea-130">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b8aea-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8aea-131">Request body</span></span>
<span data-ttu-id="b8aea-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b8aea-132">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="b8aea-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8aea-133">Response</span></span>
<span data-ttu-id="b8aea-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8aea-p106">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8aea-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8aea-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b8aea-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8aea-137">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "reset_accessReview"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews('2975E9B5-44CE-4E71-93D3-30F03B5AA992')/resetDecisions()
```
##### <a name="response"></a><span data-ttu-id="b8aea-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8aea-138">Response</span></span>
><span data-ttu-id="b8aea-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8aea-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-25 00:00:01 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Reset accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
