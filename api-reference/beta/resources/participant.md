---
title: tipo de recurso de participantes
description: El tipo de participantes.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: c125589506dbd529d2b45df4171e9d54b346cbba
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869835"
---
# <a name="participant-resource-type"></a><span data-ttu-id="90a39-103">tipo de recurso de participantes</span><span class="sxs-lookup"><span data-stu-id="90a39-103">participant resource type</span></span>

> <span data-ttu-id="90a39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90a39-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90a39-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90a39-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="90a39-106">El tipo de participantes.</span><span class="sxs-lookup"><span data-stu-id="90a39-106">The participant type.</span></span>

## <a name="methods"></a><span data-ttu-id="90a39-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="90a39-107">Methods</span></span>

| <span data-ttu-id="90a39-108">Método</span><span class="sxs-lookup"><span data-stu-id="90a39-108">Method</span></span>                                                          | <span data-ttu-id="90a39-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90a39-109">Return Type</span></span>                              | <span data-ttu-id="90a39-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a39-110">Description</span></span>                                       |
|:----------------------------------------------------------------|:-----------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="90a39-111">Obtener participante</span><span class="sxs-lookup"><span data-stu-id="90a39-111">Get participant</span></span>](../api/participant-get.md)                    | [<span data-ttu-id="90a39-112">participante</span><span class="sxs-lookup"><span data-stu-id="90a39-112">participant</span></span>](participant.md)            | <span data-ttu-id="90a39-113">Leer las propiedades del objeto **participante** .</span><span class="sxs-lookup"><span data-stu-id="90a39-113">Read properties of the **participant** object.</span></span>    |
| [<span data-ttu-id="90a39-114">ConfigureMixer</span><span class="sxs-lookup"><span data-stu-id="90a39-114">ConfigureMixer</span></span>](../api/participant-configuremixer.md)          | [<span data-ttu-id="90a39-115">commsOperation</span><span class="sxs-lookup"><span data-stu-id="90a39-115">commsOperation</span></span>](commsoperation.md)      | <span data-ttu-id="90a39-116">Configure el Mezclador de audio participante.</span><span class="sxs-lookup"><span data-stu-id="90a39-116">Configure the participant audio mixer.</span></span>            |
| [<span data-ttu-id="90a39-117">Invitar</span><span class="sxs-lookup"><span data-stu-id="90a39-117">Invite</span></span>](../api/participant-invite.md)                          | [<span data-ttu-id="90a39-118">commsOperation</span><span class="sxs-lookup"><span data-stu-id="90a39-118">commsOperation</span></span>](commsoperation.md)      | <span data-ttu-id="90a39-119">Invitar a un participante a la llamada.</span><span class="sxs-lookup"><span data-stu-id="90a39-119">Invite a participant to the call.</span></span>                 |
| [<span data-ttu-id="90a39-120">Desactivar el participante</span><span class="sxs-lookup"><span data-stu-id="90a39-120">Mute participant</span></span>](../api/participant-mute.md)                  | [<span data-ttu-id="90a39-121">commsOperation</span><span class="sxs-lookup"><span data-stu-id="90a39-121">commsOperation</span></span>](commsoperation.md)      | <span data-ttu-id="90a39-122">Desactivar a un participante en una llamada.</span><span class="sxs-lookup"><span data-stu-id="90a39-122">Mute a participant in a call.</span></span>                     |
| [<span data-ttu-id="90a39-123">Desactivar todos los participantes</span><span class="sxs-lookup"><span data-stu-id="90a39-123">Mute all participants</span></span>](../api/participant-muteall.md)          | [<span data-ttu-id="90a39-124">commsOperation</span><span class="sxs-lookup"><span data-stu-id="90a39-124">commsOperation</span></span>](commsoperation.md)      | <span data-ttu-id="90a39-125">Silenciar a todos los participantes en la reunión.</span><span class="sxs-lookup"><span data-stu-id="90a39-125">Mute all the participants in the meeting.</span></span>         |

## <a name="properties"></a><span data-ttu-id="90a39-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90a39-126">Properties</span></span>

