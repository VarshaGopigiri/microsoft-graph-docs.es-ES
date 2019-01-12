---
title: tipo de recurso de audioconferencia
description: Representa la información de acceso telefónica de un onlineMeeting.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: cd65b094a17ad3fa470471c3ed6dd3908367e578
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977510"
---
# <a name="audioconferencing-resource-type"></a><span data-ttu-id="f6182-103">tipo de recurso de audioconferencia</span><span class="sxs-lookup"><span data-stu-id="f6182-103">audioConferencing resource type</span></span>

> <span data-ttu-id="f6182-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6182-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6182-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6182-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f6182-106">Representa la información de acceso telefónica de un [onlineMeeting](onlinemeeting.md).</span><span class="sxs-lookup"><span data-stu-id="f6182-106">Represents phone access information for an [onlineMeeting](onlinemeeting.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f6182-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6182-107">Properties</span></span>

| <span data-ttu-id="f6182-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6182-108">Property</span></span>            | <span data-ttu-id="f6182-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6182-109">Type</span></span>    | <span data-ttu-id="f6182-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6182-110">Description</span></span>                                                                    |
|:--------------------|:--------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="f6182-111">dialinUrl</span><span class="sxs-lookup"><span data-stu-id="f6182-111">dialinUrl</span></span>           | <span data-ttu-id="f6182-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="f6182-112">String</span></span>  | <span data-ttu-id="f6182-113">Una dirección URL a la página web accesibles de forma externa que contiene la información de marcado.</span><span class="sxs-lookup"><span data-stu-id="f6182-113">A URL to the externally-accessible web page that contains dial-in information.</span></span> |
| <span data-ttu-id="f6182-114">leaderPasscode</span><span class="sxs-lookup"><span data-stu-id="f6182-114">leaderPasscode</span></span>      | <span data-ttu-id="f6182-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="f6182-115">String</span></span>  | <span data-ttu-id="f6182-116">La contraseña de coordinador necesaria para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="f6182-116">The leader password required to connect to the Audio Conference Provider.</span></span>      |
| <span data-ttu-id="f6182-117">participantPasscode</span><span class="sxs-lookup"><span data-stu-id="f6182-117">participantPasscode</span></span> | <span data-ttu-id="f6182-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="f6182-118">String</span></span>  | <span data-ttu-id="f6182-119">La contraseña de participantes necesaria para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="f6182-119">The participant password required to connect to the Audio Conference Provider.</span></span> |
| <span data-ttu-id="f6182-120">tollFreeNumber</span><span class="sxs-lookup"><span data-stu-id="f6182-120">tollFreeNumber</span></span>      | <span data-ttu-id="f6182-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="f6182-121">String</span></span>  | <span data-ttu-id="f6182-122">El número gratuito para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="f6182-122">The toll-free number to connect to the Audio Conference Provider.</span></span>              |
| <span data-ttu-id="f6182-123">tollNumber</span><span class="sxs-lookup"><span data-stu-id="f6182-123">tollNumber</span></span>          | <span data-ttu-id="f6182-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="f6182-124">String</span></span>  | <span data-ttu-id="f6182-125">El número de teléfono de pago para conectarse al proveedor de conferencia de Audio.</span><span class="sxs-lookup"><span data-stu-id="f6182-125">The toll number to connect to the Audio Conference Provider.</span></span>                   |

## <a name="json-representation"></a><span data-ttu-id="f6182-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6182-126">JSON representation</span></span>

<span data-ttu-id="f6182-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f6182-127">The following is a JSON representation of the resource.</span></span>

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
