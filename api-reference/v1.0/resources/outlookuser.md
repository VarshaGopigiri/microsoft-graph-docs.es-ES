---
title: Tipo de recurso outlookUser
description: Representa los servicios de Outlook disponibles para un usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 32d621b71770d220487b60b4573fb34cdf28d526
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982823"
---
# <a name="outlookuser-resource-type"></a><span data-ttu-id="2c36b-103">Tipo de recurso outlookUser</span><span class="sxs-lookup"><span data-stu-id="2c36b-103">outlookUser resource type</span></span>


<span data-ttu-id="2c36b-104">Representa los servicios de Outlook disponibles para un usuario.</span><span class="sxs-lookup"><span data-stu-id="2c36b-104">Represents the Outlook services available to a user.</span></span>


## <a name="methods"></a><span data-ttu-id="2c36b-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c36b-105">Methods</span></span>

| <span data-ttu-id="2c36b-106">Método</span><span class="sxs-lookup"><span data-stu-id="2c36b-106">Method</span></span>           | <span data-ttu-id="2c36b-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c36b-107">Return Type</span></span>    |<span data-ttu-id="2c36b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c36b-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2c36b-109">Crear categoría</span><span class="sxs-lookup"><span data-stu-id="2c36b-109">Create category</span></span>](../api/outlookuser-post-mastercategories.md) | [<span data-ttu-id="2c36b-110">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="2c36b-110">outlookCategory</span></span>](outlookcategory.md) |<span data-ttu-id="2c36b-111">Crear un objeto **outlookCategory** en la lista principal de categorías del usuario.</span><span class="sxs-lookup"><span data-stu-id="2c36b-111">Create an **outlookCategory** object in the user's master list of categories.</span></span>|
|[<span data-ttu-id="2c36b-112">Enumerar categorías</span><span class="sxs-lookup"><span data-stu-id="2c36b-112">List categories</span></span>](../api/outlookuser-list-mastercategories.md) | <span data-ttu-id="2c36b-113">Colección [outlookCategory](outlookcategory.md)</span><span class="sxs-lookup"><span data-stu-id="2c36b-113">[outlookCategory](outlookcategory.md) collection</span></span> |<span data-ttu-id="2c36b-114">Obtener todas las categorías que han sido definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2c36b-114">Get all the categories that have been defined for the user.</span></span>|
|[<span data-ttu-id="2c36b-115">supportedLanguages</span><span class="sxs-lookup"><span data-stu-id="2c36b-115">supportedLanguages</span></span>](../api/outlookuser-supportedlanguages.md) | <span data-ttu-id="2c36b-116">Colección [localeInfo](localeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="2c36b-116">[localeInfo](localeinfo.md) collection</span></span> | <span data-ttu-id="2c36b-117">Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="2c36b-117">Get the list of locales and languages that is supported for the user, as configured on the user's mailbox server.</span></span> |
|[<span data-ttu-id="2c36b-118">supportedTimeZones</span><span class="sxs-lookup"><span data-stu-id="2c36b-118">supportedTimeZones</span></span>](../api/outlookuser-supportedtimezones.md) | <span data-ttu-id="2c36b-119">Colección [timeZoneInformation](timezoneinformation.md)</span><span class="sxs-lookup"><span data-stu-id="2c36b-119">[timeZoneInformation](timezoneinformation.md) collection</span></span> | <span data-ttu-id="2c36b-120">Obtener una lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="2c36b-120">Get the list of time zones that is supported for the user, as configured on the user's mailbox server.</span></span> |


## <a name="properties"></a><span data-ttu-id="2c36b-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c36b-121">Properties</span></span>
<span data-ttu-id="2c36b-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2c36b-122">None</span></span>

## <a name="relationships"></a><span data-ttu-id="2c36b-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2c36b-123">Relationships</span></span>
| <span data-ttu-id="2c36b-124">Relación</span><span class="sxs-lookup"><span data-stu-id="2c36b-124">Relationship</span></span> | <span data-ttu-id="2c36b-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c36b-125">Type</span></span>   |<span data-ttu-id="2c36b-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c36b-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2c36b-127">masterCategories</span><span class="sxs-lookup"><span data-stu-id="2c36b-127">masterCategories</span></span>|<span data-ttu-id="2c36b-128">Colección [outlookCategory](../resources/outlookcategory.md)</span><span class="sxs-lookup"><span data-stu-id="2c36b-128">[outlookCategory](../resources/outlookcategory.md) collection</span></span>| <span data-ttu-id="2c36b-129">Lista de categorías definidas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="2c36b-129">A list of categories defined for the user.</span></span> | 

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.outlookUser",
  "@odata.annotations": [
    {
      "property": "masterCategories",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    }
  ]
}-->
```json
{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
