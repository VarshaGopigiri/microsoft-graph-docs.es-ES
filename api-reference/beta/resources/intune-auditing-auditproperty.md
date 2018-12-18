---
title: Tipo de recurso auditProperty
description: Una clase que contiene las propiedades de la propiedad de auditoría.
author: tfitzmac
ms.openlocfilehash: 801ac78cb81e126ff49c4c680fc0624611a9f6d6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316320"
---
# <a name="auditproperty-resource-type"></a><span data-ttu-id="16e17-103">Tipo de recurso auditProperty</span><span class="sxs-lookup"><span data-stu-id="16e17-103">auditProperty resource type</span></span>

> <span data-ttu-id="16e17-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16e17-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16e17-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16e17-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="16e17-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16e17-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16e17-107">Una clase que contiene las propiedades de la propiedad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="16e17-107">A class containing the properties for Audit Property.</span></span>
## <a name="properties"></a><span data-ttu-id="16e17-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16e17-108">Properties</span></span>
|<span data-ttu-id="16e17-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16e17-109">Property</span></span>|<span data-ttu-id="16e17-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="16e17-110">Type</span></span>|<span data-ttu-id="16e17-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="16e17-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16e17-112">displayName</span><span class="sxs-lookup"><span data-stu-id="16e17-112">displayName</span></span>|<span data-ttu-id="16e17-113">cadena</span><span class="sxs-lookup"><span data-stu-id="16e17-113">String</span></span>|<span data-ttu-id="16e17-114">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="16e17-114">Display name.</span></span>|
|<span data-ttu-id="16e17-115">oldValue</span><span class="sxs-lookup"><span data-stu-id="16e17-115">oldValue</span></span>|<span data-ttu-id="16e17-116">cadena</span><span class="sxs-lookup"><span data-stu-id="16e17-116">String</span></span>|<span data-ttu-id="16e17-117">Valor antiguo.</span><span class="sxs-lookup"><span data-stu-id="16e17-117">Old value.</span></span>|
|<span data-ttu-id="16e17-118">newValue</span><span class="sxs-lookup"><span data-stu-id="16e17-118">newValue</span></span>|<span data-ttu-id="16e17-119">cadena</span><span class="sxs-lookup"><span data-stu-id="16e17-119">String</span></span>|<span data-ttu-id="16e17-120">Valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="16e17-120">New value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="16e17-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="16e17-121">Relationships</span></span>
<span data-ttu-id="16e17-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="16e17-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="16e17-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16e17-123">JSON Representation</span></span>
<span data-ttu-id="16e17-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="16e17-124">Here is a JSON representation of the resource.</span></span>
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





