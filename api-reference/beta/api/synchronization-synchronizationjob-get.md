---
title: Obtener synchronizationJob
description: Recuperar el trabajo de sincronización existente y sus propiedades.
ms.openlocfilehash: c0c999d5b9ce168ba3f21af20ec5cff026d68f8d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090640"
---
# <a name="get-synchronizationjob"></a><span data-ttu-id="2c7a4-103">Obtener synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="2c7a4-103">Get synchronizationJob</span></span>

> <span data-ttu-id="2c7a4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2c7a4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2c7a4-106">Recuperar el trabajo de sincronización existente y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-106">Retrieve the existing synchronization job and its properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="2c7a4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c7a4-107">Permissions</span></span>
<span data-ttu-id="2c7a4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2c7a4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2c7a4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c7a4-110">Permission type</span></span>                        | <span data-ttu-id="2c7a4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c7a4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="2c7a4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c7a4-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="2c7a4-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2c7a4-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="2c7a4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c7a4-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="2c7a4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-115">Not supported.</span></span>  |
|<span data-ttu-id="2c7a4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c7a4-116">Application</span></span>                            |<span data-ttu-id="2c7a4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-117">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2c7a4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c7a4-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /servicePrincipals/{id}/synchronization/jobs/{jobId}/
```

## <a name="request-headers"></a><span data-ttu-id="2c7a4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c7a4-119">Request headers</span></span>

| <span data-ttu-id="2c7a4-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c7a4-120">Name</span></span>           | <span data-ttu-id="2c7a4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c7a4-121">Type</span></span>    | <span data-ttu-id="2c7a4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c7a4-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="2c7a4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c7a4-123">Authorization</span></span>  | <span data-ttu-id="2c7a4-124">string</span><span class="sxs-lookup"><span data-stu-id="2c7a4-124">string</span></span>  | <span data-ttu-id="2c7a4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2c7a4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c7a4-127">Request body</span></span>

<span data-ttu-id="2c7a4-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2c7a4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c7a4-129">Response</span></span>

<span data-ttu-id="2c7a4-130">Si se realiza correctamente, devuelve un `200 OK` respuesta con un [synchronizationJob](../resources/synchronization-synchronizationjob.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-130">If successful, returns a `200 OK` response with a [synchronizationJob](../resources/synchronization-synchronizationjob.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c7a4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c7a4-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="2c7a4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c7a4-132">Request</span></span>
<span data-ttu-id="2c7a4-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-133">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_synchronizationjob"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/
```

##### <a name="response"></a><span data-ttu-id="2c7a4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c7a4-134">Response</span></span>
<span data-ttu-id="2c7a4-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-135">The following is an example of a response.</span></span> 

><span data-ttu-id="2c7a4-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c7a4-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationJob"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 2577

{
    "id": "{jobId}",
    "templateId": "BoxOutDelta",
    "schedule": {
        "expiration": null,
        "interval": "P10675199DT2H48M5.4775807S",
        "state": "Disabled"
    },
    "status": {
        "countSuccessiveCompleteFailures": 0,
        "escrowsPruned": false,
        "synchronizedEntryCountByType": [],
        "code": "Paused",
        "lastExecution": null,
        "lastSuccessfulExecution": null,
        "progress": [],
        "lastSuccessfulExecutionWithExports": null,
        "steadyStateFirstAchievedTime": "0001-01-01T00:00:00Z",
        "steadyStateLastAchievedTime": "0001-01-01T00:00:00Z",
        "quarantine": null,
        "troubleshootingUrl": null
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get synchronizationJob",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->