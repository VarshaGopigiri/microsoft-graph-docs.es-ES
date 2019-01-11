---
title: tipo de recurso imageInfo
description: Un tipo complejo para que representa la propiedad **atribución** en el elemento visualInfo del objeto de actividad.
localization_priority: Normal
ms.openlocfilehash: 2bac97ff945c0e0975ffa19636a954308b895e88
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856465"
---
# <a name="imageinfo-resource-type"></a><span data-ttu-id="03e49-103">tipo de recurso imageInfo</span><span class="sxs-lookup"><span data-stu-id="03e49-103">imageInfo resource type</span></span>

<span data-ttu-id="03e49-104">Un tipo complejo para que representa la propiedad **atribución** en el elemento [visualInfo](../resources/projectrome-visualinfo.md) del objeto de [actividad](../resources/projectrome-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="03e49-104">A complex type for representing the **attribution** property in the [visualInfo](../resources/projectrome-visualinfo.md) part of the [activity](../resources/projectrome-activity.md) object.</span></span>

## <a name="properties"></a><span data-ttu-id="03e49-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03e49-105">Properties</span></span>

|<span data-ttu-id="03e49-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="03e49-106">Name</span></span> | <span data-ttu-id="03e49-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="03e49-107">Type</span></span> | <span data-ttu-id="03e49-108">Description</span><span class="sxs-lookup"><span data-stu-id="03e49-108">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="03e49-109">iconUrl</span><span class="sxs-lookup"><span data-stu-id="03e49-109">iconUrl</span></span> | <span data-ttu-id="03e49-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="03e49-110">String</span></span> | <span data-ttu-id="03e49-111">Opcional; URI que señala a un icono que representa la aplicación que se usa para generar la actividad</span><span class="sxs-lookup"><span data-stu-id="03e49-111">Optional; URI that points to an icon which represents the application used to generate the activity</span></span>|
|<span data-ttu-id="03e49-112">alternateText</span><span class="sxs-lookup"><span data-stu-id="03e49-112">alternateText</span></span> | <span data-ttu-id="03e49-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="03e49-113">String</span></span> | <span data-ttu-id="03e49-114">Opcional; contenido accesible de texto alternativo para la imagen</span><span class="sxs-lookup"><span data-stu-id="03e49-114">Optional; alt-text accessible content for the image</span></span>|
|<span data-ttu-id="03e49-115">addImageQuery</span><span class="sxs-lookup"><span data-stu-id="03e49-115">addImageQuery</span></span> | <span data-ttu-id="03e49-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="03e49-116">Boolean</span></span> | <span data-ttu-id="03e49-117">Opcional; parámetro utilizado para indicar el servidor es capaz de procesar imagen dinámicamente en respuesta a parametrización.</span><span class="sxs-lookup"><span data-stu-id="03e49-117">Optional; parameter used to indicate the server is able to render image dynamically in response to parameterization.</span></span> <span data-ttu-id="03e49-118">Por ejemplo: una imagen de contraste alto</span><span class="sxs-lookup"><span data-stu-id="03e49-118">For example – a high contrast image</span></span>|

## <a name="json-representation"></a><span data-ttu-id="03e49-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="03e49-119">JSON Representation</span></span>

<span data-ttu-id="03e49-120">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="03e49-120">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "iconUrl",
    "alternateText",
    "addImageQuery"
  ],
  "@odata.type": "microsoft.graph.imageInfo"
}-->

```json
{
    "@odata.type": "microsoft.graph.imageInfo",
    "iconUrl": "String (URL)",
    "alternateText": "String",
    "addImageQuery": "boolean"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "imageinfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
