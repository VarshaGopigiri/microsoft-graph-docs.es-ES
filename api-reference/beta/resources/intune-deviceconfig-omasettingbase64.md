---
title: Tipo de recurso omaSettingBase64
description: Definición de Base64 de la configuración de OMA.
ms.openlocfilehash: eebe9730c36ab4bc7e48aa765ecd3959897c6c12
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086607"
---
# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="d015b-103">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="d015b-103">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="d015b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d015b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d015b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d015b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d015b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d015b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d015b-107">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="d015b-107">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="d015b-108">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="d015b-108">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="d015b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d015b-109">Properties</span></span>
|<span data-ttu-id="d015b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d015b-110">Property</span></span>|<span data-ttu-id="d015b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d015b-111">Type</span></span>|<span data-ttu-id="d015b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d015b-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d015b-113">displayName</span><span class="sxs-lookup"><span data-stu-id="d015b-113">displayName</span></span>|<span data-ttu-id="d015b-114">cadena</span><span class="sxs-lookup"><span data-stu-id="d015b-114">String</span></span>|<span data-ttu-id="d015b-115">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="d015b-115">Display Name.</span></span> <span data-ttu-id="d015b-116">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="d015b-116">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="d015b-117">descripción</span><span class="sxs-lookup"><span data-stu-id="d015b-117">description</span></span>|<span data-ttu-id="d015b-118">String</span><span class="sxs-lookup"><span data-stu-id="d015b-118">String</span></span>|<span data-ttu-id="d015b-119">Descripción.</span><span class="sxs-lookup"><span data-stu-id="d015b-119">Description.</span></span> <span data-ttu-id="d015b-120">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="d015b-120">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="d015b-121">omaUri</span><span class="sxs-lookup"><span data-stu-id="d015b-121">omaUri</span></span>|<span data-ttu-id="d015b-122">cadena</span><span class="sxs-lookup"><span data-stu-id="d015b-122">String</span></span>|<span data-ttu-id="d015b-123">OMA.</span><span class="sxs-lookup"><span data-stu-id="d015b-123">OMA.</span></span> <span data-ttu-id="d015b-124">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="d015b-124">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="d015b-125">fileName</span><span class="sxs-lookup"><span data-stu-id="d015b-125">fileName</span></span>|<span data-ttu-id="d015b-126">cadena</span><span class="sxs-lookup"><span data-stu-id="d015b-126">String</span></span>|<span data-ttu-id="d015b-127">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="d015b-127">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="d015b-128">\*.CRT</span><span class="sxs-lookup"><span data-stu-id="d015b-128">\*.crt</span></span> | <span data-ttu-id="d015b-129">\*.p7b</span><span class="sxs-lookup"><span data-stu-id="d015b-129">\*.p7b</span></span> | <span data-ttu-id="d015b-130">\* .bin).</span><span class="sxs-lookup"><span data-stu-id="d015b-130">\*.bin).</span></span>|
|<span data-ttu-id="d015b-131">valor</span><span class="sxs-lookup"><span data-stu-id="d015b-131">value</span></span>|<span data-ttu-id="d015b-132">cadena</span><span class="sxs-lookup"><span data-stu-id="d015b-132">String</span></span>|<span data-ttu-id="d015b-133">Valor.</span><span class="sxs-lookup"><span data-stu-id="d015b-133">Value.</span></span> <span data-ttu-id="d015b-134">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="d015b-134">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="d015b-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d015b-135">Relationships</span></span>
<span data-ttu-id="d015b-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d015b-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d015b-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d015b-137">JSON Representation</span></span>
<span data-ttu-id="d015b-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d015b-138">Here is a JSON representation of the resource.</span></span>
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





