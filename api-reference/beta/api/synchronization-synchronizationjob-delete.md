---
title: Eliminar synchronizationJob
description: Detener el trabajo de sincronización y eliminar de forma permanente todos los Estados asociados con ella. Sincronizadas cuentas se dejan como-es.
ms.openlocfilehash: d77101e8dfaf55a36dfd7260afb30aade81bbae8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089567"
---
# <a name="delete-synchronizationjob"></a><span data-ttu-id="d6f79-104">Eliminar synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="d6f79-104">Delete synchronizationJob</span></span>

> <span data-ttu-id="d6f79-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d6f79-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d6f79-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d6f79-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d6f79-107">Detener el trabajo de sincronización y eliminar de forma permanente todos los Estados asociados con ella.</span><span class="sxs-lookup"><span data-stu-id="d6f79-107">Stop the synchronization job, and permanently delete all the state associated with it.</span></span> <span data-ttu-id="d6f79-108">Sincronizadas cuentas se dejan como-es.</span><span class="sxs-lookup"><span data-stu-id="d6f79-108">Synchronized accounts are left as-is.</span></span>

## <a name="permissions"></a><span data-ttu-id="d6f79-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="d6f79-109">Permissions</span></span>
<span data-ttu-id="d6f79-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6f79-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d6f79-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6f79-112">Permission type</span></span>                        | <span data-ttu-id="d6f79-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6f79-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6f79-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6f79-114">Delegated (work or school account)</span></span>     |<span data-ttu-id="d6f79-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6f79-115">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="d6f79-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6f79-116">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="d6f79-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6f79-117">Not supported.</span></span>  |
|<span data-ttu-id="d6f79-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6f79-118">Application</span></span>                            |<span data-ttu-id="d6f79-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6f79-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="d6f79-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6f79-120">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /servicePrincipals/{id}/synchronization/jobs/{jobId}/
```

## <a name="request-headers"></a><span data-ttu-id="d6f79-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6f79-121">Request headers</span></span>

| <span data-ttu-id="d6f79-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="d6f79-122">Name</span></span>           | <span data-ttu-id="d6f79-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f79-123">Type</span></span>    | <span data-ttu-id="d6f79-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6f79-124">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="d6f79-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6f79-125">Authorization</span></span>  | <span data-ttu-id="d6f79-126">string</span><span class="sxs-lookup"><span data-stu-id="d6f79-126">string</span></span>  | <span data-ttu-id="d6f79-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6f79-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d6f79-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6f79-129">Request body</span></span>

<span data-ttu-id="d6f79-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d6f79-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d6f79-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6f79-131">Response</span></span>

<span data-ttu-id="d6f79-132">Si se realiza correctamente, devuelve un `204 No Content` respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6f79-132">If successful, returns a `204 No Content` response.</span></span> <span data-ttu-id="d6f79-133">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6f79-133">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6f79-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6f79-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d6f79-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6f79-135">Request</span></span>
<span data-ttu-id="d6f79-136">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6f79-136">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_synchronizationjob"
}-->
```http
DELETE https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/
```

##### <a name="response"></a><span data-ttu-id="d6f79-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6f79-137">Response</span></span>
<span data-ttu-id="d6f79-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6f79-138">The following is an example of the response.</span></span> 

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
  "description": "Delete synchronizationJob",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->