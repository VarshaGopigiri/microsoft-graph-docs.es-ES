---
title: Obtener el contrato
description: Recuperar las propiedades y relaciones de un objeto de contrato.
ms.openlocfilehash: 9887ed39bcb2a63980388e5265bb56d6500625d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084652"
---
# <a name="get-agreement"></a><span data-ttu-id="17dcd-103">Obtener el contrato</span><span class="sxs-lookup"><span data-stu-id="17dcd-103">Get agreement</span></span>

> <span data-ttu-id="17dcd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17dcd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17dcd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17dcd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="17dcd-106">Recuperar las propiedades y relaciones de un objeto de [contrato](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="17dcd-106">Retrieve the properties and relationships of an [agreement](../resources/agreement.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="17dcd-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="17dcd-107">Permissions</span></span>
<span data-ttu-id="17dcd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17dcd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17dcd-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17dcd-110">Permission type</span></span>                        | <span data-ttu-id="17dcd-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17dcd-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="17dcd-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17dcd-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="17dcd-113">Agreement.Read.All</span><span class="sxs-lookup"><span data-stu-id="17dcd-113">Agreement.Read.All</span></span> |
|<span data-ttu-id="17dcd-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17dcd-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="17dcd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17dcd-115">Not supported.</span></span> |
|<span data-ttu-id="17dcd-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17dcd-116">Application</span></span>                            | <span data-ttu-id="17dcd-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17dcd-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="17dcd-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17dcd-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /agreements/<id>
```
<!--
## Optional query parameters
This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.
-->

## <a name="request-headers"></a><span data-ttu-id="17dcd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17dcd-119">Request headers</span></span>
| <span data-ttu-id="17dcd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="17dcd-120">Name</span></span>         | <span data-ttu-id="17dcd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="17dcd-121">Type</span></span>        | <span data-ttu-id="17dcd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="17dcd-122">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="17dcd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="17dcd-123">Authorization</span></span> | <span data-ttu-id="17dcd-124">string</span><span class="sxs-lookup"><span data-stu-id="17dcd-124">string</span></span> | <span data-ttu-id="17dcd-125">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="17dcd-125">Bearer \{token\}.</span></span> <span data-ttu-id="17dcd-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17dcd-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="17dcd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17dcd-127">Request body</span></span>
<span data-ttu-id="17dcd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17dcd-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="17dcd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17dcd-129">Response</span></span>
<span data-ttu-id="17dcd-130">Si tiene éxito, este método devuelve una `200 OK` objeto de [acuerdo](../resources/agreement.md) y código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17dcd-130">If successful, this method returns a `200 OK` response code and [agreement](../resources/agreement.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="17dcd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17dcd-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="17dcd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17dcd-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_agreement"
}-->
```http
GET https://graph.microsoft.com/beta/agreements/<id>?$expand=files
```
##### <a name="response"></a><span data-ttu-id="17dcd-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17dcd-133">Response</span></span>
><span data-ttu-id="17dcd-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17dcd-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.agreement"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "displayName": "MSGraph Sample",
  "isViewingBeforeAcceptanceRequired": true,
  "id": "id-value",
  "files": [
    {
      "id": "id-value",
      "language": "en",
      "fileName": "TOU.pdf",
      "isDefault": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get agreement",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
