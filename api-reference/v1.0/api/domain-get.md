---
title: Obtener dominio
description: Recupere las propiedades y las relaciones del objeto domain.
ms.openlocfilehash: ab446db054d2bb8bdb6cd18ccb41879988e6d30c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029776"
---
# <a name="get-domain"></a><span data-ttu-id="a7bd8-103">Obtener dominio</span><span class="sxs-lookup"><span data-stu-id="a7bd8-103">Get domain</span></span>

<span data-ttu-id="a7bd8-104">Recupere las propiedades y las relaciones del objeto domain.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-104">Retrieve the properties and relationships of domain object.</span></span>

## <a name="permissions"></a><span data-ttu-id="a7bd8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7bd8-105">Permissions</span></span>

<span data-ttu-id="a7bd8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7bd8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a7bd8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7bd8-108">Permission type</span></span>      | <span data-ttu-id="a7bd8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7bd8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a7bd8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7bd8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a7bd8-111">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7bd8-111">Directory.Read.All</span></span>    |
|<span data-ttu-id="a7bd8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7bd8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7bd8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-113">Not supported.</span></span>    |
|<span data-ttu-id="a7bd8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7bd8-114">Application</span></span> | <span data-ttu-id="a7bd8-115">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a7bd8-115">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a7bd8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7bd8-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}
```

> <span data-ttu-id="a7bd8-117">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-117">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="a7bd8-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a7bd8-118">Optional query parameters</span></span>

<span data-ttu-id="a7bd8-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a7bd8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7bd8-120">Request headers</span></span>

| <span data-ttu-id="a7bd8-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7bd8-121">Name</span></span>      |<span data-ttu-id="a7bd8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bd8-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a7bd8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7bd8-123">Authorization</span></span>  | <span data-ttu-id="a7bd8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a7bd8-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a7bd8-126">Content-Type</span></span>  | <span data-ttu-id="a7bd8-127">application/json</span><span class="sxs-lookup"><span data-stu-id="a7bd8-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="a7bd8-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7bd8-128">Request body</span></span>
<span data-ttu-id="a7bd8-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a7bd8-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7bd8-130">Response</span></span>

<span data-ttu-id="a7bd8-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-131">If successful, this method returns a `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a7bd8-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7bd8-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a7bd8-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7bd8-133">Request</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["contoso.com"],
  "name": "get_domain"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains/contoso.com
```
##### <a name="response"></a><span data-ttu-id="a7bd8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7bd8-134">Response</span></span>
<span data-ttu-id="a7bd8-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7bd8-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 192

{
  "authenticationType": "authenticationType-value",
  "availabilityStatus": "availabilityStatus-value",
  "id": "contoso.com",
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->