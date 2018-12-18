---
title: Tipo de recurso omaSettingStringXml
description: Definición de la cadena XML de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: c7f7d07a94550d86e6507e9202195d09e9555f60
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332014"
---
# <a name="omasettingstringxml-resource-type"></a><span data-ttu-id="fdfc8-103">Tipo de recurso omaSettingStringXml</span><span class="sxs-lookup"><span data-stu-id="fdfc8-103">omaSettingStringXml resource type</span></span>

> <span data-ttu-id="fdfc8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fdfc8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fdfc8-105">Definición de la cadena XML de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="fdfc8-105">OMA Settings StringXML definition.</span></span>

<span data-ttu-id="fdfc8-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fdfc8-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="fdfc8-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fdfc8-107">Properties</span></span>
|<span data-ttu-id="fdfc8-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fdfc8-108">Property</span></span>|<span data-ttu-id="fdfc8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdfc8-109">Type</span></span>|<span data-ttu-id="fdfc8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdfc8-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fdfc8-111">displayName</span><span class="sxs-lookup"><span data-stu-id="fdfc8-111">displayName</span></span>|<span data-ttu-id="fdfc8-112">cadena</span><span class="sxs-lookup"><span data-stu-id="fdfc8-112">String</span></span>|<span data-ttu-id="fdfc8-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="fdfc8-113">Display Name.</span></span> <span data-ttu-id="fdfc8-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fdfc8-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="fdfc8-115">descripción</span><span class="sxs-lookup"><span data-stu-id="fdfc8-115">description</span></span>|<span data-ttu-id="fdfc8-116">String</span><span class="sxs-lookup"><span data-stu-id="fdfc8-116">String</span></span>|<span data-ttu-id="fdfc8-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="fdfc8-117">Description.</span></span> <span data-ttu-id="fdfc8-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fdfc8-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="fdfc8-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="fdfc8-119">omaUri</span></span>|<span data-ttu-id="fdfc8-120">cadena</span><span class="sxs-lookup"><span data-stu-id="fdfc8-120">String</span></span>|<span data-ttu-id="fdfc8-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="fdfc8-121">OMA.</span></span> <span data-ttu-id="fdfc8-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fdfc8-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="fdfc8-123">fileName</span><span class="sxs-lookup"><span data-stu-id="fdfc8-123">fileName</span></span>|<span data-ttu-id="fdfc8-124">cadena</span><span class="sxs-lookup"><span data-stu-id="fdfc8-124">String</span></span>|<span data-ttu-id="fdfc8-125">Nombre de archivo asociado a la propiedad de valor (\*.xml).</span><span class="sxs-lookup"><span data-stu-id="fdfc8-125">File name associated with the Value property (\*.xml).</span></span>|
|<span data-ttu-id="fdfc8-126">valor</span><span class="sxs-lookup"><span data-stu-id="fdfc8-126">value</span></span>|<span data-ttu-id="fdfc8-127">Binario</span><span class="sxs-lookup"><span data-stu-id="fdfc8-127">Binary</span></span>|<span data-ttu-id="fdfc8-128">Valor.</span><span class="sxs-lookup"><span data-stu-id="fdfc8-128">Value.</span></span> <span data-ttu-id="fdfc8-129">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="fdfc8-129">(UTF8 encoded byte array)</span></span>|

## <a name="relationships"></a><span data-ttu-id="fdfc8-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fdfc8-130">Relationships</span></span>
<span data-ttu-id="fdfc8-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fdfc8-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fdfc8-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fdfc8-132">JSON Representation</span></span>
<span data-ttu-id="fdfc8-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fdfc8-133">Here is a JSON representation of the resource.</span></span>
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