| <span data-ttu-id="90a39-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90a39-127">Property</span></span>             | <span data-ttu-id="90a39-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="90a39-128">Type</span></span>                                     | <span data-ttu-id="90a39-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a39-129">Description</span></span>                                                  |
| :------------------- | :--------------------------------------- | :------------------------------------------------------------|
| <span data-ttu-id="90a39-130">id</span><span class="sxs-lookup"><span data-stu-id="90a39-130">id</span></span>                   | <span data-ttu-id="90a39-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="90a39-131">String</span></span>                                   | <span data-ttu-id="90a39-132">El identificador de participante.</span><span class="sxs-lookup"><span data-stu-id="90a39-132">The participant id.</span></span>                                          |
| <span data-ttu-id="90a39-133">Info</span><span class="sxs-lookup"><span data-stu-id="90a39-133">info</span></span>                 | [<span data-ttu-id="90a39-134">participantInfo</span><span class="sxs-lookup"><span data-stu-id="90a39-134">participantInfo</span></span>](participantinfo.md)    | <span data-ttu-id="90a39-135">El participante del participante.</span><span class="sxs-lookup"><span data-stu-id="90a39-135">The participant of the participant.</span></span>                          |
| <span data-ttu-id="90a39-136">isInLobby</span><span class="sxs-lookup"><span data-stu-id="90a39-136">isInLobby</span></span>            | <span data-ttu-id="90a39-137">boolean</span><span class="sxs-lookup"><span data-stu-id="90a39-137">boolean</span></span>                                  | <span data-ttu-id="90a39-138">True si el participante se encuentra en la sala de espera</span><span class="sxs-lookup"><span data-stu-id="90a39-138">true if the participant is in lobby</span></span>                          |
| <span data-ttu-id="90a39-139">isMuted</span><span class="sxs-lookup"><span data-stu-id="90a39-139">isMuted</span></span>              | <span data-ttu-id="90a39-140">boolean</span><span class="sxs-lookup"><span data-stu-id="90a39-140">boolean</span></span>                                  | <span data-ttu-id="90a39-141">True si se ha desactivado el participante (cliente o servidor ha desactivado)</span><span class="sxs-lookup"><span data-stu-id="90a39-141">true if the participant is muted (client or server muted)</span></span>    |
| <span data-ttu-id="90a39-142">mediaStreams</span><span class="sxs-lookup"><span data-stu-id="90a39-142">mediaStreams</span></span>         | <span data-ttu-id="90a39-143">colección de [mediaStream](mediastream.md)</span><span class="sxs-lookup"><span data-stu-id="90a39-143">[mediaStream](mediastream.md) collection</span></span> | <span data-ttu-id="90a39-144">La lista de flujos de medios.</span><span class="sxs-lookup"><span data-stu-id="90a39-144">The list of media streams.</span></span>                                   |
| <span data-ttu-id="90a39-145">metadatos</span><span class="sxs-lookup"><span data-stu-id="90a39-145">metadata</span></span>             | <span data-ttu-id="90a39-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="90a39-146">String</span></span>                                   | <span data-ttu-id="90a39-147">Un blob de datos proporcionados por el participante en la lista de participantes</span><span class="sxs-lookup"><span data-stu-id="90a39-147">A blob of data provided by the participant in the roster</span></span>     |
| <span data-ttu-id="90a39-148">recordingInfo</span><span class="sxs-lookup"><span data-stu-id="90a39-148">recordingInfo</span></span>        | [<span data-ttu-id="90a39-149">recordingInfo</span><span class="sxs-lookup"><span data-stu-id="90a39-149">recordingInfo</span></span>](recordinginfo.md)        | <span data-ttu-id="90a39-150">Información sobre si el participante tiene capacidad de grabación.</span><span class="sxs-lookup"><span data-stu-id="90a39-150">Information on whether the participant has recording capability.</span></span> |

## <a name="relationships"></a><span data-ttu-id="90a39-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="90a39-151">Relationships</span></span>
<span data-ttu-id="90a39-152">Ninguno</span><span class="sxs-lookup"><span data-stu-id="90a39-152">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="90a39-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90a39-153">JSON representation</span></span>

<span data-ttu-id="90a39-154">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="90a39-154">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.participant"
}-->
```json
{
  "id": "String (identifier)",
  "info": {"@odata.type": "#microsoft.graph.participantInfo"},
  "isInLobby": true,
  "isMuted": true,
  "mediaStreams": [ { "@odata.type": "#microsoft.graph.mediaStream" } ],
  "metadata": "String",
  "recordingInfo": { "@odata.type": "#microsoft.graph.recordingInfo" }
}
```

## <a name="example"></a><span data-ttu-id="90a39-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90a39-155">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.participant"
}-->
```json
{
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "info": {
    "identity": {
      "user": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "Heidi Steen"
      }
    },
    "languageId": "en-US",
    "region": "westus"
  },
  "isInLobby": false,
  "isMuted": false,
  "mediaStreams": [
    {
      "sourceId": "1",
      "direction": "sendReceive",
      "label": "main-audio",
      "mediaType": "audio",
      "serverMuted": false
    }
  ],
  "metadata": "metadata-value",
  "recordingInfo": {
    "status": "recordingCapable"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "participant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
