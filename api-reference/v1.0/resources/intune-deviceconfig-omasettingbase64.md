---
title: Tipo de recurso omaSettingBase64
description: Definición de Base64 de la configuración de OMA.
ms.openlocfilehash: 891c13a4cfcc8c0cf378cb5c7f9c6449bd876b7c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031210"
---
# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="42ef3-103">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="42ef3-103">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="42ef3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="42ef3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="42ef3-105">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="42ef3-105">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="42ef3-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="42ef3-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="42ef3-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42ef3-107">Properties</span></span>
|<span data-ttu-id="42ef3-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42ef3-108">Property</span></span>|<span data-ttu-id="42ef3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="42ef3-109">Type</span></span>|<span data-ttu-id="42ef3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="42ef3-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="42ef3-111">displayName</span><span class="sxs-lookup"><span data-stu-id="42ef3-111">displayName</span></span>|<span data-ttu-id="42ef3-112">cadena</span><span class="sxs-lookup"><span data-stu-id="42ef3-112">String</span></span>|<span data-ttu-id="42ef3-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="42ef3-113">Display Name.</span></span> <span data-ttu-id="42ef3-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="42ef3-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="42ef3-115">descripción</span><span class="sxs-lookup"><span data-stu-id="42ef3-115">description</span></span>|<span data-ttu-id="42ef3-116">String</span><span class="sxs-lookup"><span data-stu-id="42ef3-116">String</span></span>|<span data-ttu-id="42ef3-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="42ef3-117">Description.</span></span> <span data-ttu-id="42ef3-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="42ef3-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="42ef3-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="42ef3-119">omaUri</span></span>|<span data-ttu-id="42ef3-120">cadena</span><span class="sxs-lookup"><span data-stu-id="42ef3-120">String</span></span>|<span data-ttu-id="42ef3-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="42ef3-121">OMA.</span></span> <span data-ttu-id="42ef3-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="42ef3-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="42ef3-123">fileName</span><span class="sxs-lookup"><span data-stu-id="42ef3-123">fileName</span></span>|<span data-ttu-id="42ef3-124">cadena</span><span class="sxs-lookup"><span data-stu-id="42ef3-124">String</span></span>|<span data-ttu-id="42ef3-125">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="42ef3-125">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="42ef3-126">\*.CRT</span><span class="sxs-lookup"><span data-stu-id="42ef3-126">\*.crt</span></span> | <span data-ttu-id="42ef3-127">\*.p7b</span><span class="sxs-lookup"><span data-stu-id="42ef3-127">\*.p7b</span></span> | <span data-ttu-id="42ef3-128">\* .bin).</span><span class="sxs-lookup"><span data-stu-id="42ef3-128">\*.bin).</span></span>|
|<span data-ttu-id="42ef3-129">valor</span><span class="sxs-lookup"><span data-stu-id="42ef3-129">value</span></span>|<span data-ttu-id="42ef3-130">cadena</span><span class="sxs-lookup"><span data-stu-id="42ef3-130">String</span></span>|<span data-ttu-id="42ef3-131">Valor.</span><span class="sxs-lookup"><span data-stu-id="42ef3-131">Value.</span></span> <span data-ttu-id="42ef3-132">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="42ef3-132">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="42ef3-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="42ef3-133">Relationships</span></span>
<span data-ttu-id="42ef3-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="42ef3-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="42ef3-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="42ef3-135">JSON Representation</span></span>
<span data-ttu-id="42ef3-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="42ef3-136">Here is a JSON representation of the resource.</span></span>
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



