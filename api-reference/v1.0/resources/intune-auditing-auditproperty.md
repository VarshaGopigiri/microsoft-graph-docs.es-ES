---
title: Tipo de recurso auditProperty
description: Una clase que contiene las propiedades de la propiedad de auditoría.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e91f3771be981f6ff410e8774f6a8ac9fbc121dd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870920"
---
# <a name="auditproperty-resource-type"></a><span data-ttu-id="008b0-103">Tipo de recurso auditProperty</span><span class="sxs-lookup"><span data-stu-id="008b0-103">auditProperty resource type</span></span>

> <span data-ttu-id="008b0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="008b0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="008b0-105">Una clase que contiene las propiedades de la propiedad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="008b0-105">A class containing the properties for Audit Property.</span></span>
## <a name="properties"></a><span data-ttu-id="008b0-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="008b0-106">Properties</span></span>
|<span data-ttu-id="008b0-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="008b0-107">Property</span></span>|<span data-ttu-id="008b0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="008b0-108">Type</span></span>|<span data-ttu-id="008b0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="008b0-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="008b0-110">displayName</span><span class="sxs-lookup"><span data-stu-id="008b0-110">displayName</span></span>|<span data-ttu-id="008b0-111">cadena</span><span class="sxs-lookup"><span data-stu-id="008b0-111">String</span></span>|<span data-ttu-id="008b0-112">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="008b0-112">Display name.</span></span>|
|<span data-ttu-id="008b0-113">oldValue</span><span class="sxs-lookup"><span data-stu-id="008b0-113">oldValue</span></span>|<span data-ttu-id="008b0-114">cadena</span><span class="sxs-lookup"><span data-stu-id="008b0-114">String</span></span>|<span data-ttu-id="008b0-115">Valor antiguo.</span><span class="sxs-lookup"><span data-stu-id="008b0-115">Old value.</span></span>|
|<span data-ttu-id="008b0-116">newValue</span><span class="sxs-lookup"><span data-stu-id="008b0-116">newValue</span></span>|<span data-ttu-id="008b0-117">cadena</span><span class="sxs-lookup"><span data-stu-id="008b0-117">String</span></span>|<span data-ttu-id="008b0-118">Valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="008b0-118">New value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="008b0-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="008b0-119">Relationships</span></span>
<span data-ttu-id="008b0-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="008b0-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="008b0-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="008b0-121">JSON Representation</span></span>
<span data-ttu-id="008b0-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="008b0-122">Here is a JSON representation of the resource.</span></span>
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



