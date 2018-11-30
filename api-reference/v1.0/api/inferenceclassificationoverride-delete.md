---
title: Delete inferenceClassificationOverride
description: Elimina un reemplazo especificado por su identificador.
ms.openlocfilehash: ef4ff995e0e7f4392d9ca13835976076b3fdbe59
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029698"
---
# <a name="delete-inferenceclassificationoverride"></a><span data-ttu-id="3eccd-103">Delete inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="3eccd-103">Delete inferenceClassificationOverride</span></span>

<span data-ttu-id="3eccd-104">Elimina un reemplazo especificado por su identificador.</span><span class="sxs-lookup"><span data-stu-id="3eccd-104">Delete an override specified by its ID.</span></span>
## <a name="permissions"></a><span data-ttu-id="3eccd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3eccd-105">Permissions</span></span>
<span data-ttu-id="3eccd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3eccd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3eccd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3eccd-108">Permission type</span></span>      | <span data-ttu-id="3eccd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3eccd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3eccd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3eccd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3eccd-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3eccd-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="3eccd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3eccd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3eccd-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3eccd-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="3eccd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3eccd-114">Application</span></span> | <span data-ttu-id="3eccd-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3eccd-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3eccd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3eccd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/inferenceClassification/overrides/{id}
DELETE /users/{id}/inferenceClassification/overrides/{id}
```
## <a name="request-headers"></a><span data-ttu-id="3eccd-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3eccd-117">Request headers</span></span>
| <span data-ttu-id="3eccd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="3eccd-118">Name</span></span>       | <span data-ttu-id="3eccd-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3eccd-119">Type</span></span> | <span data-ttu-id="3eccd-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eccd-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3eccd-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3eccd-121">Authorization</span></span>  | <span data-ttu-id="3eccd-122">string</span><span class="sxs-lookup"><span data-stu-id="3eccd-122">string</span></span>  | <span data-ttu-id="3eccd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3eccd-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3eccd-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3eccd-125">Request body</span></span>
<span data-ttu-id="3eccd-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3eccd-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3eccd-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3eccd-127">Response</span></span>

<span data-ttu-id="3eccd-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3eccd-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3eccd-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3eccd-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3eccd-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3eccd-131">Request</span></span>
<span data-ttu-id="3eccd-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3eccd-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["98f5bdef-576a-404d-a2ea-07a3cf34af4r"],
  "name": "delete_inferenceclassificationoverride"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides/98f5bdef-576a-404d-a2ea-07a3cf34af4r
```
##### <a name="response"></a><span data-ttu-id="3eccd-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3eccd-133">Response</span></span>
<span data-ttu-id="3eccd-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3eccd-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete inferenceClassificationOverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->