---
title: tipo de recurso imageInfo
description: Un tipo complejo para que representa la propiedad **atribución** en el elemento visualInfo del objeto de actividad.
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: 347e07b70e8bad6dce8571dd1fbac5cd00d9abdd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978693"
---
# <a name="imageinfo-resource-type"></a><span data-ttu-id="4cf04-103">tipo de recurso imageInfo</span><span class="sxs-lookup"><span data-stu-id="4cf04-103">imageInfo resource type</span></span>

> <span data-ttu-id="4cf04-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4cf04-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4cf04-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4cf04-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4cf04-106">Un tipo complejo para que representa la propiedad **atribución** en el elemento [visualInfo](../resources/projectrome-visualinfo.md) del objeto de [actividad](../resources/projectrome-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="4cf04-106">A complex type for representing the **attribution** property in the [visualInfo](../resources/projectrome-visualinfo.md) part of the [activity](../resources/projectrome-activity.md) object.</span></span>

## <a name="properties"></a><span data-ttu-id="4cf04-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4cf04-107">Properties</span></span>

|<span data-ttu-id="4cf04-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="4cf04-108">Name</span></span> | <span data-ttu-id="4cf04-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4cf04-109">Type</span></span> | <span data-ttu-id="4cf04-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cf04-110">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="4cf04-111">iconUrl</span><span class="sxs-lookup"><span data-stu-id="4cf04-111">iconUrl</span></span> | <span data-ttu-id="4cf04-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="4cf04-112">String</span></span> | <span data-ttu-id="4cf04-113">Opcional; URI que señala a un icono que representa la aplicación que se usa para generar la actividad</span><span class="sxs-lookup"><span data-stu-id="4cf04-113">Optional; URI that points to an icon which represents the application used to generate the activity</span></span>|
|<span data-ttu-id="4cf04-114">alternateText</span><span class="sxs-lookup"><span data-stu-id="4cf04-114">alternateText</span></span> | <span data-ttu-id="4cf04-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="4cf04-115">String</span></span> | <span data-ttu-id="4cf04-116">Opcional; contenido accesible de texto alternativo para la imagen</span><span class="sxs-lookup"><span data-stu-id="4cf04-116">Optional; alt-text accessible content for the image</span></span>|
|<span data-ttu-id="4cf04-117">addImageQuery</span><span class="sxs-lookup"><span data-stu-id="4cf04-117">addImageQuery</span></span> | <span data-ttu-id="4cf04-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="4cf04-118">Boolean</span></span> | <span data-ttu-id="4cf04-119">Opcional; parámetro utilizado para indicar el servidor es capaz de procesar imagen dinámicamente en respuesta a parametrización.</span><span class="sxs-lookup"><span data-stu-id="4cf04-119">Optional; parameter used to indicate the server is able to render image dynamically in response to parameterization.</span></span> <span data-ttu-id="4cf04-120">Por ejemplo: una imagen de contraste alto</span><span class="sxs-lookup"><span data-stu-id="4cf04-120">For example – a high contrast image</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4cf04-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4cf04-121">JSON Representation</span></span>

<span data-ttu-id="4cf04-122">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4cf04-122">Here is a JSON representation of the resource</span></span>

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
