---
title: Tipo de recurso omaSettingFloatingPoint
description: Definición de punto flotante de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ddb11f40faf9db58fefb984fcc08a9fedd66e97d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951554"
---
# <a name="omasettingfloatingpoint-resource-type"></a><span data-ttu-id="049ae-103">Tipo de recurso omaSettingFloatingPoint</span><span class="sxs-lookup"><span data-stu-id="049ae-103">omaSettingFloatingPoint resource type</span></span>

> <span data-ttu-id="049ae-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="049ae-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="049ae-105">Definición de punto flotante de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="049ae-105">OMA Settings Floating Point definition.</span></span>

<span data-ttu-id="049ae-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="049ae-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="049ae-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="049ae-107">Properties</span></span>
|<span data-ttu-id="049ae-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="049ae-108">Property</span></span>|<span data-ttu-id="049ae-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="049ae-109">Type</span></span>|<span data-ttu-id="049ae-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="049ae-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="049ae-111">displayName</span><span class="sxs-lookup"><span data-stu-id="049ae-111">displayName</span></span>|<span data-ttu-id="049ae-112">cadena</span><span class="sxs-lookup"><span data-stu-id="049ae-112">String</span></span>|<span data-ttu-id="049ae-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="049ae-113">Display Name.</span></span> <span data-ttu-id="049ae-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="049ae-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="049ae-115">descripción</span><span class="sxs-lookup"><span data-stu-id="049ae-115">description</span></span>|<span data-ttu-id="049ae-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="049ae-116">String</span></span>|<span data-ttu-id="049ae-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="049ae-117">Description.</span></span> <span data-ttu-id="049ae-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="049ae-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="049ae-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="049ae-119">omaUri</span></span>|<span data-ttu-id="049ae-120">cadena</span><span class="sxs-lookup"><span data-stu-id="049ae-120">String</span></span>|<span data-ttu-id="049ae-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="049ae-121">OMA.</span></span> <span data-ttu-id="049ae-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="049ae-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="049ae-123">value</span><span class="sxs-lookup"><span data-stu-id="049ae-123">value</span></span>|<span data-ttu-id="049ae-124">Simple</span><span class="sxs-lookup"><span data-stu-id="049ae-124">Single</span></span>|<span data-ttu-id="049ae-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="049ae-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="049ae-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="049ae-126">Relationships</span></span>
<span data-ttu-id="049ae-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="049ae-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="049ae-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="049ae-128">JSON Representation</span></span>
<span data-ttu-id="049ae-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="049ae-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingFloatingPoint"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingFloatingPoint",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "<Unknown Primitive Type Edm.Single>"
}
```



