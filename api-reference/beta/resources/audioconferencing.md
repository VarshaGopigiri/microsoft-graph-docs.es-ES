---
title: tipo de recurso de audioconferencia
description: Representa la información de acceso telefónica de un onlineMeeting.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 9bd8343f29a797a24044f02aa2a00bd098c35007
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843627"
---
# <a name="audioconferencing-resource-type"></a><span data-ttu-id="cdc0c-103">tipo de recurso de audioconferencia</span><span class="sxs-lookup"><span data-stu-id="cdc0c-103">audioConferencing resource type</span></span>

> <span data-ttu-id="cdc0c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cdc0c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cdc0c-106">Representa la información de acceso telefónica de un [onlineMeeting](onlinemeeting.md).</span><span class="sxs-lookup"><span data-stu-id="cdc0c-106">Represents phone access information for an [onlineMeeting](onlinemeeting.md).</span></span>

## <a name="properties"></a><span data-ttu-id="cdc0c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cdc0c-107">Properties</span></span>

| <span data-ttu-id="cdc0c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cdc0c-108">Property</span></span>            | <span data-ttu-id="cdc0c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cdc0c-109">Type</span></span>    | <span data-ttu-id="cdc0c-110">Description</span><span class="sxs-lookup"><span data-stu-id="cdc0c-110">Description</span></span>                                                                    |
|:--------------------|:--------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="cdc0c-111">dialinUrl</span><span class="sxs-lookup"><span data-stu-id="cdc0c-111">dialinUrl</span></span>           | <span data-ttu-id="cdc0c-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="cdc0c-112">String</span></span>  | <span data-ttu-id="cdc0c-113">Una dirección URL a la página web accesibles de forma externa que contiene la información de marcado.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-113">A URL to the externally-accessible web page that contains dial-in information.</span></span> |
| <span data-ttu-id="cdc0c-114">leaderPasscode</span><span class="sxs-lookup"><span data-stu-id="cdc0c-114">leaderPasscode</span></span>      | <span data-ttu-id="cdc0c-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="cdc0c-115">String</span></span>  | <span data-ttu-id="cdc0c-116">La contraseña de coordinador necesaria para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-116">The leader password required to connect to the Audio Conference Provider.</span></span>      |
| <span data-ttu-id="cdc0c-117">participantPasscode</span><span class="sxs-lookup"><span data-stu-id="cdc0c-117">participantPasscode</span></span> | <span data-ttu-id="cdc0c-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="cdc0c-118">String</span></span>  | <span data-ttu-id="cdc0c-119">La contraseña de participantes necesaria para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-119">The participant password required to connect to the Audio Conference Provider.</span></span> |
| <span data-ttu-id="cdc0c-120">tollFreeNumber</span><span class="sxs-lookup"><span data-stu-id="cdc0c-120">tollFreeNumber</span></span>      | <span data-ttu-id="cdc0c-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="cdc0c-121">String</span></span>  | <span data-ttu-id="cdc0c-122">El número gratuito para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-122">The toll-free number to connect to the Audio Conference Provider.</span></span>              |
| <span data-ttu-id="cdc0c-123">tollNumber</span><span class="sxs-lookup"><span data-stu-id="cdc0c-123">tollNumber</span></span>          | <span data-ttu-id="cdc0c-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="cdc0c-124">String</span></span>  | <span data-ttu-id="cdc0c-125">El número de teléfono de pago para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-125">The toll number to connect to the Audio Conference Provider.</span></span>                   |

## <a name="json-representation"></a><span data-ttu-id="cdc0c-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cdc0c-126">JSON representation</span></span>

<span data-ttu-id="cdc0c-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cdc0c-127">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioConferencing"
}-->
```json
{
  "dialinUrl": "String",
  "leaderPasscode": "String",
  "participantPasscode": "String",
  "tollFreeNumber": "String",
  "tollNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioConferencing resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
