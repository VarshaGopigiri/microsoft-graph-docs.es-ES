---
title: Tipo de recurso omaSettingBase64
description: Definición de Base64 de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: 6b0835864d3ec8f8364a15ff293a75dfeded3a0b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343725"
---
# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="50629-103">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="50629-103">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="50629-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50629-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50629-105">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="50629-105">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="50629-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="50629-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="50629-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50629-107">Properties</span></span>
|<span data-ttu-id="50629-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50629-108">Property</span></span>|<span data-ttu-id="50629-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="50629-109">Type</span></span>|<span data-ttu-id="50629-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="50629-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50629-111">displayName</span><span class="sxs-lookup"><span data-stu-id="50629-111">displayName</span></span>|<span data-ttu-id="50629-112">cadena</span><span class="sxs-lookup"><span data-stu-id="50629-112">String</span></span>|<span data-ttu-id="50629-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="50629-113">Display Name.</span></span> <span data-ttu-id="50629-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="50629-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="50629-115">descripción</span><span class="sxs-lookup"><span data-stu-id="50629-115">description</span></span>|<span data-ttu-id="50629-116">String</span><span class="sxs-lookup"><span data-stu-id="50629-116">String</span></span>|<span data-ttu-id="50629-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="50629-117">Description.</span></span> <span data-ttu-id="50629-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="50629-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="50629-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="50629-119">omaUri</span></span>|<span data-ttu-id="50629-120">cadena</span><span class="sxs-lookup"><span data-stu-id="50629-120">String</span></span>|<span data-ttu-id="50629-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="50629-121">OMA.</span></span> <span data-ttu-id="50629-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="50629-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="50629-123">fileName</span><span class="sxs-lookup"><span data-stu-id="50629-123">fileName</span></span>|<span data-ttu-id="50629-124">cadena</span><span class="sxs-lookup"><span data-stu-id="50629-124">String</span></span>|<span data-ttu-id="50629-125">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="50629-125">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="50629-126">\*.CRT</span><span class="sxs-lookup"><span data-stu-id="50629-126">\*.crt</span></span> | <span data-ttu-id="50629-127">\*.p7b</span><span class="sxs-lookup"><span data-stu-id="50629-127">\*.p7b</span></span> | <span data-ttu-id="50629-128">\* .bin).</span><span class="sxs-lookup"><span data-stu-id="50629-128">\*.bin).</span></span>|
|<span data-ttu-id="50629-129">valor</span><span class="sxs-lookup"><span data-stu-id="50629-129">value</span></span>|<span data-ttu-id="50629-130">cadena</span><span class="sxs-lookup"><span data-stu-id="50629-130">String</span></span>|<span data-ttu-id="50629-131">Valor.</span><span class="sxs-lookup"><span data-stu-id="50629-131">Value.</span></span> <span data-ttu-id="50629-132">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="50629-132">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="50629-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="50629-133">Relationships</span></span>
<span data-ttu-id="50629-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="50629-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="50629-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50629-135">JSON Representation</span></span>
<span data-ttu-id="50629-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="50629-136">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingBase64"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingBase64",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "fileName": "String",
  "value": "String"
}
```



