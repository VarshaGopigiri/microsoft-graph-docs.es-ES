---
title: tipo de recurso visualInfo
description: Un tipo complejo para que representa la propiedad **visualElements** en el objeto de actividad.
ms.openlocfilehash: f77e25a7aad7d4357f6444fbdbd0f06a5cffd023
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030483"
---
# <a name="visualinfo-resource-type"></a><span data-ttu-id="0a52e-103">tipo de recurso visualInfo</span><span class="sxs-lookup"><span data-stu-id="0a52e-103">visualInfo resource type</span></span>

<span data-ttu-id="0a52e-104">Un tipo complejo para que representa la propiedad **visualElements** en el objeto de [actividad](../resources/projectrome-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="0a52e-104">A complex type for representing the **visualElements** property in the [activity](../resources/projectrome-activity.md) object.</span></span>

<span data-ttu-id="0a52e-105">Cada actividad del usuario se mostrarán en la escala de tiempo como una tarjeta adaptable.</span><span class="sxs-lookup"><span data-stu-id="0a52e-105">Each user activity will be shown in Timeline as an Adaptive Card.</span></span> <span data-ttu-id="0a52e-106">Animamos a los programadores de la aplicación para proporcionar una tarjeta personalizada que captura la esencia de la actividad que tuvo lugar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a52e-106">App developers are encouraged to provide a custom Card which captures the essence of the activity which took place in your app.</span></span> <span data-ttu-id="0a52e-107">Esto es posible, ya que proporciona una tarjeta de JSON personalizada en la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="0a52e-107">This is possible by providing a custom JSON card in the content property.</span></span>

<span data-ttu-id="0a52e-108">Además de metadatos visual con una tarjeta adaptable, la aplicación puede especificar los metadatos de contenido: datos que se usó para generar inferencias en la actividad de usuario con el fin de ofrecer nuevas actividades para futura subcontratación vuelva.</span><span class="sxs-lookup"><span data-stu-id="0a52e-108">In addition to visual metadata with an Adaptive Card, app can specify content metadata – data that be used to build inferences on the user’s activity in order to offer new activities for future re-engagement.</span></span> <span data-ttu-id="0a52e-109">Esto es posible mediante el uso de propiedad de contentInfo de la actividad para proporcionar un objeto JSON que aprovecha las propiedades schema.org para describir el contenido.</span><span class="sxs-lookup"><span data-stu-id="0a52e-109">This is possible by using the activity's contentInfo property to provide a JSON object which leverages schema.org properties to describe the content.</span></span>

<span data-ttu-id="0a52e-110">Si no se proporciona una ficha personalizada, se generará una tarjeta simple mediante las propiedades de texto de presentación y una descripción.</span><span class="sxs-lookup"><span data-stu-id="0a52e-110">If a custom card is not provided, a simple card will be generated using displayText and description properties.</span></span> <span data-ttu-id="0a52e-111">Se recomiendan las tarjetas personalizadas para demostrar el mejor contenido desde dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a52e-111">Custom cards are recommended to showcase the best content from within your app.</span></span>

## <a name="properties"></a><span data-ttu-id="0a52e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a52e-112">Properties</span></span>

|<span data-ttu-id="0a52e-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a52e-113">Name</span></span> | <span data-ttu-id="0a52e-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a52e-114">Type</span></span> | <span data-ttu-id="0a52e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a52e-115">Description</span></span>|
|:----|:------|:-----------|
|<span data-ttu-id="0a52e-116">texto de presentación</span><span class="sxs-lookup"><span data-stu-id="0a52e-116">displayText</span></span> | <span data-ttu-id="0a52e-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="0a52e-117">String</span></span> | <span data-ttu-id="0a52e-118">Necesario.</span><span class="sxs-lookup"><span data-stu-id="0a52e-118">Required.</span></span> <span data-ttu-id="0a52e-119">Breve descripción de texto de la actividad de usuario único (por ejemplo, el nombre de documento en los casos donde una actividad hace referencia a la creación de documentos)</span><span class="sxs-lookup"><span data-stu-id="0a52e-119">Short text description of the user's unique activity (for example, document name in cases where an activity refers to document creation)</span></span>|
|<span data-ttu-id="0a52e-120">descripción</span><span class="sxs-lookup"><span data-stu-id="0a52e-120">description</span></span> | <span data-ttu-id="0a52e-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="0a52e-121">String</span></span> | <span data-ttu-id="0a52e-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a52e-122">Optional.</span></span> <span data-ttu-id="0a52e-123">Descripción de texto más larga de la actividad de usuario único (ejemplo: nombre, primera oración y metadatos de documentos)</span><span class="sxs-lookup"><span data-stu-id="0a52e-123">Longer text description of the user's unique activity (example: document name, first sentence, and/or metadata)</span></span>|
|<span data-ttu-id="0a52e-124">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0a52e-124">backgroundColor</span></span> | <span data-ttu-id="0a52e-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="0a52e-125">String</span></span> | <span data-ttu-id="0a52e-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a52e-126">Optional.</span></span> <span data-ttu-id="0a52e-127">Color de fondo utilizado para representar la actividad en la interfaz de usuario - color de marca para el origen de la aplicación de la actividad.</span><span class="sxs-lookup"><span data-stu-id="0a52e-127">Background color used to render the activity in the UI - brand color for the application source of the activity.</span></span> <span data-ttu-id="0a52e-128">Debe ser un color hexadecimal válido</span><span class="sxs-lookup"><span data-stu-id="0a52e-128">Must be a valid hex color</span></span>|
|<span data-ttu-id="0a52e-129">content</span><span class="sxs-lookup"><span data-stu-id="0a52e-129">content</span></span> | <span data-ttu-id="0a52e-130">Objeto JSON sin tipo</span><span class="sxs-lookup"><span data-stu-id="0a52e-130">Untyped JSON object</span></span> | <span data-ttu-id="0a52e-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a52e-131">Optional.</span></span> <span data-ttu-id="0a52e-132">Fragmento personalizado de datos - objeto JSON se usa para proporcionar contenido personalizado para representar la actividad en la interfaz de usuario del Shell de Windows</span><span class="sxs-lookup"><span data-stu-id="0a52e-132">Custom piece of data - JSON object used to provide custom content to render the activity in the Windows Shell UI</span></span>|
|<span data-ttu-id="0a52e-133">atribución</span><span class="sxs-lookup"><span data-stu-id="0a52e-133">attribution</span></span> | [<span data-ttu-id="0a52e-134">imageInfo</span><span class="sxs-lookup"><span data-stu-id="0a52e-134">imageInfo</span></span>](../resources/projectrome-imageinfo.md) | <span data-ttu-id="0a52e-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a52e-135">Optional.</span></span> <span data-ttu-id="0a52e-136">Objeto JSON usado para representar un icono que representa la aplicación que se usa para generar la actividad</span><span class="sxs-lookup"><span data-stu-id="0a52e-136">JSON object used to represent an icon which represents the application used to generate the activity</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0a52e-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0a52e-137">JSON Representation</span></span>

<span data-ttu-id="0a52e-138">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0a52e-138">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attribution",
    "description",
    "backgroundColor",
    "content"
  ],
  "@odata.type": "microsoft.graph.visualInfo"
}-->

```json
{
    "@odata.type": "microsoft.graph.visualInfo",
    "attribution": {
        "@odata.type": "microsoft.graph.imageInfo",
        "iconUrl": "String (URL)",
        "alternateText": "String",
        "addImageQuery": "boolean"
    },
    "description": "String",
    "backgroundColor": "String",
    "displayText": "String",
    "content": {
        "@odata.type": "microsoft.graph.Json"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "visualinfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
