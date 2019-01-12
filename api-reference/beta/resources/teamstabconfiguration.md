---
title: tipo de recurso teamsTabConfiguration (Open Type)
description: La configuración que determinan el contenido de una ficha.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 515e5896591b58054f161ff740f68b0ca4913663
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913488"
---
# <a name="teamstabconfiguration-resource-type-open-type"></a><span data-ttu-id="15775-103">tipo de recurso teamsTabConfiguration (Open Type)</span><span class="sxs-lookup"><span data-stu-id="15775-103">teamsTabConfiguration resource type (Open Type)</span></span>

> <span data-ttu-id="15775-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="15775-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="15775-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="15775-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="15775-106">La configuración que determinan el contenido de una [ficha](teamstab.md). Cuando una ficha de forma interactiva se configura, esta información se establece mediante la aplicación de proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="15775-106">The settings that determine the content of a [tab](teamstab.md). When a tab is interactively configured, this information is set by the tab provider application.</span></span>
<span data-ttu-id="15775-107">Además de las propiedades que aparece a continuación, algunas aplicaciones de proveedor de la ficha especifican propiedades personalizadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="15775-107">In addition to the properties below, some tab provider applications specify additional custom properties.</span></span>

## <a name="properties"></a><span data-ttu-id="15775-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15775-108">Properties</span></span>

|<span data-ttu-id="15775-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15775-109">Property</span></span>|<span data-ttu-id="15775-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="15775-110">Type</span></span>|<span data-ttu-id="15775-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="15775-111">Description</span></span>|
|-|-|-|
|  <span data-ttu-id="15775-112">entityId</span><span class="sxs-lookup"><span data-stu-id="15775-112">entityId</span></span>   |   <span data-ttu-id="15775-113">string</span><span class="sxs-lookup"><span data-stu-id="15775-113">string</span></span> |  <span data-ttu-id="15775-114">Identificador de la entidad hospedada por el proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="15775-114">Identifier for the entity hosted by the tab provider.</span></span>     |
|  <span data-ttu-id="15775-115">contentUrl</span><span class="sxs-lookup"><span data-stu-id="15775-115">contentUrl</span></span> |   <span data-ttu-id="15775-116">string</span><span class="sxs-lookup"><span data-stu-id="15775-116">string</span></span> |  <span data-ttu-id="15775-117">Dirección URL utilizada para representar el contenido de la ficha en los equipos.</span><span class="sxs-lookup"><span data-stu-id="15775-117">Url used for rendering tab contents in Teams.</span></span> <span data-ttu-id="15775-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15775-118">Required.</span></span>    |
|  <span data-ttu-id="15775-119">removeUrl</span><span class="sxs-lookup"><span data-stu-id="15775-119">removeUrl</span></span>  |   <span data-ttu-id="15775-120">string</span><span class="sxs-lookup"><span data-stu-id="15775-120">string</span></span> |  <span data-ttu-id="15775-121">Dirección URL de los equipos cliente llamado cuando se quita una ficha mediante el cliente de los equipos.</span><span class="sxs-lookup"><span data-stu-id="15775-121">Url called by Teams client when a Tab is removed using the Teams Client.</span></span>     |
|  <span data-ttu-id="15775-122">websiteUrl</span><span class="sxs-lookup"><span data-stu-id="15775-122">websiteUrl</span></span> |   <span data-ttu-id="15775-123">string</span><span class="sxs-lookup"><span data-stu-id="15775-123">string</span></span> |  <span data-ttu-id="15775-124">Dirección URL para mostrar el contenido de la ficha fuera de los equipos.</span><span class="sxs-lookup"><span data-stu-id="15775-124">Url for showing tab contents outside of Teams.</span></span>     |

## <a name="json-representation"></a><span data-ttu-id="15775-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="15775-125">JSON representation</span></span>

<span data-ttu-id="15775-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="15775-126">The following is a JSON representation of the resource.</span></span>
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
