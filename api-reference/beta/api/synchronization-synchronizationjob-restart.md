---
title: Reiniciar synchronizationJob
description: Reinicie el trabajo de sincronización, forzando que se va a procesar todos los objetos en el directorio. Borra, opcionalmente, el estado de sincronización existente y errores anteriores.
localization_priority: Normal
ms.openlocfilehash: 154ae4234eea6fb3499d36720e71b40cac727f9c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841030"
---
# <a name="restart-synchronizationjob"></a><span data-ttu-id="6e8cc-104">Reiniciar synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="6e8cc-104">Restart synchronizationJob</span></span>

> <span data-ttu-id="6e8cc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e8cc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6e8cc-107">Reinicie el trabajo de sincronización, forzando que se va a procesar todos los objetos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-107">Restart the synchronization job, forcing it to reprocess all the objects in the directory.</span></span> <span data-ttu-id="6e8cc-108">Borra, opcionalmente, el estado de sincronización existente y errores anteriores.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-108">Optionally clears existing synchronization state and previous errors.</span></span>

## <a name="permissions"></a><span data-ttu-id="6e8cc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="6e8cc-109">Permissions</span></span>
<span data-ttu-id="6e8cc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e8cc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e8cc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e8cc-112">Permission type</span></span>                        | <span data-ttu-id="6e8cc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e8cc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="6e8cc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e8cc-114">Delegated (work or school account)</span></span>     |<span data-ttu-id="6e8cc-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e8cc-115">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="6e8cc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e8cc-116">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="6e8cc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-117">Not supported.</span></span> |
|<span data-ttu-id="6e8cc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e8cc-118">Application</span></span>                            |<span data-ttu-id="6e8cc-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-119">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="6e8cc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e8cc-120">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/restart
```

## <a name="request-headers"></a><span data-ttu-id="6e8cc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e8cc-121">Request headers</span></span>

| <span data-ttu-id="6e8cc-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="6e8cc-122">Name</span></span>           | <span data-ttu-id="6e8cc-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8cc-123">Type</span></span>    | <span data-ttu-id="6e8cc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e8cc-124">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="6e8cc-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="6e8cc-125">Authorization</span></span>  | <span data-ttu-id="6e8cc-126">string</span><span class="sxs-lookup"><span data-stu-id="6e8cc-126">string</span></span>  | <span data-ttu-id="6e8cc-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6e8cc-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e8cc-129">Request body</span></span>

<span data-ttu-id="6e8cc-130">En el cuerpo de la solicitud, proporcione un objeto JSON con el siguiente parámetro.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-130">In the request body, provide a JSON object with the following parameter.</span></span>

| <span data-ttu-id="6e8cc-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6e8cc-131">Parameter</span></span>     | <span data-ttu-id="6e8cc-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8cc-132">Type</span></span>      | <span data-ttu-id="6e8cc-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e8cc-133">Description</span></span>    |
|:--------------|:----------|:---------------|
|<span data-ttu-id="6e8cc-134">criterios</span><span class="sxs-lookup"><span data-stu-id="6e8cc-134">criteria</span></span>       |[<span data-ttu-id="6e8cc-135">synchronizationJobRestartCriteria</span><span class="sxs-lookup"><span data-stu-id="6e8cc-135">synchronizationJobRestartCriteria</span></span>](../resources/synchronization-synchronizationjobrestartcriteria.md) |<span data-ttu-id="6e8cc-136">Reinicie criterios</span><span class="sxs-lookup"><span data-stu-id="6e8cc-136">Restart criteria</span></span>|

## <a name="response"></a><span data-ttu-id="6e8cc-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e8cc-137">Response</span></span>

<span data-ttu-id="6e8cc-138">Si se realiza correctamente, devuelve un `204 No Content` respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-138">If successful, returns a `204 No Content` response.</span></span> <span data-ttu-id="6e8cc-139">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-139">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6e8cc-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e8cc-140">Example</span></span>

##### <a name="request"></a><span data-ttu-id="6e8cc-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e8cc-141">Request</span></span>
<span data-ttu-id="6e8cc-142">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-142">The following is an example of a request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="6e8cc-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e8cc-143">Response</span></span>
<span data-ttu-id="6e8cc-144">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e8cc-144">The following is an example of a response.</span></span>

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
