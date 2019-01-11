---
title: tipo de recurso invitationParticipantInfo
description: El **InvitationParticipant** se usa para representar un conjunto de identidades asociado con una invitación a una conversación y proporciona los parámetros de invitación adicionales.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 7a6fb418b7076b0f0a42dc05b6afe71dcda6a71e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27865005"
---
# <a name="invitationparticipantinfo-resource-type"></a><span data-ttu-id="094d4-103">tipo de recurso invitationParticipantInfo</span><span class="sxs-lookup"><span data-stu-id="094d4-103">invitationParticipantInfo resource type</span></span>

> <span data-ttu-id="094d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="094d4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="094d4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="094d4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="094d4-106">El **InvitationParticipant** se usa para representar un conjunto de identidades asociado con una invitación a una conversación y proporciona los parámetros de invitación adicionales.</span><span class="sxs-lookup"><span data-stu-id="094d4-106">The **InvitationParticipant** is used to represent a set of identities associated with a conversation invitation, and provides additional invitation parameters.</span></span>

## <a name="properties"></a><span data-ttu-id="094d4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="094d4-107">Properties</span></span>

| <span data-ttu-id="094d4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="094d4-108">Property</span></span>                           | <span data-ttu-id="094d4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="094d4-109">Type</span></span>                          | <span data-ttu-id="094d4-110">Description</span><span class="sxs-lookup"><span data-stu-id="094d4-110">Description</span></span>                                                                          |
| :--------------------------------- | :---------------------------- | :----------------------------------------------------------------------------------- |
| <span data-ttu-id="094d4-111">endpointType</span><span class="sxs-lookup"><span data-stu-id="094d4-111">endpointType</span></span>                       | <span data-ttu-id="094d4-112">String</span><span class="sxs-lookup"><span data-stu-id="094d4-112">String</span></span>                        | <span data-ttu-id="094d4-113">Los valores posibles son: `default` y `voicemail`.</span><span class="sxs-lookup"><span data-stu-id="094d4-113">Possible values are: `default`, `voicemail`.</span></span> |
| <span data-ttu-id="094d4-114">identity</span><span class="sxs-lookup"><span data-stu-id="094d4-114">identity</span></span>                           | [<span data-ttu-id="094d4-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="094d4-115">identitySet</span></span>](identityset.md) | <span data-ttu-id="094d4-116">El [identitySet](identityset.md) asociado con esta invitación.</span><span class="sxs-lookup"><span data-stu-id="094d4-116">The [identitySet](identityset.md) associated with this invitation.</span></span>                   |
| <span data-ttu-id="094d4-117">languageId</span><span class="sxs-lookup"><span data-stu-id="094d4-117">languageId</span></span>                         | <span data-ttu-id="094d4-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="094d4-118">String</span></span>                        | <span data-ttu-id="094d4-119">La cadena de referencia cultural del idioma.</span><span class="sxs-lookup"><span data-stu-id="094d4-119">The language culture string.</span></span>                                                                                     |
| <span data-ttu-id="094d4-120">región</span><span class="sxs-lookup"><span data-stu-id="094d4-120">region</span></span>                             | <span data-ttu-id="094d4-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="094d4-121">String</span></span>                        | <span data-ttu-id="094d4-122">Región del participante.</span><span class="sxs-lookup"><span data-stu-id="094d4-122">Region of the participant.</span></span>                                                           |
| <span data-ttu-id="094d4-123">replacesCallId</span><span class="sxs-lookup"><span data-stu-id="094d4-123">replacesCallId</span></span>                     | <span data-ttu-id="094d4-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="094d4-124">String</span></span>                        | <span data-ttu-id="094d4-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="094d4-125">Optional.</span></span> <span data-ttu-id="094d4-126">La llamada que la idenity destino actualmente es una parte de.</span><span class="sxs-lookup"><span data-stu-id="094d4-126">The call which the target idenity is currently a part of.</span></span> <span data-ttu-id="094d4-127">Una vez que el participante se agrega, se eliminará esta llamada.</span><span class="sxs-lookup"><span data-stu-id="094d4-127">This call will be dropped once the participant is added.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="094d4-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="094d4-128">JSON representation</span></span>

<span data-ttu-id="094d4-129">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="094d4-129">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.invitationParticipantInfo"
}-->
```json
{
  "endpointType": "default | voicemail",
  "identity": {"@odata.type": "#microsoft.graph.identitySet"},
  "languageId": "String",
  "region": "String",
  "replacesCallId": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "invitationParticipantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
