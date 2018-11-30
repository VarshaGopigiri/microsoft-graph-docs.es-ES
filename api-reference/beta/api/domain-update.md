---
title: Actualizar dominio
description: Actualiza las propiedades del objeto del dominio.
ms.openlocfilehash: 38a4baca42b22465ba2ea98081b7619d5f8af0e1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085887"
---
# <a name="update-domain"></a><span data-ttu-id="4a4cb-103">Actualizar dominio</span><span class="sxs-lookup"><span data-stu-id="4a4cb-103">Update domain</span></span>

> <span data-ttu-id="4a4cb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a4cb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4a4cb-106">Actualiza las propiedades del objeto del dominio.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-106">Update the properties of domain object.</span></span>

> <span data-ttu-id="4a4cb-107">**Importante:** Solo se pueden actualizar los dominios verificados.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-107">**Important:** Only verified domains can be updated.</span></span>

## <a name="permissions"></a><span data-ttu-id="4a4cb-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a4cb-108">Permissions</span></span>

<span data-ttu-id="4a4cb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4a4cb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4a4cb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a4cb-111">Permission type</span></span>      | <span data-ttu-id="4a4cb-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a4cb-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a4cb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a4cb-113">Delegated (work or school account)</span></span> | <span data-ttu-id="4a4cb-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4a4cb-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4a4cb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a4cb-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a4cb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-116">Not supported.</span></span>    |
|<span data-ttu-id="4a4cb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a4cb-117">Application</span></span> | <span data-ttu-id="4a4cb-118">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a4cb-118">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4a4cb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a4cb-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /domains/{id}
```

> <span data-ttu-id="4a4cb-120">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-120">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4a4cb-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a4cb-121">Request headers</span></span>

| <span data-ttu-id="4a4cb-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a4cb-122">Name</span></span>       | <span data-ttu-id="4a4cb-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a4cb-123">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="4a4cb-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="4a4cb-124">Authorization</span></span>  | <span data-ttu-id="4a4cb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4a4cb-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4a4cb-127">Content-Type</span></span>  | <span data-ttu-id="4a4cb-128">application/json</span><span class="sxs-lookup"><span data-stu-id="4a4cb-128">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="4a4cb-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a4cb-129">Request body</span></span>

<span data-ttu-id="4a4cb-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que quiera actualizar. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud conservarán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para un rendimiento óptimo, incluya solo los valores modificados.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-p104">In the request body, supply the values for relevant fields to be updated. Existing properties not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, only include changed values.</span></span>

## <a name="response"></a><span data-ttu-id="4a4cb-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a4cb-133">Response</span></span>

<span data-ttu-id="4a4cb-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`, pero no el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a4cb-134">If successful, this method returns a `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="4a4cb-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a4cb-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4a4cb-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a4cb-136">Request</span></span>

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

##### <a name="response"></a><span data-ttu-id="4a4cb-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a4cb-137">Response</span></span>

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