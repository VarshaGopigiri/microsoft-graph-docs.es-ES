---
title: tipo de recurso airPrintDestination
description: Representa un destino de AirPrint.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6d1548737956d35d42fc077afe92de1885a54581
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878592"
---
# <a name="airprintdestination-resource-type"></a><span data-ttu-id="5133a-103">tipo de recurso airPrintDestination</span><span class="sxs-lookup"><span data-stu-id="5133a-103">airPrintDestination resource type</span></span>

> <span data-ttu-id="5133a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5133a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5133a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5133a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5133a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5133a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5133a-107">Representa un destino de AirPrint.</span><span class="sxs-lookup"><span data-stu-id="5133a-107">Represents an AirPrint destination.</span></span>
## <a name="properties"></a><span data-ttu-id="5133a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5133a-108">Properties</span></span>
|<span data-ttu-id="5133a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5133a-109">Property</span></span>|<span data-ttu-id="5133a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5133a-110">Type</span></span>|<span data-ttu-id="5133a-111">Description</span><span class="sxs-lookup"><span data-stu-id="5133a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5133a-112">ipAddress</span><span class="sxs-lookup"><span data-stu-id="5133a-112">ipAddress</span></span>|<span data-ttu-id="5133a-113">cadena</span><span class="sxs-lookup"><span data-stu-id="5133a-113">String</span></span>|<span data-ttu-id="5133a-114">La dirección IP de destino AirPrint.</span><span class="sxs-lookup"><span data-stu-id="5133a-114">The IP Address of the AirPrint destination.</span></span>|
|<span data-ttu-id="5133a-115">resourcePath</span><span class="sxs-lookup"><span data-stu-id="5133a-115">resourcePath</span></span>|<span data-ttu-id="5133a-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="5133a-116">String</span></span>|<span data-ttu-id="5133a-117">La ruta de acceso de recursos asociados con la impresora.</span><span class="sxs-lookup"><span data-stu-id="5133a-117">The Resource Path associated with the printer.</span></span> <span data-ttu-id="5133a-118">Esto corresponde al parámetro de la _ipps.tcp Bonjour registro rp.</span><span class="sxs-lookup"><span data-stu-id="5133a-118">This corresponds to the rp parameter of the _ipps.tcp Bonjour record.</span></span> <span data-ttu-id="5133a-119">Por ejemplo: Canon_MG5300_series/impresoras, impresoras/Xerox_Phaser_7600, ipp, print y Epson_IPP_Printer.</span><span class="sxs-lookup"><span data-stu-id="5133a-119">For example: printers/Canon_MG5300_series, printers/Xerox_Phaser_7600, ipp/print, Epson_IPP_Printer.</span></span>|
|<span data-ttu-id="5133a-120">port</span><span class="sxs-lookup"><span data-stu-id="5133a-120">port</span></span>|<span data-ttu-id="5133a-121">Int32</span><span class="sxs-lookup"><span data-stu-id="5133a-121">Int32</span></span>|<span data-ttu-id="5133a-122">El puerto de escucha del destino AirPrint.</span><span class="sxs-lookup"><span data-stu-id="5133a-122">The listening port of the AirPrint destination.</span></span> <span data-ttu-id="5133a-123">Si no se especifica esta clave AirPrint va a usar el puerto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5133a-123">If this key is not specified AirPrint will use the default port.</span></span> <span data-ttu-id="5133a-124">Disponible en iOS 11.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5133a-124">Available in iOS 11.0 and later.</span></span>|
|<span data-ttu-id="5133a-125">forceTls</span><span class="sxs-lookup"><span data-stu-id="5133a-125">forceTls</span></span>|<span data-ttu-id="5133a-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="5133a-126">Boolean</span></span>|<span data-ttu-id="5133a-127">Si es true conexiones AirPrint están protegidas por la seguridad de capa de transporte (TLS).</span><span class="sxs-lookup"><span data-stu-id="5133a-127">If true AirPrint connections are secured by Transport Layer Security (TLS).</span></span> <span data-ttu-id="5133a-128">Valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="5133a-128">Default is false.</span></span> <span data-ttu-id="5133a-129">Disponible en iOS 11.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5133a-129">Available in iOS 11.0 and later.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5133a-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5133a-130">Relationships</span></span>
<span data-ttu-id="5133a-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5133a-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5133a-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5133a-132">JSON Representation</span></span>
<span data-ttu-id="5133a-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5133a-133">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.airPrintDestination"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.airPrintDestination",
  "ipAddress": "String",
  "resourcePath": "String",
  "port": 1024,
  "forceTls": true
}
```





