---
title: Eliminar dominio
description: Elimina un dominio de un inquilino.
ms.openlocfilehash: 2ed3772d767099e8ccd7fd5453c7a8231c9ea96c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086554"
---
# <a name="delete-domain"></a><span data-ttu-id="2c1bc-103">Eliminar dominio</span><span class="sxs-lookup"><span data-stu-id="2c1bc-103">Delete domain</span></span>

> <span data-ttu-id="2c1bc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2c1bc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2c1bc-106">Elimina un dominio de un inquilino.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-106">Deletes a domain from a tenant.</span></span>

> <span data-ttu-id="2c1bc-107">**Importante:** Los dominios eliminados no son recuperables.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-107">**Important:** Deleted domains are not recoverable.</span></span>

## <a name="permissions"></a><span data-ttu-id="2c1bc-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c1bc-108">Permissions</span></span>

<span data-ttu-id="2c1bc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2c1bc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2c1bc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c1bc-111">Permission type</span></span>      | <span data-ttu-id="2c1bc-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c1bc-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2c1bc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c1bc-113">Delegated (work or school account)</span></span> | <span data-ttu-id="2c1bc-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2c1bc-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2c1bc-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c1bc-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2c1bc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-116">Not supported.</span></span>    |
|<span data-ttu-id="2c1bc-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c1bc-117">Application</span></span> | <span data-ttu-id="2c1bc-118">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2c1bc-118">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2c1bc-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c1bc-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /domains/{id}
```

> <span data-ttu-id="2c1bc-120">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-120">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2c1bc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c1bc-121">Request headers</span></span>

| <span data-ttu-id="2c1bc-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c1bc-122">Name</span></span>       | <span data-ttu-id="2c1bc-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c1bc-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2c1bc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c1bc-124">Authorization</span></span>  | <span data-ttu-id="2c1bc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2c1bc-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2c1bc-127">Content-Type</span></span>  | <span data-ttu-id="2c1bc-128">application/json</span><span class="sxs-lookup"><span data-stu-id="2c1bc-128">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="2c1bc-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c1bc-129">Request body</span></span>

<span data-ttu-id="2c1bc-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2c1bc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c1bc-131">Response</span></span>

<span data-ttu-id="2c1bc-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-p104">If successful, this method returns `204 No Content` response code. It does not return a response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c1bc-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c1bc-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2c1bc-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c1bc-135">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_domain"
}-->
```http
DELETE https://graph.microsoft.com/beta/domains/contoso.com
```

##### <a name="response"></a><span data-ttu-id="2c1bc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c1bc-136">Response</span></span>

<span data-ttu-id="2c1bc-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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