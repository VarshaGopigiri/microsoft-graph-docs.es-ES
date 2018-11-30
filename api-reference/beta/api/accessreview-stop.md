---
title: Detener accessReview
description: En el anuncio de Azure access revisa la característica, detener una accessReview actualmente activa.  El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.  (Para impedir que una revisión periódica de acceso iniciar instancias futuras, actualizarlo para cambiar su fecha de finalización programada).  Después de obtener el acceso revisar se detiene, revisores ya no pueden dar a la entrada y las decisiones de revisión de acceso se pueden aplicar.
ms.openlocfilehash: 2a4ac5d13f3be70cc5a4a24f4051429c473e7690
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085966"
---
# <a name="stop-accessreview"></a><span data-ttu-id="fc1fb-106">Detener accessReview</span><span class="sxs-lookup"><span data-stu-id="fc1fb-106">Stop accessReview</span></span>

> <span data-ttu-id="fc1fb-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc1fb-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fc1fb-109">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, detenga un activo actualmente [accessReview](../resources/accessreview.md).</span><span class="sxs-lookup"><span data-stu-id="fc1fb-109">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, stop a currently active [accessReview](../resources/accessreview.md).</span></span>  <span data-ttu-id="fc1fb-110">El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-110">The target object can be either a one-time access review, or an instance of a recurring access review.</span></span>  <span data-ttu-id="fc1fb-111">(Para impedir que una revisión periódica de acceso iniciar instancias futuras, [actualizarlo](accessreview-update.md) para cambiar su fecha de finalización programada).</span><span class="sxs-lookup"><span data-stu-id="fc1fb-111">(To prevent a recurring access review from starting future instances, [update it](accessreview-update.md) to change its scheduled end date).</span></span>  <span data-ttu-id="fc1fb-112">Después de obtener el acceso revisar se detiene, revisores ya no pueden dar a la entrada y las decisiones de revisión de acceso se pueden aplicar.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-112">After the access review stops, reviewers can no longer give input, and the access review decisions can be applied.</span></span>
## <a name="permissions"></a><span data-ttu-id="fc1fb-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc1fb-113">Permissions</span></span>
<span data-ttu-id="fc1fb-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc1fb-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc1fb-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc1fb-116">Permission type</span></span>                        | <span data-ttu-id="fc1fb-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc1fb-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="fc1fb-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc1fb-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="fc1fb-119">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc1fb-119">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="fc1fb-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc1fb-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fc1fb-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-121">Not supported.</span></span> |
|<span data-ttu-id="fc1fb-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc1fb-122">Application</span></span>                            | <span data-ttu-id="fc1fb-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-123">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fc1fb-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc1fb-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews('<id>')/stop()
```
## <a name="request-headers"></a><span data-ttu-id="fc1fb-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc1fb-125">Request headers</span></span>
| <span data-ttu-id="fc1fb-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc1fb-126">Name</span></span>         | <span data-ttu-id="fc1fb-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc1fb-127">Type</span></span>        | <span data-ttu-id="fc1fb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc1fb-128">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="fc1fb-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc1fb-129">Authorization</span></span> | <span data-ttu-id="fc1fb-130">string</span><span class="sxs-lookup"><span data-stu-id="fc1fb-130">string</span></span> | <span data-ttu-id="fc1fb-131">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-131">Bearer \{token\}.</span></span> <span data-ttu-id="fc1fb-132">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-132">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fc1fb-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc1fb-133">Request body</span></span>
<span data-ttu-id="fc1fb-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-134">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="fc1fb-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc1fb-135">Response</span></span>
<span data-ttu-id="fc1fb-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-p106">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc1fb-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc1fb-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fc1fb-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc1fb-139">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "stop_accessReview"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews('2975E9B5-44CE-4E71-93D3-30F03B5AA992')/stop()
```
##### <a name="response"></a><span data-ttu-id="fc1fb-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc1fb-140">Response</span></span>
><span data-ttu-id="fc1fb-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "Stop accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
