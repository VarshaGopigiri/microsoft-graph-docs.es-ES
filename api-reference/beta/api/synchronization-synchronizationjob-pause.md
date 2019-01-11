---
title: 'synchronizationJob: pausar'
description: Detener temporalmente la sincronización. Se conserva el progreso, incluido el estado de trabajo, y el trabajo continuará desde donde la dejó cuando se realiza una llamada de inicio.
localization_priority: Normal
ms.openlocfilehash: f39b3a700b31169ea15f089da8873b517b50dc15
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804882"
---
# <a name="synchronizationjob-pause"></a><span data-ttu-id="1e53e-104">synchronizationJob: pausar</span><span class="sxs-lookup"><span data-stu-id="1e53e-104">synchronizationJob: pause</span></span>

> <span data-ttu-id="1e53e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e53e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e53e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e53e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1e53e-107">Detener temporalmente la sincronización.</span><span class="sxs-lookup"><span data-stu-id="1e53e-107">Temporarily stop synchronization.</span></span> <span data-ttu-id="1e53e-108">Se conserva el progreso, incluido el estado de trabajo, y el trabajo continuará desde donde la dejó cuando se realiza una llamada de [Inicio](../api/synchronization-synchronizationjob-start.md) .</span><span class="sxs-lookup"><span data-stu-id="1e53e-108">All the progress, including job state, is persisted, and the job will continue from where it left off when a [Start](../api/synchronization-synchronizationjob-start.md) call is made.</span></span>

## <a name="permissions"></a><span data-ttu-id="1e53e-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="1e53e-109">Permissions</span></span>
<span data-ttu-id="1e53e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1e53e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1e53e-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e53e-112">Permission type</span></span>                        | <span data-ttu-id="1e53e-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e53e-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="1e53e-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e53e-114">Delegated (work or school account)</span></span>     |<span data-ttu-id="1e53e-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1e53e-115">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="1e53e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e53e-116">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="1e53e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e53e-117">Not supported.</span></span>  |
|<span data-ttu-id="1e53e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e53e-118">Application</span></span>                            |<span data-ttu-id="1e53e-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e53e-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1e53e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e53e-120">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/pause
```

## <a name="request-headers"></a><span data-ttu-id="1e53e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1e53e-121">Request headers</span></span>

| <span data-ttu-id="1e53e-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e53e-122">Name</span></span>           | <span data-ttu-id="1e53e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e53e-123">Type</span></span>    | <span data-ttu-id="1e53e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e53e-124">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="1e53e-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="1e53e-125">Authorization</span></span>  | <span data-ttu-id="1e53e-126">string</span><span class="sxs-lookup"><span data-stu-id="1e53e-126">string</span></span>  | <span data-ttu-id="1e53e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e53e-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1e53e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1e53e-129">Request body</span></span>

<span data-ttu-id="1e53e-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1e53e-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1e53e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e53e-131">Response</span></span>

<span data-ttu-id="1e53e-132">Si se realiza correctamente, devuelve un `204 No Content` respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e53e-132">If successful, returns a `204 No Content` response.</span></span> <span data-ttu-id="1e53e-133">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e53e-133">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1e53e-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e53e-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1e53e-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e53e-135">Request</span></span>
<span data-ttu-id="1e53e-136">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e53e-136">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationjob_pause"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/pause
```

##### <a name="response"></a><span data-ttu-id="1e53e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e53e-137">Response</span></span>
<span data-ttu-id="1e53e-138">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e53e-138">The following is an example of a response.</span></span>
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
  "description": "synchronizationJob: pause",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
