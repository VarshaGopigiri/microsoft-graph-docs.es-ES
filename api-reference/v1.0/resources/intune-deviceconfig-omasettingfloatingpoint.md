---
title: Tipo de recurso omaSettingFloatingPoint
description: Definición de punto flotante de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: efed2112f85ee0600fcbe499616a7f3e787beb59
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360756"
---
# <a name="omasettingfloatingpoint-resource-type"></a><span data-ttu-id="0462e-103">Tipo de recurso omaSettingFloatingPoint</span><span class="sxs-lookup"><span data-stu-id="0462e-103">omaSettingFloatingPoint resource type</span></span>

> <span data-ttu-id="0462e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0462e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0462e-105">Definición de punto flotante de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="0462e-105">OMA Settings Floating Point definition.</span></span>

<span data-ttu-id="0462e-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="0462e-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="0462e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0462e-107">Properties</span></span>
|<span data-ttu-id="0462e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0462e-108">Property</span></span>|<span data-ttu-id="0462e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0462e-109">Type</span></span>|<span data-ttu-id="0462e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0462e-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0462e-111">displayName</span><span class="sxs-lookup"><span data-stu-id="0462e-111">displayName</span></span>|<span data-ttu-id="0462e-112">cadena</span><span class="sxs-lookup"><span data-stu-id="0462e-112">String</span></span>|<span data-ttu-id="0462e-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="0462e-113">Display Name.</span></span> <span data-ttu-id="0462e-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="0462e-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="0462e-115">descripción</span><span class="sxs-lookup"><span data-stu-id="0462e-115">description</span></span>|<span data-ttu-id="0462e-116">String</span><span class="sxs-lookup"><span data-stu-id="0462e-116">String</span></span>|<span data-ttu-id="0462e-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="0462e-117">Description.</span></span> <span data-ttu-id="0462e-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="0462e-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="0462e-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="0462e-119">omaUri</span></span>|<span data-ttu-id="0462e-120">cadena</span><span class="sxs-lookup"><span data-stu-id="0462e-120">String</span></span>|<span data-ttu-id="0462e-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="0462e-121">OMA.</span></span> <span data-ttu-id="0462e-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="0462e-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="0462e-123">value</span><span class="sxs-lookup"><span data-stu-id="0462e-123">value</span></span>|<span data-ttu-id="0462e-124">Simple</span><span class="sxs-lookup"><span data-stu-id="0462e-124">Single</span></span>|<span data-ttu-id="0462e-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="0462e-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0462e-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0462e-126">Relationships</span></span>
<span data-ttu-id="0462e-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0462e-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0462e-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0462e-128">JSON Representation</span></span>
<span data-ttu-id="0462e-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0462e-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingFloatingPoint"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingFloatingPoint",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "<Unknown Primitive Type Edm.Single>"
}
```



