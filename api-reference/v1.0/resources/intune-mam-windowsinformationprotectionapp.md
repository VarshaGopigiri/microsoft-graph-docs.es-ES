---
title: Tipo de recurso windowsInformationProtectionApp
description: Aplicación para Windows Information Protection
author: tfitzmac
ms.openlocfilehash: 480d9d2b1d8049eebb664923c0b1e31bd86bd9da
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337481"
---
# <a name="windowsinformationprotectionapp-resource-type"></a><span data-ttu-id="ab0fb-103">Tipo de recurso windowsInformationProtectionApp</span><span class="sxs-lookup"><span data-stu-id="ab0fb-103">windowsInformationProtectionApp resource type</span></span>

> <span data-ttu-id="ab0fb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab0fb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab0fb-105">Aplicación para Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="ab0fb-105">App for Windows information protection</span></span>
## <a name="properties"></a><span data-ttu-id="ab0fb-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab0fb-106">Properties</span></span>
|<span data-ttu-id="ab0fb-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab0fb-107">Property</span></span>|<span data-ttu-id="ab0fb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab0fb-108">Type</span></span>|<span data-ttu-id="ab0fb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab0fb-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab0fb-110">displayName</span><span class="sxs-lookup"><span data-stu-id="ab0fb-110">displayName</span></span>|<span data-ttu-id="ab0fb-111">cadena</span><span class="sxs-lookup"><span data-stu-id="ab0fb-111">String</span></span>|<span data-ttu-id="ab0fb-112">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab0fb-112">App display name.</span></span>|
|<span data-ttu-id="ab0fb-113">descripción</span><span class="sxs-lookup"><span data-stu-id="ab0fb-113">description</span></span>|<span data-ttu-id="ab0fb-114">cadena</span><span class="sxs-lookup"><span data-stu-id="ab0fb-114">String</span></span>|<span data-ttu-id="ab0fb-115">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab0fb-115">The app's description.</span></span>|
|<span data-ttu-id="ab0fb-116">publisherName</span><span class="sxs-lookup"><span data-stu-id="ab0fb-116">publisherName</span></span>|<span data-ttu-id="ab0fb-117">cadena</span><span class="sxs-lookup"><span data-stu-id="ab0fb-117">String</span></span>|<span data-ttu-id="ab0fb-118">El nombre del editor</span><span class="sxs-lookup"><span data-stu-id="ab0fb-118">The publisher name</span></span>|
|<span data-ttu-id="ab0fb-119">productName</span><span class="sxs-lookup"><span data-stu-id="ab0fb-119">productName</span></span>|<span data-ttu-id="ab0fb-120">cadena</span><span class="sxs-lookup"><span data-stu-id="ab0fb-120">String</span></span>|<span data-ttu-id="ab0fb-121">El nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="ab0fb-121">The product name.</span></span>|
|<span data-ttu-id="ab0fb-122">denegado</span><span class="sxs-lookup"><span data-stu-id="ab0fb-122">denied</span></span>|<span data-ttu-id="ab0fb-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab0fb-123">Boolean</span></span>|<span data-ttu-id="ab0fb-124">Si es true, se deniega la protección o la exención a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab0fb-124">If true, app is denied protection or exemption.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ab0fb-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ab0fb-125">Relationships</span></span>
<span data-ttu-id="ab0fb-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ab0fb-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ab0fb-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab0fb-127">JSON Representation</span></span>
<span data-ttu-id="ab0fb-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ab0fb-128">Here is a JSON representation of the resource.</span></span>
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



