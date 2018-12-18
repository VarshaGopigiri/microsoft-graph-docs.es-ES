---
title: Tipo de recurso omaSettingBase64
description: Definición de Base64 de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: ee25db94cc1426194166a7c66b9a8a626d62c3e4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304077"
---
# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="14f2a-103">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="14f2a-103">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="14f2a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="14f2a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="14f2a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="14f2a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="14f2a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="14f2a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="14f2a-107">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="14f2a-107">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="14f2a-108">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="14f2a-108">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="14f2a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14f2a-109">Properties</span></span>
|<span data-ttu-id="14f2a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14f2a-110">Property</span></span>|<span data-ttu-id="14f2a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="14f2a-111">Type</span></span>|<span data-ttu-id="14f2a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="14f2a-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="14f2a-113">displayName</span><span class="sxs-lookup"><span data-stu-id="14f2a-113">displayName</span></span>|<span data-ttu-id="14f2a-114">cadena</span><span class="sxs-lookup"><span data-stu-id="14f2a-114">String</span></span>|<span data-ttu-id="14f2a-115">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="14f2a-115">Display Name.</span></span> <span data-ttu-id="14f2a-116">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="14f2a-116">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="14f2a-117">descripción</span><span class="sxs-lookup"><span data-stu-id="14f2a-117">description</span></span>|<span data-ttu-id="14f2a-118">String</span><span class="sxs-lookup"><span data-stu-id="14f2a-118">String</span></span>|<span data-ttu-id="14f2a-119">Descripción.</span><span class="sxs-lookup"><span data-stu-id="14f2a-119">Description.</span></span> <span data-ttu-id="14f2a-120">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="14f2a-120">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="14f2a-121">omaUri</span><span class="sxs-lookup"><span data-stu-id="14f2a-121">omaUri</span></span>|<span data-ttu-id="14f2a-122">cadena</span><span class="sxs-lookup"><span data-stu-id="14f2a-122">String</span></span>|<span data-ttu-id="14f2a-123">OMA.</span><span class="sxs-lookup"><span data-stu-id="14f2a-123">OMA.</span></span> <span data-ttu-id="14f2a-124">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="14f2a-124">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="14f2a-125">fileName</span><span class="sxs-lookup"><span data-stu-id="14f2a-125">fileName</span></span>|<span data-ttu-id="14f2a-126">cadena</span><span class="sxs-lookup"><span data-stu-id="14f2a-126">String</span></span>|<span data-ttu-id="14f2a-127">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="14f2a-127">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="14f2a-128">\*.CRT</span><span class="sxs-lookup"><span data-stu-id="14f2a-128">\*.crt</span></span> | <span data-ttu-id="14f2a-129">\*.p7b</span><span class="sxs-lookup"><span data-stu-id="14f2a-129">\*.p7b</span></span> | <span data-ttu-id="14f2a-130">\* .bin).</span><span class="sxs-lookup"><span data-stu-id="14f2a-130">\*.bin).</span></span>|
|<span data-ttu-id="14f2a-131">valor</span><span class="sxs-lookup"><span data-stu-id="14f2a-131">value</span></span>|<span data-ttu-id="14f2a-132">cadena</span><span class="sxs-lookup"><span data-stu-id="14f2a-132">String</span></span>|<span data-ttu-id="14f2a-133">Valor.</span><span class="sxs-lookup"><span data-stu-id="14f2a-133">Value.</span></span> <span data-ttu-id="14f2a-134">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="14f2a-134">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="14f2a-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="14f2a-135">Relationships</span></span>
<span data-ttu-id="14f2a-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="14f2a-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="14f2a-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14f2a-137">JSON Representation</span></span>
<span data-ttu-id="14f2a-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="14f2a-138">Here is a JSON representation of the resource.</span></span>
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





