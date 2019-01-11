---
title: Tipo de recurso windowsInformationProtectionStoreApp
description: Aplicación de la tienda de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4e78aa854b15763cade9a4d6020f1737bbca1642
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814479"
---
# <a name="windowsinformationprotectionstoreapp-resource-type"></a><span data-ttu-id="14021-103">Tipo de recurso windowsInformationProtectionStoreApp</span><span class="sxs-lookup"><span data-stu-id="14021-103">windowsInformationProtectionStoreApp resource type</span></span>

> <span data-ttu-id="14021-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="14021-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="14021-105">Aplicación de la tienda de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="14021-105">Store App for Windows information protection</span></span>

<span data-ttu-id="14021-106">Hereda de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="14021-106">Inherits from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>

## <a name="properties"></a><span data-ttu-id="14021-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14021-107">Properties</span></span>
|<span data-ttu-id="14021-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14021-108">Property</span></span>|<span data-ttu-id="14021-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="14021-109">Type</span></span>|<span data-ttu-id="14021-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="14021-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="14021-111">displayName</span><span class="sxs-lookup"><span data-stu-id="14021-111">displayName</span></span>|<span data-ttu-id="14021-112">cadena</span><span class="sxs-lookup"><span data-stu-id="14021-112">String</span></span>|<span data-ttu-id="14021-113">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14021-113">App display name.</span></span> <span data-ttu-id="14021-114">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="14021-114">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="14021-115">descripción</span><span class="sxs-lookup"><span data-stu-id="14021-115">description</span></span>|<span data-ttu-id="14021-116">cadena</span><span class="sxs-lookup"><span data-stu-id="14021-116">String</span></span>|<span data-ttu-id="14021-117">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14021-117">The app's description.</span></span> <span data-ttu-id="14021-118">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="14021-118">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="14021-119">publisherName</span><span class="sxs-lookup"><span data-stu-id="14021-119">publisherName</span></span>|<span data-ttu-id="14021-120">cadena</span><span class="sxs-lookup"><span data-stu-id="14021-120">String</span></span>|<span data-ttu-id="14021-121">Nombre del publicador. Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="14021-121">The publisher name Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="14021-122">productName</span><span class="sxs-lookup"><span data-stu-id="14021-122">productName</span></span>|<span data-ttu-id="14021-123">cadena</span><span class="sxs-lookup"><span data-stu-id="14021-123">String</span></span>|<span data-ttu-id="14021-124">El nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="14021-124">The product name.</span></span> <span data-ttu-id="14021-125">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="14021-125">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|
|<span data-ttu-id="14021-126">denegado</span><span class="sxs-lookup"><span data-stu-id="14021-126">denied</span></span>|<span data-ttu-id="14021-127">Booleano</span><span class="sxs-lookup"><span data-stu-id="14021-127">Boolean</span></span>|<span data-ttu-id="14021-128">Si es true, se deniega la protección o la exención a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14021-128">If true, app is denied protection or exemption.</span></span> <span data-ttu-id="14021-129">Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="14021-129">Inherited from [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="14021-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="14021-130">Relationships</span></span>
<span data-ttu-id="14021-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="14021-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="14021-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14021-132">JSON Representation</span></span>
<span data-ttu-id="14021-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="14021-133">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionStoreApp",
  "displayName": "String",
  "description": "String",
  "publisherName": "String",
  "productName": "String",
  "denied": true
}
```



