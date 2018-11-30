---
title: tipo de recurso mediaStream
description: El tipo de mediaStream.
ms.openlocfilehash: 28eb98a3ab1be67c60c6ebd35deb7618f1618be3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090726"
---
# <a name="mediastream-resource-type"></a><span data-ttu-id="8232e-103">tipo de recurso mediaStream</span><span class="sxs-lookup"><span data-stu-id="8232e-103">mediaStream resource type</span></span>

> <span data-ttu-id="8232e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8232e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8232e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8232e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8232e-106">El tipo de mediaStream.</span><span class="sxs-lookup"><span data-stu-id="8232e-106">The mediaStream type.</span></span>

## <a name="properties"></a><span data-ttu-id="8232e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8232e-107">Properties</span></span>

| <span data-ttu-id="8232e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8232e-108">Property</span></span>    | <span data-ttu-id="8232e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8232e-109">Type</span></span>    | <span data-ttu-id="8232e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8232e-110">Description</span></span>                                                                                                   |
| :---------- | :------ | :------------------------------------------------------------------------------------------------------------ |
| <span data-ttu-id="8232e-111">dirección</span><span class="sxs-lookup"><span data-stu-id="8232e-111">direction</span></span>   | <span data-ttu-id="8232e-112">String</span><span class="sxs-lookup"><span data-stu-id="8232e-112">String</span></span>  | <span data-ttu-id="8232e-113">La dirección.</span><span class="sxs-lookup"><span data-stu-id="8232e-113">The direction.</span></span> <span data-ttu-id="8232e-114">Los valores posibles son `inactive`, `sendOnly`, `receiveOnly`, `sendReceive`.</span><span class="sxs-lookup"><span data-stu-id="8232e-114">The possible values are `inactive`, `sendOnly`, `receiveOnly`, `sendReceive`.</span></span>                  |
| <span data-ttu-id="8232e-115">label</span><span class="sxs-lookup"><span data-stu-id="8232e-115">label</span></span>       | <span data-ttu-id="8232e-116">String</span><span class="sxs-lookup"><span data-stu-id="8232e-116">String</span></span>  | <span data-ttu-id="8232e-117">La etiqueta de secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="8232e-117">The media stream label.</span></span>                                                                                       |
| <span data-ttu-id="8232e-118">mediaType</span><span class="sxs-lookup"><span data-stu-id="8232e-118">mediaType</span></span>   | <span data-ttu-id="8232e-119">String</span><span class="sxs-lookup"><span data-stu-id="8232e-119">String</span></span>  | <span data-ttu-id="8232e-120">El tipo de medios.</span><span class="sxs-lookup"><span data-stu-id="8232e-120">The media type.</span></span> <span data-ttu-id="8232e-121">Los valores posibles son `unknown`, `audio`, `video`, `videoBasedScreenSharing`, `data`.</span><span class="sxs-lookup"><span data-stu-id="8232e-121">The possible value are `unknown`, `audio`, `video`, `videoBasedScreenSharing`, `data`.</span></span>        |
| <span data-ttu-id="8232e-122">serverMuted</span><span class="sxs-lookup"><span data-stu-id="8232e-122">serverMuted</span></span> | <span data-ttu-id="8232e-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="8232e-123">Boolean</span></span> | <span data-ttu-id="8232e-124">Si se desactiva la multimedia por el servidor.</span><span class="sxs-lookup"><span data-stu-id="8232e-124">If the media is muted by the server.</span></span>                                                                          |
| <span data-ttu-id="8232e-125">sourceId</span><span class="sxs-lookup"><span data-stu-id="8232e-125">sourceId</span></span>    | <span data-ttu-id="8232e-126">String</span><span class="sxs-lookup"><span data-stu-id="8232e-126">String</span></span>  | <span data-ttu-id="8232e-127">El identificador de origen.</span><span class="sxs-lookup"><span data-stu-id="8232e-127">The source ID.</span></span>                                                                                                |

## <a name="json-representation"></a><span data-ttu-id="8232e-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8232e-128">JSON representation</span></span>

<span data-ttu-id="8232e-129">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8232e-129">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "serverMuted"
  ],
  "@odata.type": "microsoft.graph.mediaStream"
}-->
```json
{
  "direction": "inactive | sendOnly | receiveOnly | sendReceive",
  "label": "String",
  "mediaType": "unknown | audio | video | videoBasedScreenSharing | data",
  "serverMuted": true,
  "sourceId": "String"
}
```

## <a name="example"></a><span data-ttu-id="8232e-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8232e-130">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.mediaStream"
}-->
```json
{
  "direction": "sendReceive",
  "label": "main-audio",
  "mediaType": "audio",
  "serverMuted": false,
  "sourceId": "1024"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaStream resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
