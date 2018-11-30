---
title: Crear synchronizationJob
description: Crear nuevo trabajo de sincronización con un esquema de sincronización predeterminado. El trabajo se crea en un estado deshabilitado. Llamada de trabajo de inicio para iniciar la sincronización.
ms.openlocfilehash: 3c7e3c3a9c89f95b031cd45d38848e0f2f451de7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090272"
---
# <a name="create-synchronizationjob"></a><span data-ttu-id="c7836-105">Crear synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="c7836-105">Create synchronizationJob</span></span>

> <span data-ttu-id="c7836-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c7836-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c7836-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c7836-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c7836-108">Crear nuevo trabajo de sincronización con un esquema de sincronización predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c7836-108">Create new synchronization job with a default synchronization schema.</span></span> <span data-ttu-id="c7836-109">El trabajo se crea en un estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="c7836-109">The job is created in a disabled state.</span></span> <span data-ttu-id="c7836-110">Llamar a [iniciar el trabajo](synchronization-synchronizationjob-start.md) para iniciar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="c7836-110">Call [Start job](synchronization-synchronizationjob-start.md) to start synchronization.</span></span>

## <a name="permissions"></a><span data-ttu-id="c7836-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="c7836-111">Permissions</span></span>
<span data-ttu-id="c7836-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7836-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7836-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7836-114">Permission type</span></span>                        | <span data-ttu-id="c7836-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7836-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="c7836-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7836-116">Delegated (work or school account)</span></span>     |<span data-ttu-id="c7836-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7836-117">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="c7836-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7836-118">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="c7836-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7836-119">Not supported.</span></span>|
|<span data-ttu-id="c7836-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7836-120">Application</span></span>                            |<span data-ttu-id="c7836-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7836-121">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="c7836-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7836-122">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/
```

## <a name="request-headers"></a><span data-ttu-id="c7836-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7836-123">Request headers</span></span>

| <span data-ttu-id="c7836-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="c7836-124">Name</span></span>           | <span data-ttu-id="c7836-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7836-125">Type</span></span>    | <span data-ttu-id="c7836-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7836-126">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="c7836-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7836-127">Authorization</span></span>  | <span data-ttu-id="c7836-128">string</span><span class="sxs-lookup"><span data-stu-id="c7836-128">string</span></span>  | <span data-ttu-id="c7836-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7836-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c7836-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7836-131">Request body</span></span>

<span data-ttu-id="c7836-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [synchronizationJob](../resources/synchronization-synchronizationjob.md) que se creará.</span><span class="sxs-lookup"><span data-stu-id="c7836-132">In the request body, supply a JSON representation of the [synchronizationJob](../resources/synchronization-synchronizationjob.md) object to be created.</span></span> <span data-ttu-id="c7836-133">La única propiedad necesaria es `templateId`.</span><span class="sxs-lookup"><span data-stu-id="c7836-133">The only required property is `templateId`.</span></span> <span data-ttu-id="c7836-134">El `templateId` (propiedad) debe coincidir con una de las plantillas creadas para esta entidad de seguridad de la aplicación o servicio.</span><span class="sxs-lookup"><span data-stu-id="c7836-134">The `templateId` property must match one of the templates created for this application/service principal.</span></span> <span data-ttu-id="c7836-135">Para buscar plantillas disponibles, use [las plantillas de lista](synchronization-synchronizationtemplate-list.md).</span><span class="sxs-lookup"><span data-stu-id="c7836-135">To find available templates, use [List templates](synchronization-synchronizationtemplate-list.md).</span></span>

## <a name="response"></a><span data-ttu-id="c7836-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7836-136">Response</span></span>

<span data-ttu-id="c7836-137">Si se realiza correctamente, devuelve un `201 Created` código de respuesta y un objeto [synchronizationJob](../resources/synchronization-synchronizationjob.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7836-137">If successful, returns a `201 Created` response code and a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7836-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7836-138">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c7836-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7836-139">Request</span></span>
<span data-ttu-id="c7836-140">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7836-140">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_synchronizationjob_from_synchronization"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs
Content-type: application/json

{ 
    "templateId": "BoxOutDelta"
}
```

##### <a name="response"></a><span data-ttu-id="c7836-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7836-141">Response</span></span>
<span data-ttu-id="c7836-142">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7836-142">The following is an example of a response.</span></span> 

><span data-ttu-id="c7836-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7836-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationJob"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

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
        "code": "NotConfigured",
        "lastExecution": null,
        "lastSuccessfulExecution": null,
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
  "description": "Create synchronizationJob",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->