---
title: Eliminar dominio
description: Elimina un dominio de un inquilino.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: a870692e6a2710728dac4f2df55aaf8daf0eb95a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960129"
---
# <a name="delete-domain"></a><span data-ttu-id="cbd2c-103">Eliminar dominio</span><span class="sxs-lookup"><span data-stu-id="cbd2c-103">Delete domain</span></span>

> <span data-ttu-id="cbd2c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cbd2c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cbd2c-106">Elimina un dominio de un inquilino.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-106">Deletes a domain from a tenant.</span></span>

> <span data-ttu-id="cbd2c-107">**Importante:** Los dominios eliminados no son recuperables.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-107">**Important:** Deleted domains are not recoverable.</span></span>

## <a name="permissions"></a><span data-ttu-id="cbd2c-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="cbd2c-108">Permissions</span></span>

<span data-ttu-id="cbd2c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cbd2c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="cbd2c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cbd2c-111">Permission type</span></span>      | <span data-ttu-id="cbd2c-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cbd2c-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cbd2c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cbd2c-113">Delegated (work or school account)</span></span> | <span data-ttu-id="cbd2c-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cbd2c-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cbd2c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cbd2c-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cbd2c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-116">Not supported.</span></span>    |
|<span data-ttu-id="cbd2c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cbd2c-117">Application</span></span> | <span data-ttu-id="cbd2c-118">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cbd2c-118">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cbd2c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cbd2c-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /domains/{id}
```

> <span data-ttu-id="cbd2c-120">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-120">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cbd2c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cbd2c-121">Request headers</span></span>

| <span data-ttu-id="cbd2c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="cbd2c-122">Name</span></span>       | <span data-ttu-id="cbd2c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbd2c-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="cbd2c-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="cbd2c-124">Authorization</span></span>  | <span data-ttu-id="cbd2c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cbd2c-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cbd2c-127">Content-Type</span></span>  | <span data-ttu-id="cbd2c-128">application/json</span><span class="sxs-lookup"><span data-stu-id="cbd2c-128">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="cbd2c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cbd2c-129">Request body</span></span>

<span data-ttu-id="cbd2c-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cbd2c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbd2c-131">Response</span></span>

<span data-ttu-id="cbd2c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-p104">If successful, this method returns `204 No Content` response code. It does not return a response body.</span></span>

## <a name="example"></a><span data-ttu-id="cbd2c-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbd2c-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cbd2c-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cbd2c-135">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_domain"
}-->
```http
DELETE https://graph.microsoft.com/beta/domains/contoso.com
```

##### <a name="response"></a><span data-ttu-id="cbd2c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbd2c-136">Response</span></span>

<span data-ttu-id="cbd2c-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
