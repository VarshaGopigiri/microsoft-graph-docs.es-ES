---
title: Reiniciar synchronizationJob
description: Reinicie el trabajo de sincronización, forzando que se va a procesar todos los objetos en el directorio. Borra, opcionalmente, el estado de sincronización existente y errores anteriores.
ms.openlocfilehash: 0b7ebfcd7b13400225d9ea149442207ecd994a8d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089386"
---
# <a name="restart-synchronizationjob"></a><span data-ttu-id="0cdc9-104">Reiniciar synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="0cdc9-104">Restart synchronizationJob</span></span>

> <span data-ttu-id="0cdc9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0cdc9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0cdc9-107">Reinicie el trabajo de sincronización, forzando que se va a procesar todos los objetos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-107">Restart the synchronization job, forcing it to reprocess all the objects in the directory.</span></span> <span data-ttu-id="0cdc9-108">Borra, opcionalmente, el estado de sincronización existente y errores anteriores.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-108">Optionally clears existing synchronization state and previous errors.</span></span>

## <a name="permissions"></a><span data-ttu-id="0cdc9-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="0cdc9-109">Permissions</span></span>
<span data-ttu-id="0cdc9-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0cdc9-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0cdc9-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0cdc9-112">Permission type</span></span>                        | <span data-ttu-id="0cdc9-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0cdc9-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="0cdc9-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0cdc9-114">Delegated (work or school account)</span></span>     |<span data-ttu-id="0cdc9-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0cdc9-115">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="0cdc9-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0cdc9-116">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="0cdc9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-117">Not supported.</span></span> |
|<span data-ttu-id="0cdc9-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0cdc9-118">Application</span></span>                            |<span data-ttu-id="0cdc9-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-119">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="0cdc9-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0cdc9-120">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/restart
```

## <a name="request-headers"></a><span data-ttu-id="0cdc9-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0cdc9-121">Request headers</span></span>

| <span data-ttu-id="0cdc9-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="0cdc9-122">Name</span></span>           | <span data-ttu-id="0cdc9-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cdc9-123">Type</span></span>    | <span data-ttu-id="0cdc9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cdc9-124">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="0cdc9-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="0cdc9-125">Authorization</span></span>  | <span data-ttu-id="0cdc9-126">string</span><span class="sxs-lookup"><span data-stu-id="0cdc9-126">string</span></span>  | <span data-ttu-id="0cdc9-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0cdc9-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0cdc9-129">Request body</span></span>

<span data-ttu-id="0cdc9-130">En el cuerpo de la solicitud, proporcione un objeto JSON con el siguiente parámetro.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-130">In the request body, provide a JSON object with the following parameter.</span></span>

| <span data-ttu-id="0cdc9-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0cdc9-131">Parameter</span></span>     | <span data-ttu-id="0cdc9-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cdc9-132">Type</span></span>      | <span data-ttu-id="0cdc9-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cdc9-133">Description</span></span>    |
|:--------------|:----------|:---------------|
|<span data-ttu-id="0cdc9-134">criterios</span><span class="sxs-lookup"><span data-stu-id="0cdc9-134">criteria</span></span>       |[<span data-ttu-id="0cdc9-135">synchronizationJobRestartCriteria</span><span class="sxs-lookup"><span data-stu-id="0cdc9-135">synchronizationJobRestartCriteria</span></span>](../resources/synchronization-synchronizationjobrestartcriteria.md) |<span data-ttu-id="0cdc9-136">Reinicie criterios</span><span class="sxs-lookup"><span data-stu-id="0cdc9-136">Restart criteria</span></span>|

## <a name="response"></a><span data-ttu-id="0cdc9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cdc9-137">Response</span></span>

<span data-ttu-id="0cdc9-138">Si se realiza correctamente, devuelve un `204 No Content` respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-138">If successful, returns a `204 No Content` response.</span></span> <span data-ttu-id="0cdc9-139">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-139">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0cdc9-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0cdc9-140">Example</span></span>

##### <a name="request"></a><span data-ttu-id="0cdc9-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0cdc9-141">Request</span></span>
<span data-ttu-id="0cdc9-142">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-142">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationjob_restart"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/restart
Authorization: Bearer <token>
Content-type: application/json

{
   "criteria": {
       "resetScope": "ConnectorDataStore, Escrows, QuarantineState"
   }
}
```

##### <a name="response"></a><span data-ttu-id="0cdc9-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cdc9-143">Response</span></span>
<span data-ttu-id="0cdc9-144">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cdc9-144">The following is an example of a response.</span></span>

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
  "description": "synchronizationJob: restart",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
