---
title: Tipo de recurso omaSettingBoolean
description: Definición booleana de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: 10101217d1c0f07931cb847e1c14f36844c8dc9b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323285"
---
# <a name="omasettingboolean-resource-type"></a><span data-ttu-id="a4dcd-103">Tipo de recurso omaSettingBoolean</span><span class="sxs-lookup"><span data-stu-id="a4dcd-103">omaSettingBoolean resource type</span></span>

> <span data-ttu-id="a4dcd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4dcd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4dcd-105">Definición booleana de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="a4dcd-105">OMA Settings Boolean definition.</span></span>

<span data-ttu-id="a4dcd-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="a4dcd-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="a4dcd-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4dcd-107">Properties</span></span>
|<span data-ttu-id="a4dcd-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4dcd-108">Property</span></span>|<span data-ttu-id="a4dcd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4dcd-109">Type</span></span>|<span data-ttu-id="a4dcd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4dcd-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4dcd-111">displayName</span><span class="sxs-lookup"><span data-stu-id="a4dcd-111">displayName</span></span>|<span data-ttu-id="a4dcd-112">cadena</span><span class="sxs-lookup"><span data-stu-id="a4dcd-112">String</span></span>|<span data-ttu-id="a4dcd-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="a4dcd-113">Display Name.</span></span> <span data-ttu-id="a4dcd-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="a4dcd-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="a4dcd-115">descripción</span><span class="sxs-lookup"><span data-stu-id="a4dcd-115">description</span></span>|<span data-ttu-id="a4dcd-116">String</span><span class="sxs-lookup"><span data-stu-id="a4dcd-116">String</span></span>|<span data-ttu-id="a4dcd-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="a4dcd-117">Description.</span></span> <span data-ttu-id="a4dcd-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="a4dcd-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="a4dcd-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="a4dcd-119">omaUri</span></span>|<span data-ttu-id="a4dcd-120">cadena</span><span class="sxs-lookup"><span data-stu-id="a4dcd-120">String</span></span>|<span data-ttu-id="a4dcd-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="a4dcd-121">OMA.</span></span> <span data-ttu-id="a4dcd-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="a4dcd-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="a4dcd-123">valor</span><span class="sxs-lookup"><span data-stu-id="a4dcd-123">value</span></span>|<span data-ttu-id="a4dcd-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4dcd-124">Boolean</span></span>|<span data-ttu-id="a4dcd-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="a4dcd-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a4dcd-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a4dcd-126">Relationships</span></span>
<span data-ttu-id="a4dcd-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a4dcd-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a4dcd-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a4dcd-128">JSON Representation</span></span>
<span data-ttu-id="a4dcd-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a4dcd-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingBoolean"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingBoolean",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": true
}
```



