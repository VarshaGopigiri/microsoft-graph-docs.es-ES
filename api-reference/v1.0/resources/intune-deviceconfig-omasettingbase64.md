---
title: Tipo de recurso omaSettingBase64
description: Definición de Base64 de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6205cd0ad894cc6e39f6d587a262bce173b7ef57
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860224"
---
# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="8de82-103">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="8de82-103">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="8de82-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8de82-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8de82-105">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="8de82-105">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="8de82-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="8de82-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8de82-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8de82-107">Properties</span></span>
|<span data-ttu-id="8de82-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8de82-108">Property</span></span>|<span data-ttu-id="8de82-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8de82-109">Type</span></span>|<span data-ttu-id="8de82-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8de82-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8de82-111">displayName</span><span class="sxs-lookup"><span data-stu-id="8de82-111">displayName</span></span>|<span data-ttu-id="8de82-112">cadena</span><span class="sxs-lookup"><span data-stu-id="8de82-112">String</span></span>|<span data-ttu-id="8de82-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="8de82-113">Display Name.</span></span> <span data-ttu-id="8de82-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="8de82-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="8de82-115">descripción</span><span class="sxs-lookup"><span data-stu-id="8de82-115">description</span></span>|<span data-ttu-id="8de82-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="8de82-116">String</span></span>|<span data-ttu-id="8de82-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="8de82-117">Description.</span></span> <span data-ttu-id="8de82-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="8de82-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="8de82-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="8de82-119">omaUri</span></span>|<span data-ttu-id="8de82-120">cadena</span><span class="sxs-lookup"><span data-stu-id="8de82-120">String</span></span>|<span data-ttu-id="8de82-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="8de82-121">OMA.</span></span> <span data-ttu-id="8de82-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="8de82-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="8de82-123">fileName</span><span class="sxs-lookup"><span data-stu-id="8de82-123">fileName</span></span>|<span data-ttu-id="8de82-124">cadena</span><span class="sxs-lookup"><span data-stu-id="8de82-124">String</span></span>|<span data-ttu-id="8de82-125">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="8de82-125">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="8de82-126">\*.CRT</span><span class="sxs-lookup"><span data-stu-id="8de82-126">\*.crt</span></span> | <span data-ttu-id="8de82-127">\*.p7b</span><span class="sxs-lookup"><span data-stu-id="8de82-127">\*.p7b</span></span> | <span data-ttu-id="8de82-128">\* .bin).</span><span class="sxs-lookup"><span data-stu-id="8de82-128">\*.bin).</span></span>|
|<span data-ttu-id="8de82-129">valor</span><span class="sxs-lookup"><span data-stu-id="8de82-129">value</span></span>|<span data-ttu-id="8de82-130">cadena</span><span class="sxs-lookup"><span data-stu-id="8de82-130">String</span></span>|<span data-ttu-id="8de82-131">Valor.</span><span class="sxs-lookup"><span data-stu-id="8de82-131">Value.</span></span> <span data-ttu-id="8de82-132">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="8de82-132">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="8de82-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8de82-133">Relationships</span></span>
<span data-ttu-id="8de82-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8de82-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8de82-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8de82-135">JSON Representation</span></span>
<span data-ttu-id="8de82-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8de82-136">Here is a JSON representation of the resource.</span></span>
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



