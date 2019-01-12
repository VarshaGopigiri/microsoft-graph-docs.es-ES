---
title: Tipo de recurso omaSettingString
description: Definición de la cadena de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ce33092b2ed011b6f3d7460ab988fbb195a1bd5a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946617"
---
# <a name="omasettingstring-resource-type"></a><span data-ttu-id="17798-103">Tipo de recurso omaSettingString</span><span class="sxs-lookup"><span data-stu-id="17798-103">omaSettingString resource type</span></span>

> <span data-ttu-id="17798-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17798-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17798-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17798-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="17798-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17798-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17798-107">Definición de la cadena de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="17798-107">OMA Settings String definition.</span></span>

<span data-ttu-id="17798-108">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="17798-108">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="17798-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17798-109">Properties</span></span>
|<span data-ttu-id="17798-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17798-110">Property</span></span>|<span data-ttu-id="17798-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="17798-111">Type</span></span>|<span data-ttu-id="17798-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="17798-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="17798-113">displayName</span><span class="sxs-lookup"><span data-stu-id="17798-113">displayName</span></span>|<span data-ttu-id="17798-114">cadena</span><span class="sxs-lookup"><span data-stu-id="17798-114">String</span></span>|<span data-ttu-id="17798-115">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="17798-115">Display Name.</span></span> <span data-ttu-id="17798-116">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="17798-116">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="17798-117">descripción</span><span class="sxs-lookup"><span data-stu-id="17798-117">description</span></span>|<span data-ttu-id="17798-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="17798-118">String</span></span>|<span data-ttu-id="17798-119">Descripción.</span><span class="sxs-lookup"><span data-stu-id="17798-119">Description.</span></span> <span data-ttu-id="17798-120">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="17798-120">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="17798-121">omaUri</span><span class="sxs-lookup"><span data-stu-id="17798-121">omaUri</span></span>|<span data-ttu-id="17798-122">cadena</span><span class="sxs-lookup"><span data-stu-id="17798-122">String</span></span>|<span data-ttu-id="17798-123">OMA.</span><span class="sxs-lookup"><span data-stu-id="17798-123">OMA.</span></span> <span data-ttu-id="17798-124">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="17798-124">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="17798-125">valor</span><span class="sxs-lookup"><span data-stu-id="17798-125">value</span></span>|<span data-ttu-id="17798-126">cadena</span><span class="sxs-lookup"><span data-stu-id="17798-126">String</span></span>|<span data-ttu-id="17798-127">Valor.</span><span class="sxs-lookup"><span data-stu-id="17798-127">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="17798-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="17798-128">Relationships</span></span>
<span data-ttu-id="17798-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="17798-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="17798-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17798-130">JSON Representation</span></span>
<span data-ttu-id="17798-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="17798-131">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingString"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingString",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String"
}
```





