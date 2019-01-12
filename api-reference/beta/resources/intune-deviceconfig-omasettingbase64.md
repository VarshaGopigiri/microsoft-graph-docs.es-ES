---
title: Tipo de recurso omaSettingBase64
description: Definición de Base64 de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8f1c6a488adf2f39b2c415e31c4919380ebda5ab
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982571"
---
# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="533a1-103">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="533a1-103">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="533a1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="533a1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="533a1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="533a1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="533a1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="533a1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="533a1-107">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="533a1-107">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="533a1-108">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="533a1-108">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="533a1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="533a1-109">Properties</span></span>
|<span data-ttu-id="533a1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="533a1-110">Property</span></span>|<span data-ttu-id="533a1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="533a1-111">Type</span></span>|<span data-ttu-id="533a1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="533a1-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="533a1-113">displayName</span><span class="sxs-lookup"><span data-stu-id="533a1-113">displayName</span></span>|<span data-ttu-id="533a1-114">cadena</span><span class="sxs-lookup"><span data-stu-id="533a1-114">String</span></span>|<span data-ttu-id="533a1-115">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="533a1-115">Display Name.</span></span> <span data-ttu-id="533a1-116">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="533a1-116">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="533a1-117">descripción</span><span class="sxs-lookup"><span data-stu-id="533a1-117">description</span></span>|<span data-ttu-id="533a1-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="533a1-118">String</span></span>|<span data-ttu-id="533a1-119">Descripción.</span><span class="sxs-lookup"><span data-stu-id="533a1-119">Description.</span></span> <span data-ttu-id="533a1-120">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="533a1-120">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="533a1-121">omaUri</span><span class="sxs-lookup"><span data-stu-id="533a1-121">omaUri</span></span>|<span data-ttu-id="533a1-122">cadena</span><span class="sxs-lookup"><span data-stu-id="533a1-122">String</span></span>|<span data-ttu-id="533a1-123">OMA.</span><span class="sxs-lookup"><span data-stu-id="533a1-123">OMA.</span></span> <span data-ttu-id="533a1-124">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="533a1-124">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="533a1-125">fileName</span><span class="sxs-lookup"><span data-stu-id="533a1-125">fileName</span></span>|<span data-ttu-id="533a1-126">cadena</span><span class="sxs-lookup"><span data-stu-id="533a1-126">String</span></span>|<span data-ttu-id="533a1-127">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="533a1-127">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="533a1-128">\*.CRT</span><span class="sxs-lookup"><span data-stu-id="533a1-128">\*.crt</span></span> | <span data-ttu-id="533a1-129">\*.p7b</span><span class="sxs-lookup"><span data-stu-id="533a1-129">\*.p7b</span></span> | <span data-ttu-id="533a1-130">\* .bin).</span><span class="sxs-lookup"><span data-stu-id="533a1-130">\*.bin).</span></span>|
|<span data-ttu-id="533a1-131">valor</span><span class="sxs-lookup"><span data-stu-id="533a1-131">value</span></span>|<span data-ttu-id="533a1-132">cadena</span><span class="sxs-lookup"><span data-stu-id="533a1-132">String</span></span>|<span data-ttu-id="533a1-133">Valor.</span><span class="sxs-lookup"><span data-stu-id="533a1-133">Value.</span></span> <span data-ttu-id="533a1-134">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="533a1-134">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="533a1-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="533a1-135">Relationships</span></span>
<span data-ttu-id="533a1-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="533a1-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="533a1-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="533a1-137">JSON Representation</span></span>
<span data-ttu-id="533a1-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="533a1-138">Here is a JSON representation of the resource.</span></span>
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





