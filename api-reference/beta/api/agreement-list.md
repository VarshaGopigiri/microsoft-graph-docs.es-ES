---
title: Contratos de lista
description: Recuperar una lista de objetos de contrato.
localization_priority: Normal
ms.openlocfilehash: 3ae255a386986b5627aed99f29dca5bfb9934e30
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859923"
---
# <a name="list-agreements"></a><span data-ttu-id="f155c-103">Contratos de lista</span><span class="sxs-lookup"><span data-stu-id="f155c-103">List agreements</span></span>

> <span data-ttu-id="f155c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f155c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f155c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f155c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f155c-106">Recuperar una lista de objetos de [contrato](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="f155c-106">Retrieve a list of [agreement](../resources/agreement.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="f155c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f155c-107">Permissions</span></span>
<span data-ttu-id="f155c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f155c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f155c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f155c-110">Permission type</span></span>                        | <span data-ttu-id="f155c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f155c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="f155c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f155c-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="f155c-113">Agreement.Read.All</span><span class="sxs-lookup"><span data-stu-id="f155c-113">Agreement.Read.All</span></span> |
|<span data-ttu-id="f155c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f155c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f155c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f155c-115">Not supported.</span></span> |
|<span data-ttu-id="f155c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f155c-116">Application</span></span>                            | <span data-ttu-id="f155c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f155c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f155c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f155c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /agreements
```
<!--
## Optional query parameters
This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.
-->

## <a name="request-headers"></a><span data-ttu-id="f155c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f155c-119">Request headers</span></span>
| <span data-ttu-id="f155c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f155c-120">Name</span></span>         | <span data-ttu-id="f155c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="f155c-121">Type</span></span>        | <span data-ttu-id="f155c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f155c-122">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="f155c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f155c-123">Authorization</span></span> | <span data-ttu-id="f155c-124">string</span><span class="sxs-lookup"><span data-stu-id="f155c-124">string</span></span> | <span data-ttu-id="f155c-125">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="f155c-125">Bearer \{token\}.</span></span> <span data-ttu-id="f155c-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="f155c-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f155c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f155c-127">Request body</span></span>
<span data-ttu-id="f155c-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f155c-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="f155c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f155c-129">Response</span></span>
<span data-ttu-id="f155c-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [contrato](../resources/agreement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f155c-130">If successful, this method returns a `200 OK` response code and collection of [agreement](../resources/agreement.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f155c-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f155c-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f155c-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f155c-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_agreements"
}-->
```http
GET https://graph.microsoft.com/beta/agreements
```
##### <a name="response"></a><span data-ttu-id="f155c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f155c-133">Response</span></span>
><span data-ttu-id="f155c-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f155c-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.agreement",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 146

{
  "value": [
    {
      "displayName": "displayName-value",
      "isViewingBeforeAcceptanceRequired": true,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List agreements",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
