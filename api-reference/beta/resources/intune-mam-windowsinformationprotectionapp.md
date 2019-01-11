---
title: Tipo de recurso windowsInformationProtectionApp
description: Aplicación para Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d44aa233e03a193ea0d061f55748cb0d7319a95b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809593"
---
# <a name="windowsinformationprotectionapp-resource-type"></a><span data-ttu-id="fc65e-103">Tipo de recurso windowsInformationProtectionApp</span><span class="sxs-lookup"><span data-stu-id="fc65e-103">windowsInformationProtectionApp resource type</span></span>

> <span data-ttu-id="fc65e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc65e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc65e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc65e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fc65e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fc65e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc65e-107">Aplicación para Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="fc65e-107">App for Windows information protection</span></span>
## <a name="properties"></a><span data-ttu-id="fc65e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc65e-108">Properties</span></span>
|<span data-ttu-id="fc65e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc65e-109">Property</span></span>|<span data-ttu-id="fc65e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc65e-110">Type</span></span>|<span data-ttu-id="fc65e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc65e-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fc65e-112">displayName</span><span class="sxs-lookup"><span data-stu-id="fc65e-112">displayName</span></span>|<span data-ttu-id="fc65e-113">cadena</span><span class="sxs-lookup"><span data-stu-id="fc65e-113">String</span></span>|<span data-ttu-id="fc65e-114">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc65e-114">App display name.</span></span>|
|<span data-ttu-id="fc65e-115">descripción</span><span class="sxs-lookup"><span data-stu-id="fc65e-115">description</span></span>|<span data-ttu-id="fc65e-116">cadena</span><span class="sxs-lookup"><span data-stu-id="fc65e-116">String</span></span>|<span data-ttu-id="fc65e-117">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc65e-117">The app's description.</span></span>|
|<span data-ttu-id="fc65e-118">publisherName</span><span class="sxs-lookup"><span data-stu-id="fc65e-118">publisherName</span></span>|<span data-ttu-id="fc65e-119">cadena</span><span class="sxs-lookup"><span data-stu-id="fc65e-119">String</span></span>|<span data-ttu-id="fc65e-120">El nombre del editor</span><span class="sxs-lookup"><span data-stu-id="fc65e-120">The publisher name</span></span>|
|<span data-ttu-id="fc65e-121">productName</span><span class="sxs-lookup"><span data-stu-id="fc65e-121">productName</span></span>|<span data-ttu-id="fc65e-122">cadena</span><span class="sxs-lookup"><span data-stu-id="fc65e-122">String</span></span>|<span data-ttu-id="fc65e-123">El nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="fc65e-123">The product name.</span></span>|
|<span data-ttu-id="fc65e-124">denegado</span><span class="sxs-lookup"><span data-stu-id="fc65e-124">denied</span></span>|<span data-ttu-id="fc65e-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="fc65e-125">Boolean</span></span>|<span data-ttu-id="fc65e-126">Si es true, se deniega la protección o la exención a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc65e-126">If true, app is denied protection or exemption.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fc65e-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fc65e-127">Relationships</span></span>
<span data-ttu-id="fc65e-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fc65e-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fc65e-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fc65e-129">JSON Representation</span></span>
<span data-ttu-id="fc65e-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fc65e-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionApp",
  "displayName": "String",
  "description": "String",
  "publisherName": "String",
  "productName": "String",
  "denied": true
}
```





