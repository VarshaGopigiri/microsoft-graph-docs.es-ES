---
title: Eliminar accessReview
description: En AD Azure access revisiones característica, eliminar un objeto accessReview.
ms.openlocfilehash: b9578b575705de909eca99ac70f5efbb70d053cc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084343"
---
# <a name="delete-accessreview"></a><span data-ttu-id="63ab9-103">Eliminar accessReview</span><span class="sxs-lookup"><span data-stu-id="63ab9-103">Delete accessReview</span></span>

> <span data-ttu-id="63ab9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63ab9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63ab9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63ab9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="63ab9-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, eliminar un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="63ab9-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, delete an [accessReview](../resources/accessreview.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="63ab9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="63ab9-107">Permissions</span></span>
<span data-ttu-id="63ab9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63ab9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63ab9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63ab9-110">Permission type</span></span>                        | <span data-ttu-id="63ab9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63ab9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="63ab9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63ab9-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="63ab9-113">AccessReview.ReadWrite.All y también deben tener ProgramControl.ReadWrite.All a un escenario completo con una llamada para eliminar un programControl</span><span class="sxs-lookup"><span data-stu-id="63ab9-113">AccessReview.ReadWrite.All, and should also have ProgramControl.ReadWrite.All to complete scenario with a call to delete a programControl</span></span> |
|<span data-ttu-id="63ab9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63ab9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="63ab9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63ab9-115">Not supported.</span></span> |
|<span data-ttu-id="63ab9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63ab9-116">Application</span></span>                            | <span data-ttu-id="63ab9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63ab9-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="63ab9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63ab9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /accessReviews('<id>')
```
## <a name="request-headers"></a><span data-ttu-id="63ab9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63ab9-119">Request headers</span></span>
| <span data-ttu-id="63ab9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="63ab9-120">Name</span></span>         | <span data-ttu-id="63ab9-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="63ab9-121">Type</span></span>        | <span data-ttu-id="63ab9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="63ab9-122">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="63ab9-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="63ab9-123">Authorization</span></span> | <span data-ttu-id="63ab9-124">string</span><span class="sxs-lookup"><span data-stu-id="63ab9-124">string</span></span> | <span data-ttu-id="63ab9-125">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="63ab9-125">Bearer \{token\}.</span></span> <span data-ttu-id="63ab9-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63ab9-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="63ab9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63ab9-127">Request body</span></span>
<span data-ttu-id="63ab9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="63ab9-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="63ab9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63ab9-129">Response</span></span>
<span data-ttu-id="63ab9-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63ab9-p104">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63ab9-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63ab9-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="63ab9-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63ab9-133">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_accessReview"
}-->
```http
DELETE https://graph.microsoft.com/beta/accessReviews('2975E9B5-44CE-4E71-93D3-30F03B5AA992')
```
##### <a name="response"></a><span data-ttu-id="63ab9-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63ab9-134">Response</span></span>
><span data-ttu-id="63ab9-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63ab9-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
