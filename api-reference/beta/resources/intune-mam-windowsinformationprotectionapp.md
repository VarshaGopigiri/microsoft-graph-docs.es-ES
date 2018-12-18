---
title: Tipo de recurso windowsInformationProtectionApp
description: Aplicación para Windows Information Protection
author: tfitzmac
ms.openlocfilehash: 6ad47301dc7ec9650026021a2131d34b4d704e70
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334387"
---
# <a name="windowsinformationprotectionapp-resource-type"></a><span data-ttu-id="adc08-103">Tipo de recurso windowsInformationProtectionApp</span><span class="sxs-lookup"><span data-stu-id="adc08-103">windowsInformationProtectionApp resource type</span></span>

> <span data-ttu-id="adc08-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="adc08-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="adc08-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="adc08-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="adc08-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="adc08-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="adc08-107">Aplicación para Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="adc08-107">App for Windows information protection</span></span>
## <a name="properties"></a><span data-ttu-id="adc08-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="adc08-108">Properties</span></span>
|<span data-ttu-id="adc08-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="adc08-109">Property</span></span>|<span data-ttu-id="adc08-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="adc08-110">Type</span></span>|<span data-ttu-id="adc08-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="adc08-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="adc08-112">displayName</span><span class="sxs-lookup"><span data-stu-id="adc08-112">displayName</span></span>|<span data-ttu-id="adc08-113">cadena</span><span class="sxs-lookup"><span data-stu-id="adc08-113">String</span></span>|<span data-ttu-id="adc08-114">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="adc08-114">App display name.</span></span>|
|<span data-ttu-id="adc08-115">descripción</span><span class="sxs-lookup"><span data-stu-id="adc08-115">description</span></span>|<span data-ttu-id="adc08-116">cadena</span><span class="sxs-lookup"><span data-stu-id="adc08-116">String</span></span>|<span data-ttu-id="adc08-117">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="adc08-117">The app's description.</span></span>|
|<span data-ttu-id="adc08-118">publisherName</span><span class="sxs-lookup"><span data-stu-id="adc08-118">publisherName</span></span>|<span data-ttu-id="adc08-119">cadena</span><span class="sxs-lookup"><span data-stu-id="adc08-119">String</span></span>|<span data-ttu-id="adc08-120">El nombre del editor</span><span class="sxs-lookup"><span data-stu-id="adc08-120">The publisher name</span></span>|
|<span data-ttu-id="adc08-121">productName</span><span class="sxs-lookup"><span data-stu-id="adc08-121">productName</span></span>|<span data-ttu-id="adc08-122">cadena</span><span class="sxs-lookup"><span data-stu-id="adc08-122">String</span></span>|<span data-ttu-id="adc08-123">El nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="adc08-123">The product name.</span></span>|
|<span data-ttu-id="adc08-124">denegado</span><span class="sxs-lookup"><span data-stu-id="adc08-124">denied</span></span>|<span data-ttu-id="adc08-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="adc08-125">Boolean</span></span>|<span data-ttu-id="adc08-126">Si es true, se deniega la protección o la exención a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="adc08-126">If true, app is denied protection or exemption.</span></span>|

## <a name="relationships"></a><span data-ttu-id="adc08-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="adc08-127">Relationships</span></span>
<span data-ttu-id="adc08-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="adc08-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="adc08-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="adc08-129">JSON Representation</span></span>
<span data-ttu-id="adc08-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="adc08-130">Here is a JSON representation of the resource.</span></span>
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





