---
title: tipo de recurso visualInfo
description: Un tipo complejo para que representa la propiedad **visualElements** en el objeto de actividad.
localization_priority: Normal
ms.openlocfilehash: 3e1dd3d7e4ecfaf5053f839f0ac0d0039692b2a4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855317"
---
# <a name="visualinfo-resource-type"></a><span data-ttu-id="ab9a3-103">tipo de recurso visualInfo</span><span class="sxs-lookup"><span data-stu-id="ab9a3-103">visualInfo resource type</span></span>

> <span data-ttu-id="ab9a3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab9a3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ab9a3-106">Un tipo complejo para que representa la propiedad **visualElements** en el objeto de [actividad](../resources/projectrome-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="ab9a3-106">A complex type for representing the **visualElements** property in the [activity](../resources/projectrome-activity.md) object.</span></span>

<span data-ttu-id="ab9a3-107">Cada actividad del usuario se mostrarán en la escala de tiempo como una tarjeta adaptable.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-107">Each user activity will be shown in Timeline as an Adaptive Card.</span></span> <span data-ttu-id="ab9a3-108">Animamos a los programadores de la aplicación para proporcionar una tarjeta personalizada que captura la esencia de la actividad que tuvo lugar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-108">App developers are encouraged to provide a custom Card which captures the essence of the activity which took place in your app.</span></span> <span data-ttu-id="ab9a3-109">Esto es posible, ya que proporciona una tarjeta de JSON personalizada en la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-109">This is possible by providing a custom JSON card in the content property.</span></span>

<span data-ttu-id="ab9a3-110">Además de metadatos visual con una tarjeta adaptable, la aplicación puede especificar los metadatos de contenido: datos que se usó para generar inferencias en la actividad de usuario con el fin de ofrecer nuevas actividades para futura subcontratación vuelva.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-110">In addition to visual metadata with an Adaptive Card, app can specify content metadata – data that be used to build inferences on the user’s activity in order to offer new activities for future re-engagement.</span></span> <span data-ttu-id="ab9a3-111">Esto es posible mediante el uso de propiedad de contentInfo de la actividad para proporcionar un objeto JSON que aprovecha las propiedades schema.org para describir el contenido.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-111">This is possible by using the activity's contentInfo property to provide a JSON object which leverages schema.org properties to describe the content.</span></span>

<span data-ttu-id="ab9a3-112">Si no se proporciona una ficha personalizada, se generará una tarjeta simple mediante las propiedades de texto de presentación y una descripción.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-112">If a custom card is not provided, a simple card will be generated using displayText and description properties.</span></span> <span data-ttu-id="ab9a3-113">Se recomiendan las tarjetas personalizadas para demostrar el mejor contenido desde dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-113">Custom cards are recommended to showcase the best content from within your app.</span></span>

## <a name="properties"></a><span data-ttu-id="ab9a3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab9a3-114">Properties</span></span>

|<span data-ttu-id="ab9a3-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab9a3-115">Name</span></span> | <span data-ttu-id="ab9a3-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab9a3-116">Type</span></span> | <span data-ttu-id="ab9a3-117">Description</span><span class="sxs-lookup"><span data-stu-id="ab9a3-117">Description</span></span>|
|:----|:------|:-----------|
|<span data-ttu-id="ab9a3-118">texto de presentación</span><span class="sxs-lookup"><span data-stu-id="ab9a3-118">displayText</span></span> | <span data-ttu-id="ab9a3-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab9a3-119">String</span></span> | <span data-ttu-id="ab9a3-120">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-120">Required.</span></span> <span data-ttu-id="ab9a3-121">Breve descripción de texto de la actividad de usuario único (por ejemplo, el nombre de documento en los casos donde una actividad hace referencia a la creación de documentos)</span><span class="sxs-lookup"><span data-stu-id="ab9a3-121">Short text description of the user's unique activity (for example, document name in cases where an activity refers to document creation)</span></span>|
|<span data-ttu-id="ab9a3-122">descripción</span><span class="sxs-lookup"><span data-stu-id="ab9a3-122">description</span></span> | <span data-ttu-id="ab9a3-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab9a3-123">String</span></span> | <span data-ttu-id="ab9a3-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-124">Optional.</span></span> <span data-ttu-id="ab9a3-125">Descripción de texto más larga de la actividad de usuario único (ejemplo: nombre, primera oración y metadatos de documentos)</span><span class="sxs-lookup"><span data-stu-id="ab9a3-125">Longer text description of the user's unique activity (example: document name, first sentence, and/or metadata)</span></span>|
|<span data-ttu-id="ab9a3-126">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ab9a3-126">backgroundColor</span></span> | <span data-ttu-id="ab9a3-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab9a3-127">String</span></span> | <span data-ttu-id="ab9a3-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-128">Optional.</span></span> <span data-ttu-id="ab9a3-129">Color de fondo utilizado para representar la actividad en la interfaz de usuario - color de marca para el origen de la aplicación de la actividad.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-129">Background color used to render the activity in the UI - brand color for the application source of the activity.</span></span> <span data-ttu-id="ab9a3-130">Debe ser un color hexadecimal válido</span><span class="sxs-lookup"><span data-stu-id="ab9a3-130">Must be a valid hex color</span></span>|
|<span data-ttu-id="ab9a3-131">content</span><span class="sxs-lookup"><span data-stu-id="ab9a3-131">content</span></span> | <span data-ttu-id="ab9a3-132">Objeto JSON sin tipo</span><span class="sxs-lookup"><span data-stu-id="ab9a3-132">Untyped JSON object</span></span> | <span data-ttu-id="ab9a3-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-133">Optional.</span></span> <span data-ttu-id="ab9a3-134">Fragmento personalizado de datos - objeto JSON se usa para proporcionar contenido personalizado para representar la actividad en la interfaz de usuario del Shell de Windows</span><span class="sxs-lookup"><span data-stu-id="ab9a3-134">Custom piece of data - JSON object used to provide custom content to render the activity in the Windows Shell UI</span></span>|
|<span data-ttu-id="ab9a3-135">atribución</span><span class="sxs-lookup"><span data-stu-id="ab9a3-135">attribution</span></span> | [<span data-ttu-id="ab9a3-136">imageInfo</span><span class="sxs-lookup"><span data-stu-id="ab9a3-136">imageInfo</span></span>](../resources/projectrome-imageinfo.md) | <span data-ttu-id="ab9a3-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-137">Optional.</span></span> <span data-ttu-id="ab9a3-138">Objeto JSON usado para representar un icono que representa la aplicación que se usa para generar la actividad</span><span class="sxs-lookup"><span data-stu-id="ab9a3-138">JSON object used to represent an icon which represents the application used to generate the activity</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ab9a3-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab9a3-139">JSON Representation</span></span>

<span data-ttu-id="ab9a3-140">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ab9a3-140">The following is a JSON representation of the resource.</span></span>

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
    "@data.type": "microsoft.graph.visualInfo",
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
        "@data.type": "microsoft.graph.Json"
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
