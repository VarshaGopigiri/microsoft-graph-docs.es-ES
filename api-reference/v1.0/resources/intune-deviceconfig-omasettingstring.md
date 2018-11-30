---
title: Tipo de recurso omaSettingString
description: Definición de la cadena de la configuración de OMA.
ms.openlocfilehash: 543b993ee557c47e415a2f19f9791b0685c818e0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029578"
---
# <a name="omasettingstring-resource-type"></a><span data-ttu-id="e255f-103">Tipo de recurso omaSettingString</span><span class="sxs-lookup"><span data-stu-id="e255f-103">omaSettingString resource type</span></span>

> <span data-ttu-id="e255f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e255f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e255f-105">Definición de la cadena de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="e255f-105">OMA Settings String definition.</span></span>

<span data-ttu-id="e255f-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e255f-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e255f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e255f-107">Properties</span></span>
|<span data-ttu-id="e255f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e255f-108">Property</span></span>|<span data-ttu-id="e255f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e255f-109">Type</span></span>|<span data-ttu-id="e255f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e255f-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e255f-111">displayName</span><span class="sxs-lookup"><span data-stu-id="e255f-111">displayName</span></span>|<span data-ttu-id="e255f-112">cadena</span><span class="sxs-lookup"><span data-stu-id="e255f-112">String</span></span>|<span data-ttu-id="e255f-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e255f-113">Display Name.</span></span> <span data-ttu-id="e255f-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e255f-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="e255f-115">descripción</span><span class="sxs-lookup"><span data-stu-id="e255f-115">description</span></span>|<span data-ttu-id="e255f-116">String</span><span class="sxs-lookup"><span data-stu-id="e255f-116">String</span></span>|<span data-ttu-id="e255f-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="e255f-117">Description.</span></span> <span data-ttu-id="e255f-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e255f-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="e255f-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="e255f-119">omaUri</span></span>|<span data-ttu-id="e255f-120">cadena</span><span class="sxs-lookup"><span data-stu-id="e255f-120">String</span></span>|<span data-ttu-id="e255f-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="e255f-121">OMA.</span></span> <span data-ttu-id="e255f-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e255f-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="e255f-123">valor</span><span class="sxs-lookup"><span data-stu-id="e255f-123">value</span></span>|<span data-ttu-id="e255f-124">cadena</span><span class="sxs-lookup"><span data-stu-id="e255f-124">String</span></span>|<span data-ttu-id="e255f-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="e255f-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e255f-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e255f-126">Relationships</span></span>
<span data-ttu-id="e255f-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e255f-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e255f-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e255f-128">JSON Representation</span></span>
<span data-ttu-id="e255f-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e255f-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingString"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingString",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String"
}
```



