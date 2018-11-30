---
title: tipo de recurso teamsTabConfiguration (Open Type)
description: La configuración que determinan el contenido de una ficha.
ms.openlocfilehash: b9a638692302dc8d301c3b14e50096b08891d821
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084379"
---
# <a name="teamstabconfiguration-resource-type-open-type"></a><span data-ttu-id="e0fc5-103">tipo de recurso teamsTabConfiguration (Open Type)</span><span class="sxs-lookup"><span data-stu-id="e0fc5-103">teamsTabConfiguration resource type (Open Type)</span></span>

> <span data-ttu-id="e0fc5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e0fc5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e0fc5-106">La configuración que determinan el contenido de una [ficha](teamstab.md). Cuando una ficha de forma interactiva se configura, esta información se establece mediante la aplicación de proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-106">The settings that determine the content of a [tab](teamstab.md). When a tab is interactively configured, this information is set by the tab provider application.</span></span>
<span data-ttu-id="e0fc5-107">Además de las propiedades que aparece a continuación, algunas aplicaciones de proveedor de la ficha especifican propiedades personalizadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-107">In addition to the properties below, some tab provider applications specify additional custom properties.</span></span>

## <a name="properties"></a><span data-ttu-id="e0fc5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0fc5-108">Properties</span></span>

|<span data-ttu-id="e0fc5-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0fc5-109">Property</span></span>|<span data-ttu-id="e0fc5-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0fc5-110">Type</span></span>|<span data-ttu-id="e0fc5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0fc5-111">Description</span></span>|
|-|-|-|
|  <span data-ttu-id="e0fc5-112">entityId</span><span class="sxs-lookup"><span data-stu-id="e0fc5-112">entityId</span></span>   |   <span data-ttu-id="e0fc5-113">string</span><span class="sxs-lookup"><span data-stu-id="e0fc5-113">string</span></span> |  <span data-ttu-id="e0fc5-114">Identificador de la entidad hospedada por el proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-114">Identifier for the entity hosted by the tab provider.</span></span>     |
|  <span data-ttu-id="e0fc5-115">contentUrl</span><span class="sxs-lookup"><span data-stu-id="e0fc5-115">contentUrl</span></span> |   <span data-ttu-id="e0fc5-116">string</span><span class="sxs-lookup"><span data-stu-id="e0fc5-116">string</span></span> |  <span data-ttu-id="e0fc5-117">Dirección URL utilizada para representar el contenido de la ficha en los equipos.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-117">Url used for rendering tab contents in Teams.</span></span> <span data-ttu-id="e0fc5-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-118">Required.</span></span>    |
|  <span data-ttu-id="e0fc5-119">removeUrl</span><span class="sxs-lookup"><span data-stu-id="e0fc5-119">removeUrl</span></span>  |   <span data-ttu-id="e0fc5-120">string</span><span class="sxs-lookup"><span data-stu-id="e0fc5-120">string</span></span> |  <span data-ttu-id="e0fc5-121">Dirección URL de los equipos cliente llamado cuando se quita una ficha mediante el cliente de los equipos.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-121">Url called by Teams client when a Tab is removed using the Teams Client.</span></span>     |
|  <span data-ttu-id="e0fc5-122">websiteUrl</span><span class="sxs-lookup"><span data-stu-id="e0fc5-122">websiteUrl</span></span> |   <span data-ttu-id="e0fc5-123">string</span><span class="sxs-lookup"><span data-stu-id="e0fc5-123">string</span></span> |  <span data-ttu-id="e0fc5-124">Dirección URL para mostrar el contenido de la ficha fuera de los equipos.</span><span class="sxs-lookup"><span data-stu-id="e0fc5-124">Url for showing tab contents outside of Teams.</span></span>     |

## <a name="json-representation"></a><span data-ttu-id="e0fc5-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e0fc5-125">JSON representation</span></span>

<span data-ttu-id="e0fc5-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e0fc5-126">The following is a JSON representation of the resource.</span></span>
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
