---
title: Tipo de recurso omaSettingStringXml
description: Definición de la cadena XML de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0fa631992288695b069a6317128fa369ed42b4d6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967436"
---
# <a name="omasettingstringxml-resource-type"></a><span data-ttu-id="6a7e1-103">Tipo de recurso omaSettingStringXml</span><span class="sxs-lookup"><span data-stu-id="6a7e1-103">omaSettingStringXml resource type</span></span>

> <span data-ttu-id="6a7e1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6a7e1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6a7e1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6a7e1-107">Definición de la cadena XML de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-107">OMA Settings StringXML definition.</span></span>

<span data-ttu-id="6a7e1-108">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="6a7e1-108">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="6a7e1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a7e1-109">Properties</span></span>
|<span data-ttu-id="6a7e1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a7e1-110">Property</span></span>|<span data-ttu-id="6a7e1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a7e1-111">Type</span></span>|<span data-ttu-id="6a7e1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a7e1-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6a7e1-113">displayName</span><span class="sxs-lookup"><span data-stu-id="6a7e1-113">displayName</span></span>|<span data-ttu-id="6a7e1-114">cadena</span><span class="sxs-lookup"><span data-stu-id="6a7e1-114">String</span></span>|<span data-ttu-id="6a7e1-115">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-115">Display Name.</span></span> <span data-ttu-id="6a7e1-116">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="6a7e1-116">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="6a7e1-117">descripción</span><span class="sxs-lookup"><span data-stu-id="6a7e1-117">description</span></span>|<span data-ttu-id="6a7e1-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a7e1-118">String</span></span>|<span data-ttu-id="6a7e1-119">Descripción.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-119">Description.</span></span> <span data-ttu-id="6a7e1-120">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="6a7e1-120">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="6a7e1-121">omaUri</span><span class="sxs-lookup"><span data-stu-id="6a7e1-121">omaUri</span></span>|<span data-ttu-id="6a7e1-122">cadena</span><span class="sxs-lookup"><span data-stu-id="6a7e1-122">String</span></span>|<span data-ttu-id="6a7e1-123">OMA.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-123">OMA.</span></span> <span data-ttu-id="6a7e1-124">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="6a7e1-124">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="6a7e1-125">fileName</span><span class="sxs-lookup"><span data-stu-id="6a7e1-125">fileName</span></span>|<span data-ttu-id="6a7e1-126">cadena</span><span class="sxs-lookup"><span data-stu-id="6a7e1-126">String</span></span>|<span data-ttu-id="6a7e1-127">Nombre de archivo asociado a la propiedad de valor (\*.xml).</span><span class="sxs-lookup"><span data-stu-id="6a7e1-127">File name associated with the Value property (\*.xml).</span></span>|
|<span data-ttu-id="6a7e1-128">valor</span><span class="sxs-lookup"><span data-stu-id="6a7e1-128">value</span></span>|<span data-ttu-id="6a7e1-129">Binario</span><span class="sxs-lookup"><span data-stu-id="6a7e1-129">Binary</span></span>|<span data-ttu-id="6a7e1-130">Valor.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-130">Value.</span></span> <span data-ttu-id="6a7e1-131">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="6a7e1-131">(UTF8 encoded byte array)</span></span>|

## <a name="relationships"></a><span data-ttu-id="6a7e1-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6a7e1-132">Relationships</span></span>
<span data-ttu-id="6a7e1-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6a7e1-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6a7e1-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6a7e1-134">JSON Representation</span></span>
<span data-ttu-id="6a7e1-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingStringXml"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingStringXml",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "fileName": "String",
  "value": "binary"
}
```





