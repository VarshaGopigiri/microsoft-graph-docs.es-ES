---
title: Tipo de recurso auditProperty
description: Una clase que contiene las propiedades de la propiedad de auditoría.
ms.openlocfilehash: 944928014eee2e47ee0478053196bfbc1a999fc2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086567"
---
# <a name="auditproperty-resource-type"></a><span data-ttu-id="79c0f-103">Tipo de recurso auditProperty</span><span class="sxs-lookup"><span data-stu-id="79c0f-103">auditProperty resource type</span></span>

> <span data-ttu-id="79c0f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="79c0f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="79c0f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="79c0f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="79c0f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="79c0f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="79c0f-107">Una clase que contiene las propiedades de la propiedad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="79c0f-107">A class containing the properties for Audit Property.</span></span>
## <a name="properties"></a><span data-ttu-id="79c0f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79c0f-108">Properties</span></span>
|<span data-ttu-id="79c0f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="79c0f-109">Property</span></span>|<span data-ttu-id="79c0f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="79c0f-110">Type</span></span>|<span data-ttu-id="79c0f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="79c0f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="79c0f-112">displayName</span><span class="sxs-lookup"><span data-stu-id="79c0f-112">displayName</span></span>|<span data-ttu-id="79c0f-113">cadena</span><span class="sxs-lookup"><span data-stu-id="79c0f-113">String</span></span>|<span data-ttu-id="79c0f-114">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="79c0f-114">Display name.</span></span>|
|<span data-ttu-id="79c0f-115">oldValue</span><span class="sxs-lookup"><span data-stu-id="79c0f-115">oldValue</span></span>|<span data-ttu-id="79c0f-116">cadena</span><span class="sxs-lookup"><span data-stu-id="79c0f-116">String</span></span>|<span data-ttu-id="79c0f-117">Valor antiguo.</span><span class="sxs-lookup"><span data-stu-id="79c0f-117">Old value.</span></span>|
|<span data-ttu-id="79c0f-118">newValue</span><span class="sxs-lookup"><span data-stu-id="79c0f-118">newValue</span></span>|<span data-ttu-id="79c0f-119">cadena</span><span class="sxs-lookup"><span data-stu-id="79c0f-119">String</span></span>|<span data-ttu-id="79c0f-120">Valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="79c0f-120">New value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="79c0f-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="79c0f-121">Relationships</span></span>
<span data-ttu-id="79c0f-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="79c0f-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="79c0f-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="79c0f-123">JSON Representation</span></span>
<span data-ttu-id="79c0f-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="79c0f-124">Here is a JSON representation of the resource.</span></span>
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




