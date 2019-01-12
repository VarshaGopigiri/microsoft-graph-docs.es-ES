---
title: tipo de recurso imageInfo
description: Un tipo complejo para que representa la propiedad **atribución** en el elemento visualInfo del objeto de actividad.
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: a17fe40f53308a0b1b1f587425d2afb019f84bb5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982368"
---
# <a name="imageinfo-resource-type"></a><span data-ttu-id="43073-103">tipo de recurso imageInfo</span><span class="sxs-lookup"><span data-stu-id="43073-103">imageInfo resource type</span></span>

<span data-ttu-id="43073-104">Un tipo complejo para que representa la propiedad **atribución** en el elemento [visualInfo](../resources/projectrome-visualinfo.md) del objeto de [actividad](../resources/projectrome-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="43073-104">A complex type for representing the **attribution** property in the [visualInfo](../resources/projectrome-visualinfo.md) part of the [activity](../resources/projectrome-activity.md) object.</span></span>

## <a name="properties"></a><span data-ttu-id="43073-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43073-105">Properties</span></span>

|<span data-ttu-id="43073-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="43073-106">Name</span></span> | <span data-ttu-id="43073-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="43073-107">Type</span></span> | <span data-ttu-id="43073-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="43073-108">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="43073-109">iconUrl</span><span class="sxs-lookup"><span data-stu-id="43073-109">iconUrl</span></span> | <span data-ttu-id="43073-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="43073-110">String</span></span> | <span data-ttu-id="43073-111">Opcional; URI que señala a un icono que representa la aplicación que se usa para generar la actividad</span><span class="sxs-lookup"><span data-stu-id="43073-111">Optional; URI that points to an icon which represents the application used to generate the activity</span></span>|
|<span data-ttu-id="43073-112">alternateText</span><span class="sxs-lookup"><span data-stu-id="43073-112">alternateText</span></span> | <span data-ttu-id="43073-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="43073-113">String</span></span> | <span data-ttu-id="43073-114">Opcional; contenido accesible de texto alternativo para la imagen</span><span class="sxs-lookup"><span data-stu-id="43073-114">Optional; alt-text accessible content for the image</span></span>|
|<span data-ttu-id="43073-115">addImageQuery</span><span class="sxs-lookup"><span data-stu-id="43073-115">addImageQuery</span></span> | <span data-ttu-id="43073-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="43073-116">Boolean</span></span> | <span data-ttu-id="43073-117">Opcional; parámetro utilizado para indicar el servidor es capaz de procesar imagen dinámicamente en respuesta a parametrización.</span><span class="sxs-lookup"><span data-stu-id="43073-117">Optional; parameter used to indicate the server is able to render image dynamically in response to parameterization.</span></span> <span data-ttu-id="43073-118">Por ejemplo: una imagen de contraste alto</span><span class="sxs-lookup"><span data-stu-id="43073-118">For example – a high contrast image</span></span>|

## <a name="json-representation"></a><span data-ttu-id="43073-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="43073-119">JSON Representation</span></span>

<span data-ttu-id="43073-120">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="43073-120">Here is a JSON representation of the resource</span></span>

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
