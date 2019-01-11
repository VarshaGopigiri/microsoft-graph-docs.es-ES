---
title: Tipo de recurso omaSettingString
description: Definición de la cadena de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 890d636afb29fbfb188e9c1b514eecc6360001b3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841352"
---
# <a name="omasettingstring-resource-type"></a><span data-ttu-id="56203-103">Tipo de recurso omaSettingString</span><span class="sxs-lookup"><span data-stu-id="56203-103">omaSettingString resource type</span></span>

> <span data-ttu-id="56203-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56203-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56203-105">Definición de la cadena de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="56203-105">OMA Settings String definition.</span></span>

<span data-ttu-id="56203-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="56203-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="56203-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56203-107">Properties</span></span>
|<span data-ttu-id="56203-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56203-108">Property</span></span>|<span data-ttu-id="56203-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="56203-109">Type</span></span>|<span data-ttu-id="56203-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="56203-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56203-111">displayName</span><span class="sxs-lookup"><span data-stu-id="56203-111">displayName</span></span>|<span data-ttu-id="56203-112">cadena</span><span class="sxs-lookup"><span data-stu-id="56203-112">String</span></span>|<span data-ttu-id="56203-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="56203-113">Display Name.</span></span> <span data-ttu-id="56203-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="56203-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="56203-115">descripción</span><span class="sxs-lookup"><span data-stu-id="56203-115">description</span></span>|<span data-ttu-id="56203-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="56203-116">String</span></span>|<span data-ttu-id="56203-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="56203-117">Description.</span></span> <span data-ttu-id="56203-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="56203-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="56203-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="56203-119">omaUri</span></span>|<span data-ttu-id="56203-120">cadena</span><span class="sxs-lookup"><span data-stu-id="56203-120">String</span></span>|<span data-ttu-id="56203-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="56203-121">OMA.</span></span> <span data-ttu-id="56203-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="56203-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="56203-123">valor</span><span class="sxs-lookup"><span data-stu-id="56203-123">value</span></span>|<span data-ttu-id="56203-124">cadena</span><span class="sxs-lookup"><span data-stu-id="56203-124">String</span></span>|<span data-ttu-id="56203-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="56203-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="56203-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="56203-126">Relationships</span></span>
<span data-ttu-id="56203-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="56203-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="56203-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="56203-128">JSON Representation</span></span>
<span data-ttu-id="56203-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="56203-129">Here is a JSON representation of the resource.</span></span>
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



