---
title: tipo de recurso recordOperation
description: El tipo de recordOperation
author: VinodRavichandran
ms.openlocfilehash: 54b39f30df1dd53a95260b549ae9fab2eedddfd8
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380425"
---
# <a name="recordoperation-resource-type"></a><span data-ttu-id="a8ff7-103">tipo de recurso recordOperation</span><span class="sxs-lookup"><span data-stu-id="a8ff7-103">recordOperation resource type</span></span>

> <span data-ttu-id="a8ff7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a8ff7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a8ff7-106">El tipo de recordOperation</span><span class="sxs-lookup"><span data-stu-id="a8ff7-106">The recordOperation type</span></span>

## <a name="properties"></a><span data-ttu-id="a8ff7-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8ff7-107">Properties</span></span>

| <span data-ttu-id="a8ff7-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8ff7-108">Property</span></span>                       | <span data-ttu-id="a8ff7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8ff7-109">Type</span></span>                        | <span data-ttu-id="a8ff7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8ff7-110">Description</span></span>                                                                                                                                       |
| :----------------------------- | :---------------------------| :-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ff7-111">clientContext</span><span class="sxs-lookup"><span data-stu-id="a8ff7-111">clientContext</span></span>                  | <span data-ttu-id="a8ff7-112">String</span><span class="sxs-lookup"><span data-stu-id="a8ff7-112">String</span></span>                      | <span data-ttu-id="a8ff7-113">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-113">The client context.</span></span>                                                                                                                               |
| <span data-ttu-id="a8ff7-114">completionReason</span><span class="sxs-lookup"><span data-stu-id="a8ff7-114">completionReason</span></span>               | <span data-ttu-id="a8ff7-115">String</span><span class="sxs-lookup"><span data-stu-id="a8ff7-115">String</span></span>                      | <span data-ttu-id="a8ff7-116">Los valores posibles son: `operationCanceled`, `stopToneDetected`, `maxRecordDurationReached`, `initialSilenceTimeout`, `maxSilenceTimeout`, `playPromptFailed`, `playBeepFailed`, `mediaReceiveTimeout`, `unspecifiedError` y `none`.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-116">Possible values are: `operationCanceled`, `stopToneDetected`, `maxRecordDurationReached`, `initialSilenceTimeout`, `maxSilenceTimeout`, `playPromptFailed`, `playBeepFailed`, `mediaReceiveTimeout`, `unspecifiedError`, `none`.</span></span> |
| <span data-ttu-id="a8ff7-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a8ff7-117">createdDateTime</span></span>                | <span data-ttu-id="a8ff7-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a8ff7-118">DateTimeOffset</span></span>              | <span data-ttu-id="a8ff7-119">La hora de creación de la grabación.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-119">The time when the recording was created.</span></span>                                                                                                          |
| <span data-ttu-id="a8ff7-120">id</span><span class="sxs-lookup"><span data-stu-id="a8ff7-120">id</span></span>                             | <span data-ttu-id="a8ff7-121">String</span><span class="sxs-lookup"><span data-stu-id="a8ff7-121">String</span></span>                      | <span data-ttu-id="a8ff7-122">Identificador de la operación de servidor. Es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-122">The server operation id. Read-only.</span></span> <span data-ttu-id="a8ff7-123">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-123">Server generated.</span></span>                                                                                             |
| <span data-ttu-id="a8ff7-124">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="a8ff7-124">lastActionDateTime</span></span>             | <span data-ttu-id="a8ff7-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a8ff7-125">DateTimeOffset</span></span>              | <span data-ttu-id="a8ff7-126">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-126">The time of the last action of the operation.</span></span>                                                                                                     |
| <span data-ttu-id="a8ff7-127">recordResourceAccessToken</span><span class="sxs-lookup"><span data-stu-id="a8ff7-127">recordResourceAccessToken</span></span>      | <span data-ttu-id="a8ff7-128">String</span><span class="sxs-lookup"><span data-stu-id="a8ff7-128">String</span></span>                      | <span data-ttu-id="a8ff7-129">El token de acceso necesario para recuperar la grabación.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-129">The access token required to retrieve the recording.</span></span>                                                                                              |
| <span data-ttu-id="a8ff7-130">recordResourceLocation</span><span class="sxs-lookup"><span data-stu-id="a8ff7-130">recordResourceLocation</span></span>         | <span data-ttu-id="a8ff7-131">String</span><span class="sxs-lookup"><span data-stu-id="a8ff7-131">String</span></span>                      | <span data-ttu-id="a8ff7-132">La ubicación donde se encuentra la grabación.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-132">The location where the recording is located.</span></span>                                                                                                      |
| <span data-ttu-id="a8ff7-133">resultInfo</span><span class="sxs-lookup"><span data-stu-id="a8ff7-133">resultInfo</span></span>                     | [<span data-ttu-id="a8ff7-134">resultInfo</span><span class="sxs-lookup"><span data-stu-id="a8ff7-134">resultInfo</span></span>](resultinfo.md) | <span data-ttu-id="a8ff7-135">La información del resultado.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-135">The result information.</span></span>  <span data-ttu-id="a8ff7-136">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-136">Read-only.</span></span> <span data-ttu-id="a8ff7-137">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-137">Server generated.</span></span>                                                                                             |
| <span data-ttu-id="a8ff7-138">status</span><span class="sxs-lookup"><span data-stu-id="a8ff7-138">status</span></span>                         | <span data-ttu-id="a8ff7-139">String</span><span class="sxs-lookup"><span data-stu-id="a8ff7-139">String</span></span>                      | <span data-ttu-id="a8ff7-140">Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-140">Possible values are: `notStarted`, `running`, `completed`, `failed`.</span></span> <span data-ttu-id="a8ff7-141">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-141">Read-only.</span></span> <span data-ttu-id="a8ff7-142">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="a8ff7-142">Server generated.</span></span>                                                 |

## <a name="relationships"></a><span data-ttu-id="a8ff7-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a8ff7-143">Relationships</span></span>
<span data-ttu-id="a8ff7-144">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a8ff7-144">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="a8ff7-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a8ff7-145">JSON representation</span></span>

<span data-ttu-id="a8ff7-146">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a8ff7-146">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recordOperation"
}-->
```json
{
  "clientContext": "String",
  "completionReason": "operationCanceled | stopToneDetected | maxRecordDurationReached | initialSilenceTimeout | maxSilenceTimeout | playPromptFailed | playBeepFailed | mediaReceiveTimeout | unspecifiedError | none",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "recordResourceAccessToken": "String",
  "recordResourceLocation": "String",
  "resultInfo": {"@odata.type": "#microsoft.graph.resultInfo"},
  "status": "notStarted | running | completed | failed"
}
```

## <a name="example"></a><span data-ttu-id="a8ff7-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8ff7-147">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.recordOperation",
  "truncated": true
}-->
```json
{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "recordResourceAccessToken": "<access-token>",
  "recordResourceLocation": "https://resource.location/ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "status": "completed"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recordOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
