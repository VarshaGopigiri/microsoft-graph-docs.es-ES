---
title: Actualizar dominio
description: Actualiza las propiedades del objeto del dominio.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: da51badb52b5047c6d5eb1d52004104d0395fcf2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923785"
---
# <a name="update-domain"></a><span data-ttu-id="92633-103">Actualizar dominio</span><span class="sxs-lookup"><span data-stu-id="92633-103">Update domain</span></span>

<span data-ttu-id="92633-104">Actualiza las propiedades del objeto del dominio.</span><span class="sxs-lookup"><span data-stu-id="92633-104">Update the properties of domain object.</span></span>

> <span data-ttu-id="92633-105">**Importante:** Solo se pueden actualizar los dominios verificados.</span><span class="sxs-lookup"><span data-stu-id="92633-105">**Important:** Only verified domains can be updated.</span></span>

## <a name="permissions"></a><span data-ttu-id="92633-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="92633-106">Permissions</span></span>

<span data-ttu-id="92633-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="92633-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="92633-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="92633-109">Permission type</span></span>      | <span data-ttu-id="92633-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="92633-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="92633-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="92633-111">Delegated (work or school account)</span></span> | <span data-ttu-id="92633-112">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="92633-112">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="92633-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="92633-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="92633-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="92633-114">Not supported.</span></span>    |
|<span data-ttu-id="92633-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="92633-115">Application</span></span> | <span data-ttu-id="92633-116">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="92633-116">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="92633-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="92633-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /domains/{id}
```

> <span data-ttu-id="92633-118">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="92633-118">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="92633-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="92633-119">Request headers</span></span>

| <span data-ttu-id="92633-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="92633-120">Name</span></span>       | <span data-ttu-id="92633-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="92633-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="92633-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="92633-122">Authorization</span></span>  | <span data-ttu-id="92633-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92633-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="92633-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="92633-125">Content-Type</span></span>  | <span data-ttu-id="92633-126">application/json</span><span class="sxs-lookup"><span data-stu-id="92633-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="92633-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="92633-127">Request body</span></span>

<span data-ttu-id="92633-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que quiera actualizar. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud conservarán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para un rendimiento óptimo, incluya solo los valores modificados.</span><span class="sxs-lookup"><span data-stu-id="92633-p103">In the request body, supply the values for relevant fields to be updated. Existing properties not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, only include changed values.</span></span>

## <a name="response"></a><span data-ttu-id="92633-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92633-131">Response</span></span>

<span data-ttu-id="92633-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`, pero no el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92633-132">If successful, this method returns a `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="92633-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="92633-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="92633-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="92633-134">Request</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["contoso.com"],
  "name": "update_domain"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/domains/contoso.com
Content-type: application/json

{
  "isDefault": true,
  "supportedServices": [
    "Email",
    "OfficeCommunicationsOnline"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="92633-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92633-135">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
