---
title: Tipo de recurso windowsInformationProtectionApp
description: Aplicación para Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8d025b20e5341c17f756e86bb6bb84faf92a61a3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971882"
---
# <a name="windowsinformationprotectionapp-resource-type"></a><span data-ttu-id="592c1-103">Tipo de recurso windowsInformationProtectionApp</span><span class="sxs-lookup"><span data-stu-id="592c1-103">windowsInformationProtectionApp resource type</span></span>

> <span data-ttu-id="592c1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="592c1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="592c1-105">Aplicación para Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="592c1-105">App for Windows information protection</span></span>
## <a name="properties"></a><span data-ttu-id="592c1-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="592c1-106">Properties</span></span>
|<span data-ttu-id="592c1-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="592c1-107">Property</span></span>|<span data-ttu-id="592c1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="592c1-108">Type</span></span>|<span data-ttu-id="592c1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="592c1-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="592c1-110">displayName</span><span class="sxs-lookup"><span data-stu-id="592c1-110">displayName</span></span>|<span data-ttu-id="592c1-111">cadena</span><span class="sxs-lookup"><span data-stu-id="592c1-111">String</span></span>|<span data-ttu-id="592c1-112">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="592c1-112">App display name.</span></span>|
|<span data-ttu-id="592c1-113">descripción</span><span class="sxs-lookup"><span data-stu-id="592c1-113">description</span></span>|<span data-ttu-id="592c1-114">cadena</span><span class="sxs-lookup"><span data-stu-id="592c1-114">String</span></span>|<span data-ttu-id="592c1-115">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="592c1-115">The app's description.</span></span>|
|<span data-ttu-id="592c1-116">publisherName</span><span class="sxs-lookup"><span data-stu-id="592c1-116">publisherName</span></span>|<span data-ttu-id="592c1-117">cadena</span><span class="sxs-lookup"><span data-stu-id="592c1-117">String</span></span>|<span data-ttu-id="592c1-118">El nombre del editor</span><span class="sxs-lookup"><span data-stu-id="592c1-118">The publisher name</span></span>|
|<span data-ttu-id="592c1-119">productName</span><span class="sxs-lookup"><span data-stu-id="592c1-119">productName</span></span>|<span data-ttu-id="592c1-120">cadena</span><span class="sxs-lookup"><span data-stu-id="592c1-120">String</span></span>|<span data-ttu-id="592c1-121">El nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="592c1-121">The product name.</span></span>|
|<span data-ttu-id="592c1-122">denegado</span><span class="sxs-lookup"><span data-stu-id="592c1-122">denied</span></span>|<span data-ttu-id="592c1-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="592c1-123">Boolean</span></span>|<span data-ttu-id="592c1-124">Si es true, se deniega la protección o la exención a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="592c1-124">If true, app is denied protection or exemption.</span></span>|

## <a name="relationships"></a><span data-ttu-id="592c1-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="592c1-125">Relationships</span></span>
<span data-ttu-id="592c1-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="592c1-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="592c1-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="592c1-127">JSON Representation</span></span>
<span data-ttu-id="592c1-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="592c1-128">Here is a JSON representation of the resource.</span></span>
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



