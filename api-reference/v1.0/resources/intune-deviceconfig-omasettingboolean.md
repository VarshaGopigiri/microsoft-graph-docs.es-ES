---
title: Tipo de recurso omaSettingBoolean
description: Definición booleana de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 46bca1f6052dae3f4699b88258abce4b346c67bb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868211"
---
# <a name="omasettingboolean-resource-type"></a><span data-ttu-id="12e55-103">Tipo de recurso omaSettingBoolean</span><span class="sxs-lookup"><span data-stu-id="12e55-103">omaSettingBoolean resource type</span></span>

> <span data-ttu-id="12e55-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12e55-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12e55-105">Definición booleana de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="12e55-105">OMA Settings Boolean definition.</span></span>

<span data-ttu-id="12e55-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="12e55-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="12e55-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12e55-107">Properties</span></span>
|<span data-ttu-id="12e55-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="12e55-108">Property</span></span>|<span data-ttu-id="12e55-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="12e55-109">Type</span></span>|<span data-ttu-id="12e55-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="12e55-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="12e55-111">displayName</span><span class="sxs-lookup"><span data-stu-id="12e55-111">displayName</span></span>|<span data-ttu-id="12e55-112">cadena</span><span class="sxs-lookup"><span data-stu-id="12e55-112">String</span></span>|<span data-ttu-id="12e55-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="12e55-113">Display Name.</span></span> <span data-ttu-id="12e55-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="12e55-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="12e55-115">descripción</span><span class="sxs-lookup"><span data-stu-id="12e55-115">description</span></span>|<span data-ttu-id="12e55-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="12e55-116">String</span></span>|<span data-ttu-id="12e55-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="12e55-117">Description.</span></span> <span data-ttu-id="12e55-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="12e55-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="12e55-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="12e55-119">omaUri</span></span>|<span data-ttu-id="12e55-120">cadena</span><span class="sxs-lookup"><span data-stu-id="12e55-120">String</span></span>|<span data-ttu-id="12e55-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="12e55-121">OMA.</span></span> <span data-ttu-id="12e55-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="12e55-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="12e55-123">valor</span><span class="sxs-lookup"><span data-stu-id="12e55-123">value</span></span>|<span data-ttu-id="12e55-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="12e55-124">Boolean</span></span>|<span data-ttu-id="12e55-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="12e55-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="12e55-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="12e55-126">Relationships</span></span>
<span data-ttu-id="12e55-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="12e55-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="12e55-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="12e55-128">JSON Representation</span></span>
<span data-ttu-id="12e55-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="12e55-129">Here is a JSON representation of the resource.</span></span>
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



