---
title: SendReminder accessReview
description: 'En Azure AD tener acceso a la característica de revisiones, enviar un aviso a los revisores de un accessReview actualmente activa.  El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access. '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: cf5b78d2c67993fbf2da9be7c55a07fb752985c7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917282"
---
# <a name="sendreminder-accessreview"></a><span data-ttu-id="36f04-104">SendReminder accessReview</span><span class="sxs-lookup"><span data-stu-id="36f04-104">SendReminder accessReview</span></span>

> <span data-ttu-id="36f04-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36f04-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36f04-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36f04-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="36f04-107">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, enviar un aviso a los revisores de un activo actualmente [accessReview](../resources/accessreview.md).</span><span class="sxs-lookup"><span data-stu-id="36f04-107">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, send a reminder to the reviewers of a currently active [accessReview](../resources/accessreview.md).</span></span>  <span data-ttu-id="36f04-108">El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.</span><span class="sxs-lookup"><span data-stu-id="36f04-108">The target object can be either a one-time access review, or an instance of a recurring access review.</span></span> 

## <a name="permissions"></a><span data-ttu-id="36f04-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="36f04-109">Permissions</span></span>
<span data-ttu-id="36f04-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="36f04-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="36f04-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="36f04-112">Permission type</span></span>                        | <span data-ttu-id="36f04-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="36f04-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="36f04-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="36f04-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="36f04-115">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36f04-115">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="36f04-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="36f04-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="36f04-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36f04-117">Not supported.</span></span> |
|<span data-ttu-id="36f04-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="36f04-118">Application</span></span>                            | <span data-ttu-id="36f04-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36f04-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="36f04-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="36f04-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews('<id>')/sendReminder()
```
## <a name="request-headers"></a><span data-ttu-id="36f04-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="36f04-121">Request headers</span></span>
| <span data-ttu-id="36f04-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="36f04-122">Name</span></span>         | <span data-ttu-id="36f04-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="36f04-123">Type</span></span>        | <span data-ttu-id="36f04-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="36f04-124">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="36f04-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="36f04-125">Authorization</span></span> | <span data-ttu-id="36f04-126">string</span><span class="sxs-lookup"><span data-stu-id="36f04-126">string</span></span> | <span data-ttu-id="36f04-127">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="36f04-127">Bearer \{token\}.</span></span> <span data-ttu-id="36f04-128">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="36f04-128">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="36f04-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="36f04-129">Request body</span></span>
<span data-ttu-id="36f04-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="36f04-130">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="36f04-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36f04-131">Response</span></span>
<span data-ttu-id="36f04-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36f04-p106">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="36f04-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36f04-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="36f04-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="36f04-135">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "sendReminder_accessReview"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews('2975E9B5-44CE-4E71-93D3-30F03B5AA992')/sendReminder()
```
##### <a name="response"></a><span data-ttu-id="36f04-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36f04-136">Response</span></span>
><span data-ttu-id="36f04-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="36f04-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "SendReminder accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
