---
title: Tipo de recurso omaSettingStringXml
description: Definición de la cadena XML de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 976c95ed9ffa6674ddc185bb1723c7d7f9d054f6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894022"
---
# <a name="omasettingstringxml-resource-type"></a><span data-ttu-id="88c21-103">Tipo de recurso omaSettingStringXml</span><span class="sxs-lookup"><span data-stu-id="88c21-103">omaSettingStringXml resource type</span></span>

> <span data-ttu-id="88c21-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88c21-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88c21-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88c21-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="88c21-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="88c21-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="88c21-107">Definición de la cadena XML de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="88c21-107">OMA Settings StringXML definition.</span></span>

<span data-ttu-id="88c21-108">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="88c21-108">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="88c21-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88c21-109">Properties</span></span>
|<span data-ttu-id="88c21-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88c21-110">Property</span></span>|<span data-ttu-id="88c21-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="88c21-111">Type</span></span>|<span data-ttu-id="88c21-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="88c21-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="88c21-113">displayName</span><span class="sxs-lookup"><span data-stu-id="88c21-113">displayName</span></span>|<span data-ttu-id="88c21-114">cadena</span><span class="sxs-lookup"><span data-stu-id="88c21-114">String</span></span>|<span data-ttu-id="88c21-115">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="88c21-115">Display Name.</span></span> <span data-ttu-id="88c21-116">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="88c21-116">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="88c21-117">descripción</span><span class="sxs-lookup"><span data-stu-id="88c21-117">description</span></span>|<span data-ttu-id="88c21-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="88c21-118">String</span></span>|<span data-ttu-id="88c21-119">Descripción.</span><span class="sxs-lookup"><span data-stu-id="88c21-119">Description.</span></span> <span data-ttu-id="88c21-120">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="88c21-120">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="88c21-121">omaUri</span><span class="sxs-lookup"><span data-stu-id="88c21-121">omaUri</span></span>|<span data-ttu-id="88c21-122">cadena</span><span class="sxs-lookup"><span data-stu-id="88c21-122">String</span></span>|<span data-ttu-id="88c21-123">OMA.</span><span class="sxs-lookup"><span data-stu-id="88c21-123">OMA.</span></span> <span data-ttu-id="88c21-124">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="88c21-124">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="88c21-125">fileName</span><span class="sxs-lookup"><span data-stu-id="88c21-125">fileName</span></span>|<span data-ttu-id="88c21-126">cadena</span><span class="sxs-lookup"><span data-stu-id="88c21-126">String</span></span>|<span data-ttu-id="88c21-127">Nombre de archivo asociado a la propiedad de valor (\*.xml).</span><span class="sxs-lookup"><span data-stu-id="88c21-127">File name associated with the Value property (\*.xml).</span></span>|
|<span data-ttu-id="88c21-128">valor</span><span class="sxs-lookup"><span data-stu-id="88c21-128">value</span></span>|<span data-ttu-id="88c21-129">Binario</span><span class="sxs-lookup"><span data-stu-id="88c21-129">Binary</span></span>|<span data-ttu-id="88c21-130">Valor.</span><span class="sxs-lookup"><span data-stu-id="88c21-130">Value.</span></span> <span data-ttu-id="88c21-131">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="88c21-131">(UTF8 encoded byte array)</span></span>|

## <a name="relationships"></a><span data-ttu-id="88c21-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="88c21-132">Relationships</span></span>
<span data-ttu-id="88c21-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="88c21-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="88c21-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="88c21-134">JSON Representation</span></span>
<span data-ttu-id="88c21-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="88c21-135">Here is a JSON representation of the resource.</span></span>
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





