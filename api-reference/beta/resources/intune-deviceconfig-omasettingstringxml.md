---
title: Tipo de recurso omaSettingStringXml
description: Definición de la cadena XML de la configuración de OMA.
ms.openlocfilehash: bb95041a10a71591c06a55dca39a4377d32376b7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084296"
---
# <a name="omasettingstringxml-resource-type"></a><span data-ttu-id="29967-103">Tipo de recurso omaSettingStringXml</span><span class="sxs-lookup"><span data-stu-id="29967-103">omaSettingStringXml resource type</span></span>

> <span data-ttu-id="29967-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="29967-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="29967-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="29967-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="29967-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="29967-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="29967-107">Definición de la cadena XML de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="29967-107">OMA Settings StringXML definition.</span></span>

<span data-ttu-id="29967-108">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="29967-108">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="29967-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29967-109">Properties</span></span>
|<span data-ttu-id="29967-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="29967-110">Property</span></span>|<span data-ttu-id="29967-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="29967-111">Type</span></span>|<span data-ttu-id="29967-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="29967-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="29967-113">displayName</span><span class="sxs-lookup"><span data-stu-id="29967-113">displayName</span></span>|<span data-ttu-id="29967-114">cadena</span><span class="sxs-lookup"><span data-stu-id="29967-114">String</span></span>|<span data-ttu-id="29967-115">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="29967-115">Display Name.</span></span> <span data-ttu-id="29967-116">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="29967-116">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="29967-117">descripción</span><span class="sxs-lookup"><span data-stu-id="29967-117">description</span></span>|<span data-ttu-id="29967-118">String</span><span class="sxs-lookup"><span data-stu-id="29967-118">String</span></span>|<span data-ttu-id="29967-119">Descripción.</span><span class="sxs-lookup"><span data-stu-id="29967-119">Description.</span></span> <span data-ttu-id="29967-120">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="29967-120">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="29967-121">omaUri</span><span class="sxs-lookup"><span data-stu-id="29967-121">omaUri</span></span>|<span data-ttu-id="29967-122">cadena</span><span class="sxs-lookup"><span data-stu-id="29967-122">String</span></span>|<span data-ttu-id="29967-123">OMA.</span><span class="sxs-lookup"><span data-stu-id="29967-123">OMA.</span></span> <span data-ttu-id="29967-124">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="29967-124">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="29967-125">fileName</span><span class="sxs-lookup"><span data-stu-id="29967-125">fileName</span></span>|<span data-ttu-id="29967-126">cadena</span><span class="sxs-lookup"><span data-stu-id="29967-126">String</span></span>|<span data-ttu-id="29967-127">Nombre de archivo asociado a la propiedad de valor (\*.xml).</span><span class="sxs-lookup"><span data-stu-id="29967-127">File name associated with the Value property (\*.xml).</span></span>|
|<span data-ttu-id="29967-128">valor</span><span class="sxs-lookup"><span data-stu-id="29967-128">value</span></span>|<span data-ttu-id="29967-129">Binario</span><span class="sxs-lookup"><span data-stu-id="29967-129">Binary</span></span>|<span data-ttu-id="29967-130">Valor.</span><span class="sxs-lookup"><span data-stu-id="29967-130">Value.</span></span> <span data-ttu-id="29967-131">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="29967-131">(UTF8 encoded byte array)</span></span>|

## <a name="relationships"></a><span data-ttu-id="29967-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="29967-132">Relationships</span></span>
<span data-ttu-id="29967-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="29967-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="29967-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="29967-134">JSON Representation</span></span>
<span data-ttu-id="29967-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="29967-135">Here is a JSON representation of the resource.</span></span>
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





