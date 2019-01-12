---
title: Tipo de recurso auditProperty
description: Una clase que contiene las propiedades de la propiedad de auditoría.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: bd251fa942d526b01abca4191f041eb5a76745e5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952268"
---
# <a name="auditproperty-resource-type"></a><span data-ttu-id="92716-103">Tipo de recurso auditProperty</span><span class="sxs-lookup"><span data-stu-id="92716-103">auditProperty resource type</span></span>

> <span data-ttu-id="92716-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="92716-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="92716-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="92716-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="92716-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="92716-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="92716-107">Una clase que contiene las propiedades de la propiedad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="92716-107">A class containing the properties for Audit Property.</span></span>
## <a name="properties"></a><span data-ttu-id="92716-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92716-108">Properties</span></span>
|<span data-ttu-id="92716-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92716-109">Property</span></span>|<span data-ttu-id="92716-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="92716-110">Type</span></span>|<span data-ttu-id="92716-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="92716-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="92716-112">displayName</span><span class="sxs-lookup"><span data-stu-id="92716-112">displayName</span></span>|<span data-ttu-id="92716-113">cadena</span><span class="sxs-lookup"><span data-stu-id="92716-113">String</span></span>|<span data-ttu-id="92716-114">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="92716-114">Display name.</span></span>|
|<span data-ttu-id="92716-115">oldValue</span><span class="sxs-lookup"><span data-stu-id="92716-115">oldValue</span></span>|<span data-ttu-id="92716-116">cadena</span><span class="sxs-lookup"><span data-stu-id="92716-116">String</span></span>|<span data-ttu-id="92716-117">Valor antiguo.</span><span class="sxs-lookup"><span data-stu-id="92716-117">Old value.</span></span>|
|<span data-ttu-id="92716-118">newValue</span><span class="sxs-lookup"><span data-stu-id="92716-118">newValue</span></span>|<span data-ttu-id="92716-119">cadena</span><span class="sxs-lookup"><span data-stu-id="92716-119">String</span></span>|<span data-ttu-id="92716-120">Valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="92716-120">New value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="92716-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="92716-121">Relationships</span></span>
<span data-ttu-id="92716-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="92716-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="92716-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="92716-123">JSON Representation</span></span>
<span data-ttu-id="92716-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="92716-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditProperty"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditProperty",
  "displayName": "String",
  "oldValue": "String",
  "newValue": "String"
}
```





