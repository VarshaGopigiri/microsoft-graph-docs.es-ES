---
title: Obtener dominio
description: Recupere las propiedades y las relaciones del objeto domain.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 8086887652412c88372871a5a8d6914372e3f83f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955390"
---
# <a name="get-domain"></a><span data-ttu-id="f0ab2-103">Obtener dominio</span><span class="sxs-lookup"><span data-stu-id="f0ab2-103">Get domain</span></span>

> <span data-ttu-id="f0ab2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f0ab2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f0ab2-106">Recupere las propiedades y las relaciones del objeto domain.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-106">Retrieve the properties and relationships of domain object.</span></span>

## <a name="permissions"></a><span data-ttu-id="f0ab2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f0ab2-107">Permissions</span></span>

<span data-ttu-id="f0ab2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f0ab2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="f0ab2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0ab2-110">Permission type</span></span>      | <span data-ttu-id="f0ab2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0ab2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f0ab2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0ab2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f0ab2-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="f0ab2-113">Directory.Read.All</span></span>    |
|<span data-ttu-id="f0ab2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0ab2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f0ab2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-115">Not supported.</span></span>    |
|<span data-ttu-id="f0ab2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0ab2-116">Application</span></span> | <span data-ttu-id="f0ab2-117">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0ab2-117">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f0ab2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0ab2-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}
```

> <span data-ttu-id="f0ab2-119">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-119">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="f0ab2-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f0ab2-120">Optional query parameters</span></span>

<span data-ttu-id="f0ab2-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f0ab2-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0ab2-122">Request headers</span></span>

| <span data-ttu-id="f0ab2-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="f0ab2-123">Name</span></span>      |<span data-ttu-id="f0ab2-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0ab2-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f0ab2-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="f0ab2-125">Authorization</span></span>  | <span data-ttu-id="f0ab2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f0ab2-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f0ab2-128">Content-Type</span></span>  | <span data-ttu-id="f0ab2-129">application/json</span><span class="sxs-lookup"><span data-stu-id="f0ab2-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f0ab2-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0ab2-130">Request body</span></span>
<span data-ttu-id="f0ab2-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f0ab2-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0ab2-132">Response</span></span>

<span data-ttu-id="f0ab2-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-133">If successful, this method returns a `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f0ab2-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0ab2-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f0ab2-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0ab2-135">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domain"
}-->
```http
GET https://graph.microsoft.com/beta/domains/contoso.com
```
##### <a name="response"></a><span data-ttu-id="f0ab2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0ab2-136">Response</span></span>
<span data-ttu-id="f0ab2-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f0ab2-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
