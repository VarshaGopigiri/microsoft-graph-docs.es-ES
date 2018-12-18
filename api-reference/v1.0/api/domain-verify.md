---
title: 'dominio: verify'
description: Valide la propiedad del dominio.
author: lleonard-msft
ms.openlocfilehash: f6a8019d9530691e32ca8a8347d6fe8ff2ac15d2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328927"
---
# <a name="domain-verify"></a><span data-ttu-id="7d104-103">dominio: verify</span><span class="sxs-lookup"><span data-stu-id="7d104-103">domain: verify</span></span>

<span data-ttu-id="7d104-104">Valide la propiedad del dominio.</span><span class="sxs-lookup"><span data-stu-id="7d104-104">Validates the ownership of the domain.</span></span>

> <span data-ttu-id="7d104-p101">**Importante:** Solo se aplica a un dominio sin verificar. En el caso de un dominio sin verificar, la propiedad isVerified del [dominio](../resources/domain.md) es falsa.</span><span class="sxs-lookup"><span data-stu-id="7d104-p101">**Important:** Only applies to an unverified domain. For an unverified domain, the isVerified property of the [domain](../resources/domain.md) is false.</span></span>

## <a name="permissions"></a><span data-ttu-id="7d104-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7d104-107">Permissions</span></span>

<span data-ttu-id="7d104-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d104-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="7d104-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d104-110">Permission type</span></span>      | <span data-ttu-id="7d104-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d104-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7d104-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d104-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7d104-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="7d104-113">Directory.Read.All</span></span>    |
|<span data-ttu-id="7d104-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d104-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7d104-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7d104-115">Not supported.</span></span>    |
|<span data-ttu-id="7d104-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d104-116">Application</span></span> | <span data-ttu-id="7d104-117">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d104-117">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7d104-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d104-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains/{id}/verify
```

> <span data-ttu-id="7d104-119">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="7d104-119">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7d104-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d104-120">Request headers</span></span>

| <span data-ttu-id="7d104-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d104-121">Name</span></span>       | <span data-ttu-id="7d104-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d104-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7d104-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7d104-123">Authorization</span></span>  | <span data-ttu-id="7d104-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d104-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="7d104-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7d104-126">Content-Type</span></span>  | <span data-ttu-id="7d104-127">application/json</span><span class="sxs-lookup"><span data-stu-id="7d104-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="7d104-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d104-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="7d104-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d104-129">Response</span></span>

<span data-ttu-id="7d104-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d104-130">If successful, this method returns `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7d104-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d104-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7d104-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d104-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "domain_verify"
}-->
```http
POST https://graph.microsoft.com/v1.0/domains/{domain-name}/verify
```

##### <a name="response"></a><span data-ttu-id="7d104-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d104-133">Response</span></span>
<span data-ttu-id="7d104-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7d104-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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