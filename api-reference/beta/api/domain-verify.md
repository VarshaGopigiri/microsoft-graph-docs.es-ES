---
title: 'dominio: verify'
description: Valide la propiedad del dominio.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 4948f2dc833db80c2cbc3f3b8aa7c487b7bb97aa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864704"
---
# <a name="domain-verify"></a><span data-ttu-id="e9d87-103">dominio: verify</span><span class="sxs-lookup"><span data-stu-id="e9d87-103">domain: verify</span></span>

> <span data-ttu-id="e9d87-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9d87-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9d87-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9d87-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e9d87-106">Valide la propiedad del dominio.</span><span class="sxs-lookup"><span data-stu-id="e9d87-106">Validates the ownership of the domain.</span></span>

> <span data-ttu-id="e9d87-p102">**Importante:** Solo se aplica a un dominio sin verificar. En el caso de un dominio sin verificar, la propiedad isVerified del [dominio](../resources/domain.md) es falsa.</span><span class="sxs-lookup"><span data-stu-id="e9d87-p102">**Important:** Only applies to an unverified domain. For an unverified domain, the isVerified property of the [domain](../resources/domain.md) is false.</span></span>

## <a name="permissions"></a><span data-ttu-id="e9d87-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="e9d87-109">Permissions</span></span>

<span data-ttu-id="e9d87-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9d87-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="e9d87-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9d87-112">Permission type</span></span>      | <span data-ttu-id="e9d87-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9d87-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e9d87-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9d87-114">Delegated (work or school account)</span></span> | <span data-ttu-id="e9d87-115">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9d87-115">Directory.Read.All</span></span>    |
|<span data-ttu-id="e9d87-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9d87-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e9d87-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9d87-117">Not supported.</span></span>    |
|<span data-ttu-id="e9d87-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9d87-118">Application</span></span> | <span data-ttu-id="e9d87-119">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9d87-119">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e9d87-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9d87-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains/{id}/verify
```

> <span data-ttu-id="e9d87-121">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="e9d87-121">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e9d87-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9d87-122">Request headers</span></span>

| <span data-ttu-id="e9d87-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9d87-123">Name</span></span>       | <span data-ttu-id="e9d87-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9d87-124">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e9d87-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9d87-125">Authorization</span></span>  | <span data-ttu-id="e9d87-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9d87-p104">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="e9d87-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e9d87-128">Content-Type</span></span>  | <span data-ttu-id="e9d87-129">application/json</span><span class="sxs-lookup"><span data-stu-id="e9d87-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="e9d87-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9d87-130">Request body</span></span>

## <a name="response"></a><span data-ttu-id="e9d87-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9d87-131">Response</span></span>

<span data-ttu-id="e9d87-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9d87-132">If successful, this method returns `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9d87-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9d87-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e9d87-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9d87-134">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "domain_verify"
}-->
```http
POST https://graph.microsoft.com/beta/domains/contoso.com/verify
```

##### <a name="response"></a><span data-ttu-id="e9d87-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9d87-135">Response</span></span>
<span data-ttu-id="e9d87-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9d87-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "name": "contoso.com"
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
