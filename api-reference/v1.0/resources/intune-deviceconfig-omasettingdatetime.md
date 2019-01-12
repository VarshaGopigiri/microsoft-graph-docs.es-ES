---
title: Tipo de recurso omaSettingDateTime
description: Definición de DateTime de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 34c19caee6bab30dbfe0e82abf1a55f20bb5d3b4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932297"
---
# <a name="omasettingdatetime-resource-type"></a><span data-ttu-id="f2d25-103">Tipo de recurso omaSettingDateTime</span><span class="sxs-lookup"><span data-stu-id="f2d25-103">omaSettingDateTime resource type</span></span>

> <span data-ttu-id="f2d25-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f2d25-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f2d25-105">Definición de DateTime de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="f2d25-105">OMA Settings DateTime definition.</span></span>

<span data-ttu-id="f2d25-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="f2d25-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="f2d25-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2d25-107">Properties</span></span>
|<span data-ttu-id="f2d25-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f2d25-108">Property</span></span>|<span data-ttu-id="f2d25-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2d25-109">Type</span></span>|<span data-ttu-id="f2d25-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2d25-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f2d25-111">displayName</span><span class="sxs-lookup"><span data-stu-id="f2d25-111">displayName</span></span>|<span data-ttu-id="f2d25-112">cadena</span><span class="sxs-lookup"><span data-stu-id="f2d25-112">String</span></span>|<span data-ttu-id="f2d25-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="f2d25-113">Display Name.</span></span> <span data-ttu-id="f2d25-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="f2d25-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="f2d25-115">descripción</span><span class="sxs-lookup"><span data-stu-id="f2d25-115">description</span></span>|<span data-ttu-id="f2d25-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="f2d25-116">String</span></span>|<span data-ttu-id="f2d25-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="f2d25-117">Description.</span></span> <span data-ttu-id="f2d25-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="f2d25-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="f2d25-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="f2d25-119">omaUri</span></span>|<span data-ttu-id="f2d25-120">cadena</span><span class="sxs-lookup"><span data-stu-id="f2d25-120">String</span></span>|<span data-ttu-id="f2d25-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="f2d25-121">OMA.</span></span> <span data-ttu-id="f2d25-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="f2d25-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="f2d25-123">value</span><span class="sxs-lookup"><span data-stu-id="f2d25-123">value</span></span>|<span data-ttu-id="f2d25-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f2d25-124">DateTimeOffset</span></span>|<span data-ttu-id="f2d25-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="f2d25-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f2d25-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f2d25-126">Relationships</span></span>
<span data-ttu-id="f2d25-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f2d25-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f2d25-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f2d25-128">JSON Representation</span></span>
<span data-ttu-id="f2d25-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f2d25-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingDateTime"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingDateTime",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String (timestamp)"
}
```



