---
title: 'dominio: verify'
description: Valide la propiedad del dominio.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 359a266acf854e4353bce4eda0f65191ca2783c7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814836"
---
# <a name="domain-verify"></a><span data-ttu-id="4f520-103">dominio: verify</span><span class="sxs-lookup"><span data-stu-id="4f520-103">domain: verify</span></span>

<span data-ttu-id="4f520-104">Valide la propiedad del dominio.</span><span class="sxs-lookup"><span data-stu-id="4f520-104">Validates the ownership of the domain.</span></span>

> <span data-ttu-id="4f520-p101">**Importante:** Solo se aplica a un dominio sin verificar. En el caso de un dominio sin verificar, la propiedad isVerified del [dominio](../resources/domain.md) es falsa.</span><span class="sxs-lookup"><span data-stu-id="4f520-p101">**Important:** Only applies to an unverified domain. For an unverified domain, the isVerified property of the [domain](../resources/domain.md) is false.</span></span>

## <a name="permissions"></a><span data-ttu-id="4f520-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4f520-107">Permissions</span></span>

<span data-ttu-id="4f520-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4f520-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4f520-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f520-110">Permission type</span></span>      | <span data-ttu-id="4f520-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f520-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4f520-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f520-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4f520-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="4f520-113">Directory.Read.All</span></span>    |
|<span data-ttu-id="4f520-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f520-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4f520-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f520-115">Not supported.</span></span>    |
|<span data-ttu-id="4f520-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f520-116">Application</span></span> | <span data-ttu-id="4f520-117">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4f520-117">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4f520-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f520-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains/{id}/verify
```

> <span data-ttu-id="4f520-119">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="4f520-119">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4f520-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f520-120">Request headers</span></span>

| <span data-ttu-id="4f520-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f520-121">Name</span></span>       | <span data-ttu-id="4f520-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f520-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4f520-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4f520-123">Authorization</span></span>  | <span data-ttu-id="4f520-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f520-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="4f520-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4f520-126">Content-Type</span></span>  | <span data-ttu-id="4f520-127">application/json</span><span class="sxs-lookup"><span data-stu-id="4f520-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="4f520-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f520-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="4f520-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f520-129">Response</span></span>

<span data-ttu-id="4f520-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f520-130">If successful, this method returns `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f520-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f520-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4f520-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f520-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "domain_verify"
}-->
```http
POST https://graph.microsoft.com/v1.0/domains/{domain-name}/verify
```

##### <a name="response"></a><span data-ttu-id="4f520-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f520-133">Response</span></span>
<span data-ttu-id="4f520-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f520-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true,
  "id": "contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domain: verify",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
