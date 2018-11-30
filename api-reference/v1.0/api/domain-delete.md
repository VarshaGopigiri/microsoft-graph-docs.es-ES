---
title: Eliminar dominio
description: Elimina un dominio de un inquilino.
ms.openlocfilehash: e5d09eebb9c70ec0b9a172aac6b5f5ff7ecbfab7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029077"
---
# <a name="delete-domain"></a><span data-ttu-id="d2036-103">Eliminar dominio</span><span class="sxs-lookup"><span data-stu-id="d2036-103">Delete domain</span></span>

<span data-ttu-id="d2036-104">Elimina un dominio de un inquilino.</span><span class="sxs-lookup"><span data-stu-id="d2036-104">Deletes a domain from a tenant.</span></span>

> <span data-ttu-id="d2036-105">**Importante:**</span><span class="sxs-lookup"><span data-stu-id="d2036-105">**Important:**</span></span>
> - <span data-ttu-id="d2036-106">Los dominios eliminados no son recuperables.</span><span class="sxs-lookup"><span data-stu-id="d2036-106">Deleted domains are not recoverable.</span></span><br />
> - <span data-ttu-id="d2036-p101">Los intentos de eliminar el dominio fallarán si hay recursos u objetos que aún dependen de este. Encontrará todos los recursos dependientes mediante el uso de la API [Enumerar domainNameReferences](domain-list-domainnamereferences.md).</span><span class="sxs-lookup"><span data-stu-id="d2036-p101">Attempts to delete will fail if there are any resources or objects still dependent on the domain. You can find all dependent resources by using the [List domainNameReferences](domain-list-domainnamereferences.md) API.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2036-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2036-109">Permissions</span></span>

<span data-ttu-id="d2036-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2036-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="d2036-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2036-112">Permission type</span></span>      | <span data-ttu-id="d2036-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2036-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2036-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2036-114">Delegated (work or school account)</span></span> | <span data-ttu-id="d2036-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d2036-115">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d2036-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2036-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2036-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2036-117">Not supported.</span></span>    |
|<span data-ttu-id="d2036-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2036-118">Application</span></span> | <span data-ttu-id="d2036-119">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2036-119">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2036-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2036-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /domains/{id}
```

> <span data-ttu-id="d2036-121">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="d2036-121">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d2036-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2036-122">Request headers</span></span>

| <span data-ttu-id="d2036-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2036-123">Name</span></span>       | <span data-ttu-id="d2036-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2036-124">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d2036-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2036-125">Authorization</span></span>  | <span data-ttu-id="d2036-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2036-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d2036-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d2036-128">Content-Type</span></span>  | <span data-ttu-id="d2036-129">application/json</span><span class="sxs-lookup"><span data-stu-id="d2036-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d2036-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2036-130">Request body</span></span>

<span data-ttu-id="d2036-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2036-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2036-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2036-132">Response</span></span>

<span data-ttu-id="d2036-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2036-p104">If successful, this method returns `204 No Content` response code. It does not return a response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2036-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2036-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d2036-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2036-136">Request</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["contoso.com"],
  "name": "delete_domain"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/domains/contoso.com
```

##### <a name="response"></a><span data-ttu-id="d2036-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2036-137">Response</span></span>

<span data-ttu-id="d2036-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2036-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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