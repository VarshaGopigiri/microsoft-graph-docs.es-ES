---
title: Iniciar synchronizationJob
description: Iniciar un trabajo de sincronización existente. Si el trabajo está en un estado en pausa, continuará procesar los cambios desde el punto donde se pausó. Si el trabajo está en cuarentena, se borrará el estado de la cuarentena.
ms.openlocfilehash: c9f326a2c00564f25fb0ff982ede7e8454e14c8c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090036"
---
# <a name="start-synchronizationjob"></a><span data-ttu-id="ad00d-105">Iniciar synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="ad00d-105">Start synchronizationJob</span></span>

> <span data-ttu-id="ad00d-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad00d-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad00d-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad00d-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ad00d-108">Iniciar un trabajo de sincronización existente.</span><span class="sxs-lookup"><span data-stu-id="ad00d-108">Start an existing synchronization job.</span></span> <span data-ttu-id="ad00d-109">Si el trabajo está en un estado en pausa, continuará procesar los cambios desde el punto donde se pausó.</span><span class="sxs-lookup"><span data-stu-id="ad00d-109">If the job is in a paused state, it will continue processing changes from the point where it was paused.</span></span> <span data-ttu-id="ad00d-110">Si el trabajo está en cuarentena, se borrará el estado de la cuarentena.</span><span class="sxs-lookup"><span data-stu-id="ad00d-110">If the job is in quarantine, the quarantine status will be cleared.</span></span>

## <a name="permissions"></a><span data-ttu-id="ad00d-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="ad00d-111">Permissions</span></span>
<span data-ttu-id="ad00d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad00d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad00d-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad00d-114">Permission type</span></span>                        | <span data-ttu-id="ad00d-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad00d-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="ad00d-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad00d-116">Delegated (work or school account)</span></span>     |<span data-ttu-id="ad00d-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ad00d-117">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="ad00d-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad00d-118">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="ad00d-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad00d-119">Not supported.</span></span> |
|<span data-ttu-id="ad00d-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad00d-120">Application</span></span>                            |<span data-ttu-id="ad00d-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad00d-121">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ad00d-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad00d-122">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/start
```

## <a name="request-headers"></a><span data-ttu-id="ad00d-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad00d-123">Request headers</span></span>

| <span data-ttu-id="ad00d-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad00d-124">Name</span></span>           | <span data-ttu-id="ad00d-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad00d-125">Type</span></span>    | <span data-ttu-id="ad00d-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad00d-126">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="ad00d-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad00d-127">Authorization</span></span>  | <span data-ttu-id="ad00d-128">string</span><span class="sxs-lookup"><span data-stu-id="ad00d-128">string</span></span>  | <span data-ttu-id="ad00d-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad00d-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ad00d-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad00d-131">Request body</span></span>

<span data-ttu-id="ad00d-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ad00d-132">Do not supply a request body for this method.</span></span> 

## <a name="response"></a><span data-ttu-id="ad00d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad00d-133">Response</span></span>

<span data-ttu-id="ad00d-134">Si se realiza correctamente, devuelve un `204 No Content` respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad00d-134">If successful, returns a `204 No Content` response.</span></span> <span data-ttu-id="ad00d-135">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad00d-135">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ad00d-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad00d-136">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ad00d-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad00d-137">Request</span></span>
<span data-ttu-id="ad00d-138">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad00d-138">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationjob_start"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/start
```

##### <a name="response"></a><span data-ttu-id="ad00d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad00d-139">Response</span></span>
<span data-ttu-id="ad00d-140">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad00d-140">The following is an example of a response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationJob: start",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
