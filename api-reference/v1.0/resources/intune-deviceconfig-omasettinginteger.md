---
title: Tipo de recurso omaSettingInteger
description: Definición del entero de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f40d5d225c2b4b99573c482b39f886bcd463e9fe
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860455"
---
# <a name="omasettinginteger-resource-type"></a><span data-ttu-id="187b6-103">Tipo de recurso omaSettingInteger</span><span class="sxs-lookup"><span data-stu-id="187b6-103">omaSettingInteger resource type</span></span>

> <span data-ttu-id="187b6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="187b6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="187b6-105">Definición del entero de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="187b6-105">OMA Settings Integer definition.</span></span>

<span data-ttu-id="187b6-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="187b6-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="187b6-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="187b6-107">Properties</span></span>
|<span data-ttu-id="187b6-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="187b6-108">Property</span></span>|<span data-ttu-id="187b6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="187b6-109">Type</span></span>|<span data-ttu-id="187b6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="187b6-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="187b6-111">displayName</span><span class="sxs-lookup"><span data-stu-id="187b6-111">displayName</span></span>|<span data-ttu-id="187b6-112">cadena</span><span class="sxs-lookup"><span data-stu-id="187b6-112">String</span></span>|<span data-ttu-id="187b6-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="187b6-113">Display Name.</span></span> <span data-ttu-id="187b6-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="187b6-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="187b6-115">descripción</span><span class="sxs-lookup"><span data-stu-id="187b6-115">description</span></span>|<span data-ttu-id="187b6-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="187b6-116">String</span></span>|<span data-ttu-id="187b6-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="187b6-117">Description.</span></span> <span data-ttu-id="187b6-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="187b6-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="187b6-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="187b6-119">omaUri</span></span>|<span data-ttu-id="187b6-120">cadena</span><span class="sxs-lookup"><span data-stu-id="187b6-120">String</span></span>|<span data-ttu-id="187b6-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="187b6-121">OMA.</span></span> <span data-ttu-id="187b6-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="187b6-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="187b6-123">valor</span><span class="sxs-lookup"><span data-stu-id="187b6-123">value</span></span>|<span data-ttu-id="187b6-124">Int32</span><span class="sxs-lookup"><span data-stu-id="187b6-124">Int32</span></span>|<span data-ttu-id="187b6-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="187b6-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="187b6-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="187b6-126">Relationships</span></span>
<span data-ttu-id="187b6-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="187b6-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="187b6-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="187b6-128">JSON Representation</span></span>
<span data-ttu-id="187b6-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="187b6-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingInteger"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingInteger",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": 1024
}
```



