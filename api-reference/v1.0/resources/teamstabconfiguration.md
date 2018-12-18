---
title: tipo de recurso teamsTabConfiguration (Open Type)
description: La configuración que determinan el contenido de una ficha.
author: nkramer
ms.openlocfilehash: 281d27dfec1efa83859fad262e1b25fd06b5f4cc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344964"
---
# <a name="teamstabconfiguration-resource-type-open-type"></a><span data-ttu-id="f12fb-103">tipo de recurso teamsTabConfiguration (Open Type)</span><span class="sxs-lookup"><span data-stu-id="f12fb-103">teamsTabConfiguration resource type (Open Type)</span></span>



<span data-ttu-id="f12fb-104">La configuración que determinan el contenido de una [ficha](teamstab.md). Cuando una ficha de forma interactiva se configura, esta información se establece mediante la aplicación de proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="f12fb-104">The settings that determine the content of a [tab](teamstab.md). When a tab is interactively configured, this information is set by the tab provider application.</span></span>
<span data-ttu-id="f12fb-105">Además de las propiedades que aparece a continuación, algunas aplicaciones de proveedor de la ficha especifican propiedades personalizadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="f12fb-105">In addition to the properties below, some tab provider applications specify additional custom properties.</span></span>

## <a name="properties"></a><span data-ttu-id="f12fb-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f12fb-106">Properties</span></span>

|<span data-ttu-id="f12fb-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f12fb-107">Property</span></span>|<span data-ttu-id="f12fb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f12fb-108">Type</span></span>|<span data-ttu-id="f12fb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f12fb-109">Description</span></span>|
|-|-|-|
|  <span data-ttu-id="f12fb-110">entityId</span><span class="sxs-lookup"><span data-stu-id="f12fb-110">entityId</span></span>   |   <span data-ttu-id="f12fb-111">string</span><span class="sxs-lookup"><span data-stu-id="f12fb-111">string</span></span> |  <span data-ttu-id="f12fb-112">Identificador de la entidad hospedada por el proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="f12fb-112">Identifier for the entity hosted by the tab provider.</span></span>     |
|  <span data-ttu-id="f12fb-113">contentUrl</span><span class="sxs-lookup"><span data-stu-id="f12fb-113">contentUrl</span></span> |   <span data-ttu-id="f12fb-114">string</span><span class="sxs-lookup"><span data-stu-id="f12fb-114">string</span></span> |  <span data-ttu-id="f12fb-115">Dirección URL utilizada para representar el contenido de la ficha en los equipos.</span><span class="sxs-lookup"><span data-stu-id="f12fb-115">Url used for rendering tab contents in Teams.</span></span> <span data-ttu-id="f12fb-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f12fb-116">Required.</span></span>    |
|  <span data-ttu-id="f12fb-117">removeUrl</span><span class="sxs-lookup"><span data-stu-id="f12fb-117">removeUrl</span></span>  |   <span data-ttu-id="f12fb-118">string</span><span class="sxs-lookup"><span data-stu-id="f12fb-118">string</span></span> |  <span data-ttu-id="f12fb-119">Dirección URL de los equipos cliente llamado cuando se quita una ficha mediante el cliente de los equipos.</span><span class="sxs-lookup"><span data-stu-id="f12fb-119">Url called by Teams client when a Tab is removed using the Teams Client.</span></span>     |
|  <span data-ttu-id="f12fb-120">websiteUrl</span><span class="sxs-lookup"><span data-stu-id="f12fb-120">websiteUrl</span></span> |   <span data-ttu-id="f12fb-121">string</span><span class="sxs-lookup"><span data-stu-id="f12fb-121">string</span></span> |  <span data-ttu-id="f12fb-122">Dirección URL para mostrar el contenido de la ficha fuera de los equipos.</span><span class="sxs-lookup"><span data-stu-id="f12fb-122">Url for showing tab contents outside of Teams.</span></span>     |

## <a name="json-representation"></a><span data-ttu-id="f12fb-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f12fb-123">JSON representation</span></span>

<span data-ttu-id="f12fb-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f12fb-124">The following is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsTabConfiguration"
}-->

```json
{
   "entityId": "string",
   "contentUrl": "string (HTTPS Url)",
   "websiteUrl": "string (HTTPS Url)",
   "removeUrl": "string (HTTPS Url)"  
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsTabConfiguration complex type (Open Type)",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
