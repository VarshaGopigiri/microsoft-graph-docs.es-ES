---
title: Obtener el contrato
description: Recuperar las propiedades y relaciones de un objeto de contrato.
localization_priority: Normal
ms.openlocfilehash: 0ca4e941705fe716c3aa11a73c934c40deb279d4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818658"
---
# <a name="get-agreement"></a><span data-ttu-id="8d7b1-103">Obtener el contrato</span><span class="sxs-lookup"><span data-stu-id="8d7b1-103">Get agreement</span></span>

> <span data-ttu-id="8d7b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d7b1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8d7b1-106">Recuperar las propiedades y relaciones de un objeto de [contrato](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="8d7b1-106">Retrieve the properties and relationships of an [agreement](../resources/agreement.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8d7b1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8d7b1-107">Permissions</span></span>
<span data-ttu-id="8d7b1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8d7b1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8d7b1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8d7b1-110">Permission type</span></span>                        | <span data-ttu-id="8d7b1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8d7b1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="8d7b1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8d7b1-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="8d7b1-113">Agreement.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d7b1-113">Agreement.Read.All</span></span> |
|<span data-ttu-id="8d7b1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8d7b1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8d7b1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-115">Not supported.</span></span> |
|<span data-ttu-id="8d7b1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8d7b1-116">Application</span></span>                            | <span data-ttu-id="8d7b1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8d7b1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8d7b1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /agreements/<id>
```
<!--
## Optional query parameters
This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.
-->

## <a name="request-headers"></a><span data-ttu-id="8d7b1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8d7b1-119">Request headers</span></span>
| <span data-ttu-id="8d7b1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="8d7b1-120">Name</span></span>         | <span data-ttu-id="8d7b1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d7b1-121">Type</span></span>        | <span data-ttu-id="8d7b1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d7b1-122">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="8d7b1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8d7b1-123">Authorization</span></span> | <span data-ttu-id="8d7b1-124">string</span><span class="sxs-lookup"><span data-stu-id="8d7b1-124">string</span></span> | <span data-ttu-id="8d7b1-125">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-125">Bearer \{token\}.</span></span> <span data-ttu-id="8d7b1-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8d7b1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8d7b1-127">Request body</span></span>
<span data-ttu-id="8d7b1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="8d7b1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d7b1-129">Response</span></span>
<span data-ttu-id="8d7b1-130">Si tiene éxito, este método devuelve una `200 OK` objeto de [acuerdo](../resources/agreement.md) y código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-130">If successful, this method returns a `200 OK` response code and [agreement](../resources/agreement.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8d7b1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d7b1-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8d7b1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8d7b1-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_agreement"
}-->
```http
GET https://graph.microsoft.com/beta/agreements/<id>?$expand=files
```
##### <a name="response"></a><span data-ttu-id="8d7b1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d7b1-133">Response</span></span>
><span data-ttu-id="8d7b1-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8d7b1-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
