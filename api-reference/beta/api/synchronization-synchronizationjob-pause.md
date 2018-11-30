---
title: 'synchronizationJob: pausar'
description: Detener temporalmente la sincronización. Se conserva el progreso, incluido el estado de trabajo, y el trabajo continuará desde donde la dejó cuando se realiza una llamada de inicio.
ms.openlocfilehash: dd46f5760d7ddcfff1e254d7c000e1cd80304f07
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085649"
---
# <a name="synchronizationjob-pause"></a><span data-ttu-id="0b96b-104">synchronizationJob: pausar</span><span class="sxs-lookup"><span data-stu-id="0b96b-104">synchronizationJob: pause</span></span>

> <span data-ttu-id="0b96b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b96b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b96b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b96b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0b96b-107">Detener temporalmente la sincronización.</span><span class="sxs-lookup"><span data-stu-id="0b96b-107">Temporarily stop synchronization.</span></span> <span data-ttu-id="0b96b-108">Se conserva el progreso, incluido el estado de trabajo, y el trabajo continuará desde donde la dejó cuando se realiza una llamada de [Inicio](../api/synchronization-synchronizationjob-start.md) .</span><span class="sxs-lookup"><span data-stu-id="0b96b-108">All the progress, including job state, is persisted, and the job will continue from where it left off when a [Start](../api/synchronization-synchronizationjob-start.md) call is made.</span></span>

## <a name="permissions"></a><span data-ttu-id="0b96b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="0b96b-109">Permissions</span></span>
<span data-ttu-id="0b96b-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0b96b-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0b96b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0b96b-112">Permission type</span></span>                        | <span data-ttu-id="0b96b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0b96b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="0b96b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0b96b-114">Delegated (work or school account)</span></span>     |<span data-ttu-id="0b96b-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b96b-115">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="0b96b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0b96b-116">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="0b96b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b96b-117">Not supported.</span></span>  |
|<span data-ttu-id="0b96b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0b96b-118">Application</span></span>                            |<span data-ttu-id="0b96b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b96b-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="0b96b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b96b-120">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/pause
```

## <a name="request-headers"></a><span data-ttu-id="0b96b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b96b-121">Request headers</span></span>

| <span data-ttu-id="0b96b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="0b96b-122">Name</span></span>           | <span data-ttu-id="0b96b-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b96b-123">Type</span></span>    | <span data-ttu-id="0b96b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b96b-124">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="0b96b-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="0b96b-125">Authorization</span></span>  | <span data-ttu-id="0b96b-126">string</span><span class="sxs-lookup"><span data-stu-id="0b96b-126">string</span></span>  | <span data-ttu-id="0b96b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b96b-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0b96b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0b96b-129">Request body</span></span>

<span data-ttu-id="0b96b-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0b96b-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0b96b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b96b-131">Response</span></span>

<span data-ttu-id="0b96b-132">Si se realiza correctamente, devuelve un `204 No Content` respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b96b-132">If successful, returns a `204 No Content` response.</span></span> <span data-ttu-id="0b96b-133">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b96b-133">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0b96b-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b96b-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="0b96b-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0b96b-135">Request</span></span>
<span data-ttu-id="0b96b-136">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b96b-136">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationjob_pause"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/pause
```

##### <a name="response"></a><span data-ttu-id="0b96b-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b96b-137">Response</span></span>
<span data-ttu-id="0b96b-138">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b96b-138">The following is an example of a response.</span></span>
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