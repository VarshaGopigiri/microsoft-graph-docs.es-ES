---
title: Tipo de recurso windowsInformationProtectionDesktopApp
description: Aplicación de escritorio de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: 5164e6d1a9165139de1895dfae38dd8c90927504
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345517"
---
# <a name="windowsinformationprotectiondesktopapp-resource-type"></a><span data-ttu-id="60e23-103">Tipo de recurso windowsInformationProtectionDesktopApp</span><span class="sxs-lookup"><span data-stu-id="60e23-103">windowsInformationProtectionDesktopApp resource type</span></span>

> <span data-ttu-id="60e23-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="60e23-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="60e23-105">Aplicación de escritorio de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="60e23-105">Desktop App for Windows information protection</span></span>

<span data-ttu-id="60e23-106">Hereda de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="60e23-106">Inherits from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>

## <a name="properties"></a><span data-ttu-id="60e23-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60e23-107">Properties</span></span>
|<span data-ttu-id="60e23-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60e23-108">Property</span></span>|<span data-ttu-id="60e23-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="60e23-109">Type</span></span>|<span data-ttu-id="60e23-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="60e23-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="60e23-111">displayName</span><span class="sxs-lookup"><span data-stu-id="60e23-111">displayName</span></span>|<span data-ttu-id="60e23-112">cadena</span><span class="sxs-lookup"><span data-stu-id="60e23-112">String</span></span>|<span data-ttu-id="60e23-113">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60e23-113">App display name.</span></span> <span data-ttu-id="60e23-114">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="60e23-114">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="60e23-115">descripción</span><span class="sxs-lookup"><span data-stu-id="60e23-115">description</span></span>|<span data-ttu-id="60e23-116">cadena</span><span class="sxs-lookup"><span data-stu-id="60e23-116">String</span></span>|<span data-ttu-id="60e23-117">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60e23-117">The app's description.</span></span> <span data-ttu-id="60e23-118">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="60e23-118">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="60e23-119">publisherName</span><span class="sxs-lookup"><span data-stu-id="60e23-119">publisherName</span></span>|<span data-ttu-id="60e23-120">cadena</span><span class="sxs-lookup"><span data-stu-id="60e23-120">String</span></span>|<span data-ttu-id="60e23-121">Nombre del publicador. Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="60e23-121">The publisher name Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="60e23-122">productName</span><span class="sxs-lookup"><span data-stu-id="60e23-122">productName</span></span>|<span data-ttu-id="60e23-123">cadena</span><span class="sxs-lookup"><span data-stu-id="60e23-123">String</span></span>|<span data-ttu-id="60e23-124">El nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="60e23-124">The product name.</span></span> <span data-ttu-id="60e23-125">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="60e23-125">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="60e23-126">denegado</span><span class="sxs-lookup"><span data-stu-id="60e23-126">denied</span></span>|<span data-ttu-id="60e23-127">Booleano</span><span class="sxs-lookup"><span data-stu-id="60e23-127">Boolean</span></span>|<span data-ttu-id="60e23-128">Si es true, se deniega la protección o la exención a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60e23-128">If true, app is denied protection or exemption.</span></span> <span data-ttu-id="60e23-129">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="60e23-129">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="60e23-130">binaryName</span><span class="sxs-lookup"><span data-stu-id="60e23-130">binaryName</span></span>|<span data-ttu-id="60e23-131">cadena</span><span class="sxs-lookup"><span data-stu-id="60e23-131">String</span></span>|<span data-ttu-id="60e23-132">El nombre del binario.</span><span class="sxs-lookup"><span data-stu-id="60e23-132">The binary name.</span></span>|
|<span data-ttu-id="60e23-133">binaryVersionLow</span><span class="sxs-lookup"><span data-stu-id="60e23-133">binaryVersionLow</span></span>|<span data-ttu-id="60e23-134">cadena</span><span class="sxs-lookup"><span data-stu-id="60e23-134">String</span></span>|<span data-ttu-id="60e23-135">La versión binaria inferior.</span><span class="sxs-lookup"><span data-stu-id="60e23-135">The lower binary version.</span></span>|
|<span data-ttu-id="60e23-136">binaryVersionHigh</span><span class="sxs-lookup"><span data-stu-id="60e23-136">binaryVersionHigh</span></span>|<span data-ttu-id="60e23-137">cadena</span><span class="sxs-lookup"><span data-stu-id="60e23-137">String</span></span>|<span data-ttu-id="60e23-138">La versión binaria superior.</span><span class="sxs-lookup"><span data-stu-id="60e23-138">The high binary version.</span></span>|

## <a name="relationships"></a><span data-ttu-id="60e23-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="60e23-139">Relationships</span></span>
<span data-ttu-id="60e23-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="60e23-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="60e23-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60e23-141">JSON Representation</span></span>
<span data-ttu-id="60e23-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="60e23-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDesktopApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDesktopApp",
  "displayName": "String",
  "description": "String",
  "publisherName": "String",
  "productName": "String",
  "denied": true,
  "binaryName": "String",
  "binaryVersionLow": "String",
  "binaryVersionHigh": "String"
}
```



