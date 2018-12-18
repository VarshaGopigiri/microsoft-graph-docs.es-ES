---
title: Actualizar dominio
description: Actualiza las propiedades del objeto del dominio.
author: lleonard-msft
ms.openlocfilehash: ebb58ac0c1daa23d7c8c8eb08743d3856798a4ae
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361442"
---
# <a name="update-domain"></a><span data-ttu-id="e5579-103">Actualizar dominio</span><span class="sxs-lookup"><span data-stu-id="e5579-103">Update domain</span></span>

> <span data-ttu-id="e5579-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5579-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5579-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5579-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5579-106">Actualiza las propiedades del objeto del dominio.</span><span class="sxs-lookup"><span data-stu-id="e5579-106">Update the properties of domain object.</span></span>

> <span data-ttu-id="e5579-107">**Importante:** Solo se pueden actualizar los dominios verificados.</span><span class="sxs-lookup"><span data-stu-id="e5579-107">**Important:** Only verified domains can be updated.</span></span>

## <a name="permissions"></a><span data-ttu-id="e5579-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5579-108">Permissions</span></span>

<span data-ttu-id="e5579-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5579-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="e5579-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5579-111">Permission type</span></span>      | <span data-ttu-id="e5579-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5579-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5579-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5579-113">Delegated (work or school account)</span></span> | <span data-ttu-id="e5579-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e5579-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="e5579-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5579-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5579-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5579-116">Not supported.</span></span>    |
|<span data-ttu-id="e5579-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5579-117">Application</span></span> | <span data-ttu-id="e5579-118">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e5579-118">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e5579-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5579-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /domains/{id}
```

> <span data-ttu-id="e5579-120">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="e5579-120">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e5579-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5579-121">Request headers</span></span>

| <span data-ttu-id="e5579-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5579-122">Name</span></span>       | <span data-ttu-id="e5579-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5579-123">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="e5579-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5579-124">Authorization</span></span>  | <span data-ttu-id="e5579-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5579-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e5579-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e5579-127">Content-Type</span></span>  | <span data-ttu-id="e5579-128">application/json</span><span class="sxs-lookup"><span data-stu-id="e5579-128">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="e5579-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5579-129">Request body</span></span>

<span data-ttu-id="e5579-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que quiera actualizar. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud conservarán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para un rendimiento óptimo, incluya solo los valores modificados.</span><span class="sxs-lookup"><span data-stu-id="e5579-p104">In the request body, supply the values for relevant fields to be updated. Existing properties not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, only include changed values.</span></span>

## <a name="response"></a><span data-ttu-id="e5579-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5579-133">Response</span></span>

<span data-ttu-id="e5579-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`, pero no el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5579-134">If successful, this method returns a `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="e5579-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5579-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e5579-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5579-136">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_domain"
}-->
```http
PATCH https://graph.microsoft.com/beta/domains/contoso.com
Content-type: application/json

{
  "isDefault": true,
  "supportedServices": [
    "Email",
    "OfficeCommunicationsOnline"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="e5579-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5579-137">Response</span></span>

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